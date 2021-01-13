---
title: nginx开机自启动
date: 2021-01-13 20:49:29 +0800
categories: 脚本
tag: server
---

## /etc/init.d

首先，在linux系统的/etc/init.d/目录下创建nginx文件

```bash
vim /etc/init.d/nginx
```

## 脚本内容
按照nginx官网 http://wiki.nginx.org/RedHatNginxInitScript脚本，编辑脚本内容。

修改 nginx="/usr/local/nginx/sbin/nginx"    #修改为自己安装nginx的启动脚本

NGINX_CONFIG_FILE="/etc/nginx/nginx.conf"    #修改为自己安装nginx的配置文件

## 脚本权限

保存脚本文件后设置文件的执行权限：

chmod a+x /etc/init.d/nginx

## 自动启动配置

使用chkconfig管理

先将nginx服务加入chkconfig管理列表：

```bash

chkconfig --add /etc/init.d/nginx

chkconfig nginx on
```


## service管理


```bash
/etc/init.d/nginx start

/etc/init.d/nginx stop
```

```bash
service nginx start

service nginx stop
```

