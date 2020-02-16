# HTML

参考资料: [MDN](https://developer.mozilla.org/zh-CN/docs/learn)



###### 概述

开始标签+结束标签+内容=元素元素可以有属性，class属性可为元素提供一个标识名称



###### 空元素

```
<img src="images/e1.png" alt="测试图片">，没有结束标签，元素也没有内容。这是因为图像元素不需要通过内容来产生效果。
```



###### 标记文本

```
列表List，元素用<li>包围。无序列表<ul> 有序列表<ol>
链接<a href="http:baidu.com" title="百度" >百度</a>
```



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

```
无序列表 <ul><li>豆浆</li></ul>

有序列表 <ol><li>过马路</li></ol>描述列表 <dl><dt>旁白</dt><dd>戏剧中，为了渲染，加入旁白<dd></dl>

嵌套列表 <ol><li>宫保鸡丁</li><ul><li>炸花生米</li></ul</ol>
```



```
 <!--强调 em 斜体字-->  <p>I am <em>glad</em> you weren't <em>late</em>.</p> <!--非常重要 strong 粗体字-->  <p>This liquid is <strong>highly toxic</strong>.</p>

HTML文件中的<head>标签里，将会找到一行代码<meta name="viewreport" content="width=device-width">:这行代码会强制地让手机浏览器采用他们真实可视窗口的宽度来加载网页。
```



###### HTML表格

```
<tr>

<td>

合并单元格属性 colspan rowspan

定义整列数据的样式 <col>

<colgroup>元素

<caption>表格标题

<thread>表头

<tbody>页眉

<tfoot>页脚
```



###### HTML表单

所有HTML表单都以一个<form>元素开始，两个重要的属性action和method。





```

头文件：<head></head>   一般包括 CSS JS都定义在头文件中
  包括：标题：<title></title> 有且只有一个
        元信息：<meta> 页面信息的名称、关键字、作者等
        基底网址标记：<base></base>
主体：<body></body>
表格：<table></table>

      <tr></tr> 行 <td></td>列 <th></th>表头

1.简介：
<!DOCTYPE html> //html5声明
<html>
  <head>
     <meta charset="UTF-8">  //编码
     <title>页面标题</title>
  </head>
<body>
     <h1>这是一个标题</h1>
     <p>这是一个段落</p>
</body>
</html>

2.基础实例
标题：h1-h6
          <hr/>水平线
段落：<p>   换行标签</br>

链接：<a>  
例如：<a href="http://baidu.com" target="_blank">链接</a>
target属性 在新窗口中打开链接

图像：<img>
例如：<img src="/images/logo.png" width="100" height="50" alt="Big Boat"></img>


表格：<table>
border：边框属性
<th>：表格标题
cellpadding：单元格边距
cellspacing：单元格间距
例如：
<table border="1" cellpadding="5">
     <tr>
          <td>cell1_1</td>
          <td>cell1_2</td>
     </tr>
</table>

列表：
有序列表和无序列表
无序列表：
<ul>
     <li>coffee</li>
     <li>milk</li>
</ul>

有序列表：
<ol start="10">
     <li>coffee</li>
     <li>milk</li>
</ol>

自定义列表：
<dl>
     <dt>coffee</dt>
      <dd>_black hot drink</dd>
     <dt>milk</dt>
     <dd>_white hot drink</dd>   //定义自定列表项的描述
</dl>


注释：<!--  注释  -->

3.html属性
参考手册 http://www.runoob.com/tags/ref-standardattributes.html
class：类名
id：定义元素的唯一id
style：规定元素的行内样式
title：描述元素的额外信息

4.文本格式化
http://www.runoob.com/html/html-formatting.html

5.html头部
<meta>标签：
一般放在head标签内
通常用于指定网页的描述、关键字、文件最后修改时间、作着、每30s刷新
<base>:
定义页面链接标签的默认链接地址

6.CSS
http://www.runoob.com/css/css-tutorial.html
内联样式：
html元素中，使用style属性
<p syle="font-family:arial;color:red;font-size:20px;">一个段落。</p>

内部样式表：
<head>区域中 使用<style>包含css
<style type="text/css">
body {background-color:yellow;}
</style>

外部引用：
使用外部的CSS文件
<link rel="stylesheet" type="text/css" href="mystyle.css" />


7..布局
区块布局：
<div></div>
<span></span>
表格布局：
<table></table>
colspan 合并2行

8.表单
http://www.runoob.com/html/html-forms.html
<form></form>
<input>：输入元素
文本域：type="text" 
密码字段：type="password"
单选按钮：type="radio"
复选框：type="checkbox"
提交按钮：type="submit"

9.html框架
<iframe src="url"></iframe>
width：宽度
height：高度
frameborder：边框  为0设置为不显示

10.脚本
具体查看js教程
<script>
document.write("Hello World")
</script>

<noscript></noscript> 无法适用脚本的替代内容

11.字符实体
空格：&nbsp
http://www.runoob.com/html/html-entities.html
```





HTML5:

```
HTML5：1.简介<!DOCTYPE html><meta charset="UTF-8">2.支持HTML5 标签和 DOM：这是前端最核心技术，为之后学习各种开发框架，打下坚实基础。 CSS3：学习通过 css 开发网页和各种可视 UI 组件。 SASS：利用 sass 语言，开发复杂的页面 css Node.js：掌握Node.js 核心 API ，具备后端开发能力。 Express 5.x 框架：掌握 Express 框架，从而具备快速开发后端程序的能力。 socket.io 库：让前后端通过 websocket协议通信，是web 开发游戏、聊天等程序必备技术。 Mongoose 框架：可以让程序具备文档数据储存能力 Git 命令与 github：可以对项目进行版本管理，从而能团队开发项目。 Gulp 构建工具实战：通过 gulp 工具，灵活对项目进行构建。 Webpack：可以用和 Node.js 后端模块化方式，开发前端程序，从而能开发大型系统。 Jasmine & Karma：可以利用 Jasmine & Karma 轻松实现，多种浏览器同时进行单元测试，而不必切换界面。 前端相关框架：JQuery ／ Bootstrap ／ Vue.js ／React ／ Angular通过框架帮我我们快速开发程序HTML5 技术是标准的，我们用到的浏览器都支持他，所以在可预见的未来不会被淘汰。而 Node.js 是开源的，不受一个公司的控制，却受到各个大咖公司的赞助和支持，包括微软、因特尔、IBM … 具体参看 https://nodejs.org/en/foundation/members/  所以 Node.js 在可预见的未来，也不会被淘汰freecodecamp：HTML/CSS1.import a google font<link href="https://fonts.gdgdocs.org/css?family=Lobster" rel="stylesheet" type="text/css">css font-family:Lobster; 引用2.Specify how fonts should degrade默认字体所有浏览器都适用的：Monospace  Serif   Sans-Serif当某种字体不可用的时候，降级到另一种字体p{font-family: Helvetica, Sans-Serif;}3. add rounded corners with a border radiusborder-radius(边框半径) 百分比和直接像素值都可以应用在图片上4.make dead links using the hash symbolhref="http://" 换成 href="#" 就是一个固定链接5.add alt text to an image for accessibilityalt属性也称为alt text，当图片无法加载的时候显示替代文本<image src="/images/a.jpg" alt="your alt text">6.create an unordered list无序列表 <ul><li>water</li><li>cheese</li><li>milk</li></ul>7.create an ordered list有序列表<ol><li>catching mouses</li><li>geting out</li><li>finding people</li></ol>8.add placeholder text to a text field占位符 预定义文本<input type="text" placeholder="this is placeholder text"></input>9.create a form element使用HTML来构建可以跟服务器交互的web表单form，通过form添加一个action属性来达到目的action属性值指定了表单提交服务器的地址。<form action="/submit-cat-photo"></form>10.add a submit button to a form点击按钮，表单中的数据会被发送到action属性指定的地址<button type="submit">this button submits the form</button>11.use html5 to require a field设计form的时候，只有当用户填写了选项后，用户才能提交成功<input type="text" placeholder="cat photo URL" required>12.radio button 单选框<label>   <input type="radio" name="indoor-outdoor">outdooor</input>  </label>13.checkbox button 多选框 <label>  <input type="checkbox" name="personality">Loving</input>  </label> <label>  <input type="checkbox" name="personality">Sad</input>  </label>14.check radio buttons and checkboxes by default设置单选框和复选框的默认选中，input中加入checked即可<label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
<label><input type="checkbox" name="personality" checked> Loving</label>

15.style
style元素内部，定义class类选择器添加. 为前缀；定义ID选择器添加# 为前缀。

16.adjusting the padding of an Elemetn
HTML所有元素本质上都是一个小的矩形，代表着一块区域。
影响HTML元素布局的重要性：padding 内边距 ；margin 外边距；border 边框。

17.using clockwise notation to specify the padding of an element
padding-top;padding-right;padding-bottom;padding-left ;
padding:10px 20px 10px 20px; 上右 下左 顺时针方向

18.override styles in subsequent css
class="class1 class2" class2优先权

19.override class declarations by styling ID attributes
id的class属性具有更高的优先级
<h1 id="orange-text" class="pink-text blue-text">Hello World!</h1>

20.override class declarations wiht inline styles
行内样式更高优先级
<h1 id="orange-text" class="pink-text blue-text" style="color:white">Hello World!</h1>

21.override all other sytles by using important
需要确保某元素具有指定css时，使用 !important
.pink-text {
    color: pink !important;
  }



头文件：<head></head>   一般包括 CSS JS都定义在头文件中
  包括：标题：<title></title> 有且只有一个
        元信息：<meta> 页面信息的名称、关键字、作者等
        基底网址标记：<base></base>
主体：<body></body>
表格：<table></table>
      <tr></tr> 行 <td></td>列 <th></th>表头
```

