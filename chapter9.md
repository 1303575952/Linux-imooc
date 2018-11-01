# 缓存服务

## Memcached基本操作

解释|命令
:--:|:--:
安装|yum install memcached
启动|memcached -d -l -m -p
停止|kill pid

## Redis基本操作

解释|命令
:--:|:--:
安装|源码编译安装
启动|redis-server start/restart
停止|redis-server stop
客户端|redis-client

## Redis拓展知识

* Redis不仅仅支持简单的k/v类型的数据，同时还提供list，set，hash等数据结构的存储
* Redis支持数据的备份，即master-slave模式的数据备份
* Redis支持数据的持久化，可以将内存中的数据保存在磁盘中，重启的时候可以再次加载进行使用
