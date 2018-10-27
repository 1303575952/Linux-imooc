# MySQL

## MySQL基本操作

解释|命令
:--:|:--:
安装服务端|yum install mysql-community-server
启动|service mysqld start/restart
停止|service mysqld stop

## MySQL密码

* MySQL查看安装完成后默认生成的密码

```
cat /var/log/mysqld.log|grep password
```

* MySQL修改默认密码

```
set global validate_password_policy = 0;
set global validate_password_length = 1;
set password = password('123456');
```
其中前面两行是为方便设置简单密码

## MySQL远程连接

* 更新MySQL的user表，设置允许远程连接
* flush privileges或service mysqld restart
* 主机防火墙

## 开启genelog

* genelog用于记录用户的操作

```
set global general_log_file='/tmp/general.log';
set global general_log=on;
```

## 新建用户及赋予权限

## 找回MySQL密码

* 修改/etc/my.cnf,增加一行,跳出安全认证环节

```
skip-grant-tables
```

* 进入MySQL，执行
```
update user set authentication_string = password("password") where user = 'root';
flush privileges;
```

* 删除先前堆/etc/my.cnf的修改，重启MySQL
