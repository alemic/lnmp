lnmp
====

a modified lnmp script based on www.lnmp.org more suitable to Tencent QCloud


非常感谢licess, 为了更加适合在QCloud机器上使用现在做如下更改               
ReEdit by levychang <changliwei07@gmail.com>                               
修改目的：                                                                 
1.采用淘宝的Tengine代替nginx，详情http://tengine.taobao.org/index_cn.html  
2.为了更加适合QCloud产品的磁盘划分，网站的根目录移到/data/www下            
本文档是基于CentOS（或定制化的基于CentOS的Tlinux系统基础上）操作系统       
不适合SuSE和Ubuntu                                                         
免责声明：                                                                 
本文档紧供参考！本文档紧供参考！本文档紧供参考！                           
文档中的描述和相关步骤不要理解为自然而然的必然                             
作者保留权力并不对文档的正确性、完整性和质量有效性负责。                   
文档质量内容不提供任何额外保障                                             

LNMP状态管理： /root/lnmp {start|stop|reload|restart|kill|status}
LNMPA状态管理： /root/lnmpa {start|stop|reload|restart|kill|status}
Nginx状态管理：/etc/init.d/nginx {start|stop|reload|restart}
PHP-FPM状态管理：/etc/init.d/php-fpm {start|stop|quit|restart|reload|logrotate}
PureFTPd状态管理： /root/pureftpd {start|stop|restart|kill|status}
MySQL状态管理：/etc/init.d/mysql {start|stop|restart|reload|force-reload|status}
Apache状态管理：/root/httpd {start|stop|restart|graceful|graceful-stop|configtest|status}

添加虚拟主机 /root/vhost.sh
phpinfo : http://yourIP/phpinfo.php
phpMyAdmin : http://yourIP/phpmyadmin/
探针 : http://yourIP/p.php
PureFtp用户管理：http://yourIP/ftp/

LNMP相关目录：
mysql :   /data/lnmp/mysql
php :     /data/lnmp/php
nginx :   /usr/lnmp/local/nginx
网站目录 :     /data/www
Nginx日志目录：/data/www

配置文件：
Nginx主配置文件： /data/lnmp/nginx/conf/nginx.conf
MySQL配置文件：/etc/my.cnf
PHP配置文件： /data/lnmp/php/etc/php.ini
PureFtpd配置文件： /data/lnmp/pureftpd/pure-ftpd.conf
PureFtpd MySQL配置文件： /data/lnmp/pureftpd/pureftpd-mysql.conf
Apache配置文件： /data/lnmp/apache/conf/httpd.conf