# C#

```
C#
.net 开发
三个基本层：数据访问和存储，业务逻辑层，表示层。
三层结构优点：可扩展性，可伸缩性，灵活性。
web应用的时候，MVC（模型-视图-控制）
IIS发布
iis服务-网站-默认网站，右击添加应用程序-对应的路径 

外机浏览的时候 直接对应ip/网站名字 OK

C#:
字符串类：
字符串比较  int i=string.Compare(s1,s2);//i=0
删除所有空格 string s="A BC" s.trim();//ABC
大小写转换 string s="AaBbCc" string s1=s.ToLower();//转换为小写 string s2=s.ToUpper();//转换为大写
typeof运算符：
console.WriteLine(typeof(int));//输出System.Int32
font类 this.label1.Font = new Font("宋体", label1.Font.Size, label1.Font.Style | FontStyle.Bold);
datatime类 String s=DateTime.Now.ToString(); int y=DateTime.Now.Year;
在C#中，要将一个字符串或浮点数转换为整数，基本上有三种方法：
   （1）使用强制类型转换：(int)浮点数
   （2）使用Convert.ToInt32(string)
   （3）使用int.Parse(string)或int.TryParse(string,out int)
ToString格式：http://www.cnblogs.com/pyt5208/archive/2007/11/04/948724.html

              2.5 tostring("f2") 2.50

ASP.NET内建对象 C#教程试用版 P238
Request对象：P236
用途1：获取另一个网页传递的数据
       从一个网页链接到另一个网页时，传递一些数据到另一个网页。
       两个Web网页之间通过表单From传递，具体方法有两个:Post和Get。     
用途2：web服务器通过request对象获取客户端浏览器的信息
用途3：web服务器通过request对象显示web服务器的信息
用途4：用Request对象获取Cookie信息
       用cookie对象记录访问的次数
Response对象 用的比较少
用途1：用response对象发送信息在浏览器中显示
用途2：用response对象重定向浏览器
Application对象
用途：存储记录在线人数或访问网站总人数的变量
方法：Lock 和Unlock P247
Session对象
webconfig配置中 <sessionState mode="InProc" cookieless="false" timeout="1440" />
               设置session的保存时间 timeout="1440" 1440分钟=24小时
属性：SessionID 返回用户的会话标识
      TimeOut 限定超时时长 单位分钟
方法：Abandon 删除所有存储在session中的对象并释放这些源 不声明，超过时间自动释放
Server对象
提供对服务器上的资源进行访问的方法和属性
属性：MachineName 获取web服务器的计算机名称 string s=Server.MachineName;
      ScriptTimeOut 程序运行的最长时间 单位秒
方法：MapPath 宿主目录和实际路径的转换string s =Server.MapPath(\Test\f1.aspx);



asmx文件：WEB服务文件
master：主站 拿数据 一个
slave： 从站 方数据 多个(<247)
MODBUS协议：
读取多个寄存器（最多125个7D） 02SLAVEID 03功能码 00 00起始地址 00 01读取个数 CRC1 CRC2 共8个byte
写入单个寄存器 02SLAVEID 06功能码 00 00寄存器地址 00 01寄存器数据 CRC1 CRC2
写入多个寄存器 02SLAVEID 10功能码 00 00寄存器地址 00 01写入个数 02字节数 00 01寄存器数据 CRC1 CRC2


CSDN学院：

https://edu.csdn.net/course/play/5344/97487
第二章：学生信息管理系统


C#自学网：
http://www.51zxw.net/list.aspx?cid=548




.net 开发
三个基本层：数据访问和存储，业务逻辑层，表示层。
三层结构优点：可扩展性，可伸缩性，灵活性。
web应用的时候，MVC（模型-视图-控制）

IIS发布
iis服务-网站-默认网站，右击添加应用程序-对应的路径  
外机浏览的时候 直接对应ip/网站名字 OK

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





KYL
web框架 使用的是 nhibernate + jquery


JS
javascript

Jquery
jquery 是一个js函数库 保存在文件scripts文件中 直接调用文件即可
jquery.min.js 放在第一个 ，文章用到$("")这样的符号
jquery 语法 $(this).hide(）隐藏当前元素；$(p).hide(）隐藏所有段落；$(.test).hide(）隐藏所有class=test的所有元素；$(#test).hide(）隐藏所有id=test的所有元素；

AJAX:
post是发送，get是获取
比如你要将记录保存到服务器用post
如果你要从数据库中读取记录用get

例子代码网页：http://www.cnblogs.com/acles/articles/2385648.html
http://blog.csdn.net/iouxyz/article/details/5691050
http://blog.csdn.net/smartsmile2012/article/details/17220413

vs调试：
加断点 F10下一步 F5整个结束
js调试 debugger；
调整格式 ctrl+k+d
显示函数 ctrl+j

coolite 0.8版本
tree
grid
button
布局



ashx一般处理程序
asmx web服务webservice程序

js看 1,3,4,5
.net 第三个不用看
html/css


        aa    "\"[{\\\"key\\\":\\\"1\\\",\\\"info\\\":{\\\"name\\\":\\\"222\\\",\\\"age\\\":\\\"333\\\",\\\"sex\\\":\\\"444\\\"}},{\\\"key\\\":\\\"2\\\",\\\"info\\\":{\\\"name\\\":\\\"999\\\",\\\"age\\\":\\\"000\\\",\\\"sex\\\":\\\"111\\\"}}]\""    String


C#:
字符串类：
字符串比较  int i=string.Compare(s1,s2);//i=0
删除所有空格 string s="A BC" s.trim();//ABC
大小写转换 string s="AaBbCc" string s1=s.ToLower();//转换为小写 string s2=s.ToUpper();//转换为大写
typeof运算符：
console.WriteLine(typeof(int));//输出System.Int32
font类 this.label1.Font = new Font("宋体", label1.Font.Size, label1.Font.Style | FontStyle.Bold);
datatime类 String s=DateTime.Now.ToString(); int y=DateTime.Now.Year;
在C#中，要将一个字符串或浮点数转换为整数，基本上有三种方法：
 
   （1）使用强制类型转换：(int)浮点数
 
   （2）使用Convert.ToInt32(string)
 
   （3）使用int.Parse(string)或int.TryParse(string,out int)
ToString格式：http://www.cnblogs.com/pyt5208/archive/2007/11/04/948724.html
              2.5 tostring("f2") 2.50
 
```

