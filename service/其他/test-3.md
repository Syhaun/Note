## 获取root用户权限
sudo -i
## 配置服务器静态ip
```shell
cat > /etc/netplan/ens33.yaml <<EOF 2> /tmp/auto-init-system.log && netplan apply 2> /tmp/auto-init-system.log
network:
  ethernets:
    ens33:
      dhcp4: false
      addresses: [192.168.30.31/24]
      gateway4: 192.168.30.2
      nameservers:
        addresses: [114.114.114.114]
  version: 2
EOF
```
## 允许root用户登陆
vim /etc/ssh/sshd_config
PermitRootLogin yes
systemctl reload sshd
passwd root
## 配置南京源
sed -i 's/http.*ubuntu.com/https:\/\/mirror.nju.edu.cn/' /etc/apt/sources.list
## 安装系统组件
apt install -y open-vm-tools vim wget curl bash-completion gcc net-tools
## 安装docker
bash auto_install_docker.sh
# 启动docker
systemctl start docker
# 设置docker开机自启
systemctl enable docker
## 查看容器
docker ps
## 查看所有容器
docker ps -a
## 查看镜像
docker images
## 导入镜像
docker load -i mysql-8.3.0.tar

## 启动容器
docker run -d -p 81:80 --name nginx1 nginx
docker run -d -p 8080:80 nginx
docker run -p 81:80 nginx

## 停止容器
docker stop <container_name>
## 杀死容器
docker kill <container_name>
## 删除容器
docker rm <container_name>
## 挂载卷
docker run -d -p 8080:80 -v ./data:/data nginx
## 在容器中执行命令
docker exec <container_name> <command>
docker exec -it <container_name> /bin/sh
## 快速删除容器
docker ps -q | xargs docker kill
docker ps -aq | xargs docker rm

## docker-compose.yaml
vim docker-compose.yaml
mkdir -p mysql/conf
mkdir -p mysql/data
mkdir -p mysql/log
vim mysql/conf/mysql.cnf
docker compose up -d
## 安装mysql客户端
apt install -y mysql-client-core-8.0
## 登陆mysql
mysql -h 127.0.0.1 -P 3306 -p1234 -u root
mysql -p1234 -u root
## sql语句
show databases;
show variables like 'server_id';