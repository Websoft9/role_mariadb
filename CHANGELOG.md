# CHANGELOG

## To do
1. 双机
2. mysql_secure_installation
3. phpMyAdmin on Docker 安全连接问题
4. 创建普通用户的默认权限问题（针对用户同名库）
5. 弃用my.cnf配置文件的覆盖安装，把分组统一为[mysqld],[client]

1. 主从安装

## Logs

### Bug Fixes

* 2020-03-05  修改数据库连接方式login_host报错，修正为：login_unix_socket: /var/lib/mysql/mysql.sock

* 2020-03-06  修改数据库连接方式login_host报错，兼容修正为：login_unix_socket: /data/mysql/mysql.sock

* 2020-03-06  修正my.cnf的正确路径
### Features

* 2020-03-04  增加开启远程连接的可选项
* 2020-11-04  增加mariadb的引擎参数
