# 程序员自我修养

```
程序员的自我修养：
https://leohxj.gitbooks.io/a-programmer-prepares/programmer-basic/character-encoding.html

程序员基础知识

	* 
字符编码


计算机内部只存储和处理字节，字符只是人类理解的概念
人们需要在字节和字符之间建立对应关系，这就是字符编码(Character encoding).
一种字符编码可以支持的所有字符成为一个字符集（Charset）.例如ASCII字符集 中国的中文编码GB2312
UTF通用编码转换格式（Unicode Translation Format）,常用UTF-8以8位单字节为单位
语义化版本：
版本格式：主版本号.次版本号.修订号，版本号递增规则：

	* 
主版本号：当你做了不兼容的API修改
	* 
次版本号：当你做了向下兼容的功能性新增
	* 
修订号：当你做了向下兼容的问题修正
考虑使用这样的版本号：XYZ（主版本号.次版本号.修订号），1.0.0的版本号用于界定公共API的形成。




	* 
命名规范


个人认为包含了目录、文件、变量
目录：
 win和os下文件名不区分大小写，linux是区分的。所以命名建议全部小写为主，个人习惯连字符使用_，比如my-project-name；
子目录一般按照作用，使用常用单词表示，有复数的情况，使用复数命名法，比如：scripts,styles,images,data-modules;
文件：
文件的命名推荐_
变量：
命名有2种方式：
下划线命名：my_variable
驼峰式命名：myVariable
JavaScript:
驼峰式命名 myVariable
CSS:
中划线进行连接，CSS语法本身就使用连字号作为连接。例如：font-family,text-algin


	* 
书写文档


git+github+wiki


	* 
目录结构


src:目录专注于开发，存放的都是源文件，不需要压缩合并。主要分为：

	* 
css(styles)：样式文件
	* 
js(scripts)：脚本文件
	* 
img(images)：图片素材
	* 
font(fonts)：存放字体
	* 
其他：按照分类不同划分目录
文件名上面，简写都是单数，全称都是复数形式。


dist:
此目录为编译生成目录，用于部署环境，目录结构与src保持一致。
test:
此目录为测试目录，存放和项目测试相关的文件。
doc:
如果存在文档说明，放置在此目录下。


	* 
正则表达式


对于程序员而言，它算一个基础知识。很多场合都需要使用它，这个技术又是一个比较通用的东西。



数据结构与算法

	* 
堆和栈
	* 
浮点数类型
	* 
XML和JSON
	* 
算法学习之路


算法参考：http://www.blogjava.net/todayx-org/archive/2012/01/08/368091.html
快速排序：从数列中挑出一个元素，称为"基准"，重新排序数列，所有元素比基准小的摆放在基准前面，所有元素比基准大的摆在后面。在这个分区退出之后，该基准就处于数列的中间位置，称为分区操作。
归并排序：
堆排序：
选择排序：
冒泡排序：
插入排序：
希尔排序：



代码架构

	* 
设计模式
	* 
面向对象编程：继承 多态 封装
	* 
面向接口编程




网络知识
HTTP状态码


懂点设计


获取知识
MOOC:大规模开放在线课程(Massive open onine course)
国内：网易公开课 MOOC学院


提升效率
学会阅读：记录笔记
学会写作：markdown

音乐对效率的影响
阿尔法脑波
巴洛克音乐


常用软件

	* 
SublimeText 3: 最方便的编辑器，插件也多。
	* 
Beyond Compare: 对比文件工具。





```



[20+ Youtube Channels](https://www.youtube.com/watch?v=BZRLKDlSaAI)

[Top 10 Learning methods for self](https://www.youtube.com/watch?v=raoOoWU7DI0&list=PLillGF-RfqbZ_hV3gQav81bUCpCANWXOu&index=3)