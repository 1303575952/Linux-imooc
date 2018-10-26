# WebServer

## Apache

* Apache基本操作

解释|命令
:--:|:--:
安装|yum install httpd
启动|service httpd start
停止|service httpd stop

* Apache的虚拟主机配置

在/etc/httpd/conf/httpd.conf中配置，配置格式如下
```
<VirtualHost *:80>
    ServerName www.imooc.test
    DocumentRoot /data/www
    <Directory "/data/www">
        Options Indexes FollowSymLinks
        AllowOverride Node
        Require all granted
    </Directory>
</VirtualHost>
```

* Apache伪静态操作

在/etc/httpd/conf/httpd.conf中配置，配置格式如下
```
LoadModule rewrite_module modules/mod_rewrite.so
```
```
<VirtualHost *:80>
    ServerName www.imooc.test
    DocumentRoot /data/www
    <Directory "/data/www">
        Options Indexes FollowSymLinks
        AllowOverride Node
        Require all granted
        <IfModule mod_rewrite.c>
            RewriteEngine On
            RewriteRule ^(.*).htmm$ index.html
        </IfModule>
    </Directory>
</VirtualHost>
```

## Nginx

* Nginx基本操作
