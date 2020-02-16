# PostgreSQL

参考资料：[frank](https://github.com/frank-lam/fullstack-tutorial/blob/master/notes/PostgreSQL.md)

[TOC]

### 1.什么是PostgreSql？

自由的对象-关系数据库服务器。
面向关系的数据库：Oracle、Mysql、SqlServer、PostgreSql
Nosql：MongoDB、Redis



### 2.初来乍到数据库？

```
进入客户端：
sudo -u postgres psql
提示符变成： postgres=#  
\q 退出
\l  列出所有数据库
\du 列出所有用户
\c  [database_name] 连接其他数据库
\d 列出当前数据库的表
\d [table_name] 列出指定表的结构
\conninfo 列出当前数据库和连接的信息

新建数据库:TaohyDB指定给taohy
sudo -u postgres createdb -O taohy TaohyDB;
psql控制台删除用户：
先删除数据库：
postgres=# drop database TaohyDB
再删除用户：
postgres-# drop user taohy

重启数据库
sudo service postgresql restart
```



### 3.操作数据表？

```
#新建表
create table posts(title varchar(255),content text);
#删除表
drop table posts;
```



### 4.字段类型？

```
数值型：integer(int)  real  serial
文字型：char varchar text
布尔型：boolean
日期型：date time timestamp
特色类型：Array inet网络地址 Json型 XML型
```



### 5.添加表约束

```
表字段的约束条件
primary key：主键 不能空，且不能重复
not null：不能为空
unique：在所有数据中值必须唯一
check：字段设置条件
default：字段默认值

create table posts (
id serial primary key,
title varchar(255) not null,
content text check(length(content) > 8),
is_draft boolean default TRUE,
is_del boolean default FALSE,
created_date timestamp default 'now'
);
```





### 6.Insert语句

```
insert into [tablename] (field, ...) values (value, ...)

# 插入数据
INSERT INTO user_tbl(name, signup_date) VALUES('张三', '2013-12-22');
```



### 7.Select语句

`select * from posts;`



### 8.Where语句

`select * from posts where id<5;`



### 9.数据抽出选项？

```
order by：排序
limit ：给出限制计数，则返回的行数不会超过这个数；limit all 和 省略 limit 相同，不限制计数。
offset：返回行之前跳过这么多行，offset 0 和 offset相同。同时出现limit和offset，则计算返回的Limit行之前跳过offset行。
```



### 10.统计抽出数据？

```
distinct 
sum
max/min
group by /having
```



### 11.方便的函数？

```
length
concat
alias
substring
random
```



### 12.更新和删除？

```
#更新表数据
update posts set content='titletitle1' where id =5;

#删除表数据
delete from posts where id=5;
```



### 13.变更表结构？

```
alter table [tablename] ...
#修改表字段 新增一个字段
alter table posts add fullname varchar(255);

create index ...
drop index ...
```



### 14.操作多个表？

```
#2个表 users和twitters
select users.player,twitters.content from users,twitters where users.id=twitters.id;
select u.player,t.content from users as u,twitters as t where u.id=t.id;
```



### 15.使用视图

```
视图是从一个或多个表到处的对象。
视图和表不同，视图时一个虚表，即视图对应的数据不进行实际存储，数据库只存储视图的定义，在对视图的数据进行操作时，系统根据视图的定义去操作与视图相关联的基本表。
# 创建一个视图 create view ...
create view curry_twitters as select u.player,t.content from users as u,twitters as t where u.id=t.id;
# 查询一个视图 select * from viewname
select * from curry_twitters;
# 删除一个视图 drop view ...
drop view curry_twitters;
```



### 16.使用 事务

```
作为单个逻辑工作单元执行的一系列操作，要么完全执行，要么完全不执行。
事物处理可以确保非事务性单元内的所有操作都成功完成，否则不会永久更新面向数据的资源。
begin
commit
rollback

> select * from users;
> begin;
> update users set score = 50 where player = '库里';
> update users set score = 60 where player = '哈登';
> commit;
> select * from users;
> begin;
> update users set score = 0 where player = '库里';
> update users set score = 0 where player = '哈登';
> rollback;
> select * from users;
```



### 17.psql shell使用

```
shell :
新建超级用户
sudo -u postgres createuser --superuser taohy;

psql控制台设置密码退出：
sudo -u postgres psql
postgres=# \password taohy;
输入新的密码：taohongyu
再次输入：taohongyu
postgres=# \q
修改postgres密码：
[taohy@thynb ~]$ sudo -u postgres psql
postgres=# ALTER USER postgres WITH PASSWORD 'postgres';

查看pg的版本：
psql -V
```



### 18.可视化工具

pgWeb

```
linux客户端：
参考资料：https://github.com/sosedoff/pgweb
下载 https://github.com/sosedoff/pgweb/releases
解压
CMD执行  ./pgweb_linux_amd64 --host localhost --user postgres 
```

pgAdmin

