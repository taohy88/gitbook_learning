# CSS

参考资料 ：[MDN](https://developer.mozilla.org/zh-CN/docs/learn)

---

[TOC]

---



### 引用格式

<link href="styles/style.css" rel="stylesheet" type="text/css">



CSS规则集：{} ： ；

选择器： p

声明：color: red;

属性：color

属性值：red

p {color: red;}

多元素选择：不同的选择器用逗号分开。



###### 不同类型的选择器

元素选择器：p 选择<p>

ID选择器：#my-id 选择<p id="my-id"> 

唯一类选择器：.my-class 选择<p class="my-class">

属性选择器：img[src]  选择 `<img src="my.png">`  而不是img

伪类选择器：a:hover 仅在鼠标指针悬停在链接上时候选择<a>





### 根据元素在文档中的位置确定样式

后代组合器

例如 li em{ color：red; } 仅限嵌套在li元素内的em

兄弟组合器：例如 h1 + p{ font-size: 200%; } 出现在和h1平级的p 



### 块级黑子block和内联盒子inline box

display的属性设置成inline的时候，with height属性不会起作用



### CSS布局主要是基于盒模型，每个占据页面空间的块都有属性

padding 内边距

border 边框

margin 外边距



### 注释

/* */



### 控制继承

inherit 使子元素属性和父元素相同，实际就是开启继承

initial 设置属性值和浏览器默认样式相同

unset 属性重置为自然值，如果属性是自然继承就是inherit,否则就和initial一样



```
<style type="text/css">
a:link {color: #FF0000}     /* 未访问的链接 */
a:visited {color: #00FF00}  /* 已访问的链接 */
a:hover {color: #FF00FF}    /* 当有鼠标悬停在链接上 */
a:active {color: #0000FF}   /* 被选择的链接 */

#darkbannerwrap  自定义的css样式 login

CSS:
<style type="text/css">
a:link {color: #FF0000}     /* 未访问的链接 */
a:visited {color: #00FF00}  /* 已访问的链接 */
a:hover {color: #FF00FF}    /* 当有鼠标悬停在链接上 */
a:active {color: #0000FF}   /* 被选择的链接 */
#darkbannerwrap  自定义的css样式 login
```

