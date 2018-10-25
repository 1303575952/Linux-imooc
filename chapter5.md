# SSH工具

## SSH是什么

* SSH：Secure Shell 安全外壳协议
* 建立在应用层基础上的安全协议
* 可靠，专为远程登录会话和其他网络服务提供安全性协议
* 有效防止远程管理过程中的信息泄露问题
* SSH客户端适用于多种平台
* SSH服务端几乎支持所有UNIX平台

## 服务器安装SSH服务

* 安装SSH命令
> yum install openssh-server

* 启动SSH
> service sshd start

* 设置开机运行
> chkconfig sshd on

## 客户端安装SSH服务

* SSH是典型的客户端和服务端的交互模式，客户端广泛的支持各个平台
* Windows有很多工具支持SSH连接功能，例如Xshell，Putty，secureCRT
* Linux平台需安装客户端软件
> yum install openssh-clients

* 连接到服务器
> ssh username@ip

## SSH config讲解

* config为了方便我们批量管理多个ssh
* config存放在~/.ssh/config
* config配置语法

**~/.ssh/config文件配置可保证多用户登录**

## SSH安全免密码登录：ssh key

* ssh key使用非对称加密方式生成公钥和私钥
* 私钥存放在本地~/.ssh目录
* 公钥可以对外公开，放在服务器的~/.ssh/authorized_keys
* Linux平台生成ssh key
> ssh-keygen -t rsa或ssh-keygen -t dsa

**非对称加密：公钥加密私钥解密/私钥加密公钥解密**

## SSH安全端口

* 端口安全是为避免服务器远程连接端口被不法分子直到，为此改变默认端口的操作

* 改变SSH服务端口：修改/etc/ssh/sshd_config配置
