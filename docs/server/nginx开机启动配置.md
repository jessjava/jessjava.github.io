# /etc/init.d/nginx

首先，在linux系统的/etc/init.d/目录下创建nginx文件，使用如下命令：

vim /etc/init.d/nginx

# 编辑脚本

按照官网[http://wiki.nginx.org/RedHatNginxInitScript](http://wiki.nginx.org/RedHatNginxInitScript?spm=a2c6h.12873639.0.0.17cd5ad2RsrlMi)脚本，编辑脚本内容。

修改nginx="/usr/local/nginx/sbin/nginx"  #修改为自己安装nginx的启动脚本

NGINX_CONFIG_FILE="/etc/nginx/nginx.conf"  #修改为自己安装nginx的配置文件

# 执行权限

保存脚本文件后设置文件的执行权限：

chmod a+x /etc/init.d/nginx

就可以通过该脚本对nginx服务进行管理：

/etc/init.d/nginx start

/etc/init.d/nginx stop

# 使用chkconfig管理

先将nginx服务加入chkconfig管理列表：

chkconfig --add /etc/init.d/nginx



service nginx start

service nginx stop

# 设置启动开启

chkconfig nginx on

