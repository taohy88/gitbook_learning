# HTML

<!--TOC-->

###### 概述

开始标签+结束标签+内容=元素元素可以有属性，class属性可为元素提供一个标识名称



###### 空元素

<img src="images/e1.png" alt="测试图片">，没有结束标签，元素也没有内容。这是因为图像元素不需要通过内容来产生效果。



###### 标记文本

`列表List，元素用<li>包围。无序列表<ul> 有序列表<ol>`
`链接<a href="http:baidu.com" title="百度" >百度</a>`



块级元素:以块的形式展示，出现在下一行

内联元素：出现在块级元素中， 不是一整个段落或者一组内容。不会导致换行。



布尔属性：有时候你会看到没有值的属性，他是合法的。



###### HTML特殊字符

`< 等价字符引用 &lt;`

``>等价字符引用 &gt;`

`" 等价字符引用 &quot;` 

`'等价字符引用 &apos;`

`& 等价字符引用&amp;`



###### 列表 Lists

无序列表 <ul><li>豆浆</li></ul>

有序列表 <ol><li>过马路</li></ol>描述列表 <dl><dt>旁白</dt><dd>戏剧中，为了渲染，加入旁白<dd></dl>

嵌套列表 <ol><li>宫保鸡丁</li><ul><li>炸花生米</li></ul</ol>



 <!--强调 em 斜体字-->  <p>I am <em>glad</em> you weren't <em>late</em>.</p> <!--非常重要 strong 粗体字-->  <p>This liquid is <strong>highly toxic</strong>.</p>

HTML文件中的<head>标签里，将会找到一行代码<meta name="viewreport" content="width=device-width">:这行代码会强制地让手机浏览器采用他们真实可视窗口的宽度来加载网页。



###### HTML表格

<tr>

<td>

合并单元格属性 colspan rowspan

定义整列数据的样式 <col>

<colgroup>元素

<caption>表格标题

<thread>表头

<tbody>页眉

<tfoot>页脚



###### HTML表单

所有HTML表单都以一个<form>元素开始，两个重要的属性action和method。



###### 参考资料 

###### [MDN](https://developer.mozilla.org/zh-CN/docs/learn)