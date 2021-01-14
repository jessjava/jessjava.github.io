---
title: nginx开机自启动
date: 2021-01-13 20:49:29 +0800
categories: 脚本
tag: server
---

## 在linux系统 /etc/init.d/目录下创建nginx文件

```bash
vim /etc/init.d/nginx
```

## 脚本内容
按照nginx官网 <a target="_blank" href="http://wiki.nginx.org/RedHatNginxInitScript">脚本</a>，编辑脚本内容。

```bash
#修改为自己安装nginx的启动脚本
nginx="/usr/local/nginx/sbin/nginx"

#修改为自己安装nginx的配置文件
NGINX_CONFIG_FILE="/etc/nginx/nginx.conf"
```   

## 设置权限

保存脚本文件后设置文件的执行权限：

```bash
chmod a+x /etc/init.d/nginx
```

## chkconfig开机启动配置

```bash
#nginx服务加入chkconfig管理列表：
chkconfig --add /etc/init.d/nginx

#开启
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

