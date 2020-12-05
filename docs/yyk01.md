# Ubuntu关于SSH的安装与使用

## 一、在Ubuntu上启用SSH

sudo apt update  	//检查ubuntu的更新

sudo apt install openssh-server	//安装openssh-server

sudo systemctl status ssh	//验证SSH是否在运行

sudo ufw allow ssh	//打开SSH端口

## 二、连接到SSH服务器

ssh username@ip_address	//username是你的用户名，ip_address是你安装ssh的IP地址。

ip a 	//来查看自己系统的ip地址

## 三、在Ubuntu上禁用SSH

sudo systemctl disable 	--now ssh	//停止

sudo systemctl enable      --now ssh	//重新启用



