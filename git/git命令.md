# 基本配置
---
设置用户信息
`git config --global user.name"***"`

`git config --global user.email"****@**"`

查看配置信息
`git config --global user.name`

`git config --global user.email`

![Alt text](image.png)

# 基础操作指令

创建仓库 
1. 进入需要进行出创建仓库的文件夹
2. 输入命令 
   `git init`
3. 添加文件到git
`git add .`
4. 提交
`git commit -m "first commit"`
5. 将当前分支重命名为main
`git branch -M main`
6. 与远程仓库建立连接
`git remote add origin https://github.com/Syhaun/XIEJIAYUE.git`
7. 将本地main推送到名为origin的远程仓库
`git push -u origin main`

从远程仓库克隆
`git clone 远程Git仓库地址`





