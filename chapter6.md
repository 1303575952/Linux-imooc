# Linux常用命令

* 软件操作命令
* 服务器硬件资源和磁盘操作
* 文件和文件夹操作命令
* 系统用户操作命令
* 防火墙相关设置
* 提权操作sudo和文件传输操作

## 软件操作命令

* 软件包管理：yum
* 安装软件：yum install xxx
* 卸载软件：yum remove xxx
* 搜索软件：yum search xxx
* 清理缓存：yum clean packages
* 列出已安装：yum list
* 软件包信息：yum info xxx

## 服务器硬件信息资源

* 内存：free -m
* 硬盘：df -h
* 负载：w/top
* cpu个数和核数：cat /proc/info

## 文件操作命令

* Linux文件的目录结构
   + 根目录 /
   + 家目录 /home
   + 临时目录 /tmp
   + 配置文件 /etc
   + 用户程序 /usr
* 文件基本操作
* 文本编辑神器vim
* 文件权限421
* 文件搜索、查找、读取

命令|解释
:--:|:--:
tail|从文件尾部开始读
head|从文件头部读
cat|读取整个文件
more|分页读取
less|可控分页
grep|搜索关键字
find|查找文件
wc|统计个数

* 文件压缩与解压

## 系统用户操作命令

命令|解释
:--:|:--:
useradd或adduser|添加用户
userdel|删除用户
passwd|设置密码

## 防火墙设置

* 作用：保护服务器安全
* 设置防火墙规则

操作|命令
:--:|:--:
安装|yum install firewalld
启动|service firewalld start
检查状态|service firewalld status
关闭或禁用防火墙|service firewalld stop/disable

## 提权和文件上传下载操作

* 提权：sudo
   + visudo
* 文件下载
   + wget、curl
* 文件上传
   + scp
