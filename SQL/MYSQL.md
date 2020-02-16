# MYSQL

```
官网下载对应版本：

mysql-workbench安装：

1，下载mysql-workbench。下载地址：http://www.mysql.com/downloads/workbench/ ; 注意：选择版本为：Oracle&Red Hat Linux6 ，随后下载此文件，下载后的文件名为：mysql-workbench-gpl-5.2.45-1el6.i686.rpm
2，在shell中进入下载文件目录。
3，安装mysql-workbench。在打开的shell中输入命令：yum install mysql-workbench-gpl-5.2.45-1el6.i686.rpm 随后就开始安装了，期间会有一些问yes or no的地方，一律y就可以了。

mysql安装：
https://www.if-not-true-then-false.com/2010/install-mysql-on-fedora-centos-red-hat-rhel/

https://blog.csdn.net/HaHa_Sir/article/details/80552663

修改roo密码：alter user 'root'@'localhost' identified by 'Root_123root'；

mysql数据库操作：
[taohy@thynb odoo]$ mysql -u root -p
mysql> show database;   //显示数据库
mysql> use 数据库； //打开数据库
mysql> show tables; //显示数据库中的表
mysql> describe 表名; //显示数据表结构

mysql> create database 库名 character set utf-8; //新建数据库 TestDB
mysql> create table students(id int,name varchar(20)); //新建表
mysql> drop 数据库名；//删除数据库名
mysql> drop 表名；
mysql> insert into students(id,name) values(1,'taohy'); //插入数据
mysql> exit; //退出数据库

连接远程数据库：
[taohy@thynb odoo]$ mysql -h localhost -u root -p Root_123root;


peewee连接mysql：
参考资料：http://docs.peewee-orm.com/en/latest/peewee/installation.html
http://www.cnblogs.com/noway-neway/p/5274814.html

遇到问题：MySQL driver not installed!
https://my.oschina.net/johnsken/blog/1840348

sudo dnf install Mysql-python


mysqldb连接：
https://www.cnblogs.com/luyaran/p/8940097.html


mysqlworkbrench使用：
http://www.cnblogs.com/daimage/archive/2012/02/25/2367534.html


"C:\Program Files\MySQL\MySQL Server 5.0\bin\mysql.exe" -u root -p123 lng100 -h 192.168.7.20
pause
```

