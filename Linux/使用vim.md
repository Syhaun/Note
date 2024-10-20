# vim 的模式

## 创建加密文档
`vim -x file1`

### 普通模式

vim打开后默认的模式就是普通方式

![alt text](image-19.png)

一般按 *i* 或者 *a* 进入 插入模式

![alt text](image-20.png)

![alt text](image-24.png)

![alt text](image-25.png)

普通模式下 `.`可以用作重复上一次的命令的操作

`N+命令`,表示该命令重复执行N次

![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)

![alt text](image-29.png)

![alt text](image-30.png)

![alt text](image-31.png)

![alt text](image-32.png)

![alt text](image-33.png)

![alt text](image-34.png)

![alt text](image-35.png)

### 插入模式

插入文本,按 *ESC*返回普通模式

### 命令模式

![alt text](image-21.png)

![alt text](image-23.png)

### 可视模式

![alt text](image-36.png)


# 视窗操作

![alt text](image-37.png)

### 在vim执行外部命令

`:!ls`:用于显示当前目录的内容
`!rm FILENAME`:用于删除名为FILENAME的文件
`:w FILENAME`:将当前vim中正在编辑的文件另存为FILENAME文件 

### vim的功能设定

![alt text](image-38.png)

