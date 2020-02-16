# SQL

资料:[SQL 查询语句总是先执行 SELECT？你们都错了](https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA==&mid=2651021645&idx=2&sn=ad06c2660863e33f1f3625162e239f08&chksm=bdbe991e8ac91008c184778354d3f4a997eaf1497b6a85e03902898c97853e753289df8ce201&mpshare=1&scene=1&srcid=&sharer_sharetime=1572180615070&sharer_shareid=8702c119877e368127940fd8375a7fb0#rd)

```
SQL
数据操作语言DML
select
关键词distinct返回唯一不同值 select distinct 列名 from 表名；
where子句 select * from 表 where city='beijing' 单引号围绕文本值，数值不需要加；
like搜索某种模式 %用于缺少的字母 搜索以N开头 like 'N%';以g结尾 like '%g';不包含lon not like '%lon%';
通配符 _ 表示1个字符 例如 包含T开头Y结尾的字符 select * from 表 where 列名 like 'T_Y';
通配符 [anychar] 字符列任何一个单一字符 例如 包含ABC任何一个开头的字符 like '[ABC]%';
通配符 [!anychar] 不含字符列任何一个单一字符 例如 不含ABC任何一个开头的字符 like '[!ABC]%';
top返回规定的记录数 50%的记录 select top 50 percent * from 表名
update
修改数据 update 表名 set 列名=新数值 where 列名=某值
delete
删除行   delete from 表名 where 列名=数值
 
insert into
插入指定行的内容 insert into 表名（name , year) values ('taohy','2013')
数据定义语言DDL
create database
alter database
create table
alter table
drop table
create index 创建索引
drop index 删除索引

表：table 行称为记录record 列为字段field

CSDN学院：
https://edu.csdn.net/course/play/4395

SQL
数据操作语言DML
select
关键词distinct返回唯一不同值 select distinct 列名 from 表名；
where子句 select * from 表 where city='beijing' 单引号围绕文本值，数值不需要加；
like搜索某种模式 %用于缺少的字母 搜索以N开头 like 'N%';以g结尾 like '%g';不包含lon not like '%lon%';
通配符 _ 表示1个字符 例如 包含T开头Y结尾的字符 select * from 表 where 列名 like 'T_Y';
通配符 [anychar] 字符列任何一个单一字符 例如 包含ABC任何一个开头的字符 like '[ABC]%';
通配符 [!anychar] 不含字符列任何一个单一字符 例如 不含ABC任何一个开头的字符 like '[!ABC]%';
 
top返回规定的记录数 50%的记录 select top 50 percent * from 表名
 
update
修改数据 update 表名 set 列名=新数值 where 列名=某值
 
delete
删除行   delete from 表名 where 列名=数值
 
insert into
插入指定行的内容 insert into 表名（name , year) values ('taohy','2013')
 
数据定义语言DDL
create database
alter database
create table
alter table
drop table
create index 创建索引
drop index 删除索引



```

