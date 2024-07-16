`shell`是一个命令行解释器，可以接收用户的命令并调用操作系统的内核执行这些命令，并执行的结果的结果返回给用户

```shell
echo $SHELL #查看操作系统默认使用的shell
echo $0 #查看当前执行的脚本名称
cat /etc/shells #查看系统支持的所有shell
```

### shell脚本示例
```shell
#!/bin/bash #声明执行该脚本的解释器

read name #read函数是系统调用函数，它会把用户的输入读到name变量中，name变量不用提前声明，在read之前可以添加一些提示输入的显示

echo $# #传递给脚本参数的个数
echo $? #上一个命令的退出码，0表示没有错误，非0表示上一个命令执行出错
echo $* #传递给脚本的所有参数,将所有参数合并为一个字符串，使用for进行遍历是它只有一个参数，即那个字符串 for arg in $*;do echo $arg ;done
echo $@ #传递给脚本的所有参数,每个参数仍然保持独立，使用for循环遍历时可以逐个遍历传递给脚本的参数 for arg in $@;do echo $arg ;done
echo $$ #当前执行该脚本的shell的进程ID
echo $! #最后一个后台进程的进程ID
echo $0 #当前脚本的名称,是脚本文件的名称,例如example.sh,不是脚本的路径
echo $1 #传递给脚本的第一个参数
echo $2 #传递给脚本的第二个参数，没有第二个参数不会报错，只会显示一个空行
```
`bash shell.sh`可以执行脚本，不需要脚本具有执行权限
`./shell.sh`也可以执行脚本，但是需要脚本具有执行权限

```shell
#!/bin/sh
for arg in $@;do echo $arg ;done
echo $! #不会显示pid，因为没有后台进程

#!/bin/sh
for arg in $@;do echo $arg ;done
sleep 1 &
echo $! #sleep 1 &是一个后台进程，会显示它的进程id
```

### 普通变量和环境变量

普通变量是仅在当前shell或脚本中有效的变量，这些变量在定义后不会自动传递给子进程

环境变量可以传递给子进程，使用export命令可以把普通变量转换为环境变量，例如：export <var_name> 或者 export <var_name>=<value>

使用$<var_name>可以获取到变量的值

export命令可以把普通变量转换为环境变量，但是它依然是临时的，在退出shell后，声明的变量也会被销毁，在下次登陆是还需要重新声明变量。

想要使一个变量永久生效，可以把export命令声明在shell初始化的配置文件(用户登陆时系统默认执行的脚本文件)中。例如~/.bash_profile和~/.bashrc,~/.bash_profile和~/.bashrc的关系是~/.bash_profile是用户登陆时shell默认执行的脚本文件，但是~/.bash_profile中会执行~/.bashrc脚本文件，推荐把环境变量声明在~/.bashrc中。

/etc/profile是操作系统级别的配置脚本，它会把/etc/profile.d目录下的脚本全部执行一遍，用户在登陆时，会先执行/etc/profile再执行~/.bash_profile为用户的shell初始化环境。

~/.bash_profile是用户级别的配置脚本

登陆式shell会执行/etc/profile,非登陆式shell会执行/etc/bashrc

~是shell解释器中的一个特殊字符，类似于转义字符(\n等)，shell执行命令时会把~替换为用户的家目录路径