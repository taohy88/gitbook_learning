# Jquery

```
Jquery是一个js库
2.0版本以上，不支持ie浏览器，一般使用1.9版本即可
min.js是.js的压缩版本，去除了文件空白，不方便阅读和使用
一般开发环境用js版本 项目上线后可以使用min.js

Jquery
jquery 是一个js函数库 保存在文件scripts文件中 直接调用文件即可
jquery.min.js 放在第一个 ，文章用到$("")这样的符号
jquery 语法 $(this).hide(）隐藏当前元素；$(p).hide(）隐藏所有段落；$(.test).hide(）隐藏所有class=test的所有元素；$(#test).hide(）隐藏所有id=test的所有元素；

学习网站：
w3school：
http://www.w3school.com.cn/jquery/jquery_fade.asp

Jquery库特性：
HTML元素选取
HTML元素操作
CSS操作
HTML事件函数
JavaScript特效和动画
HTML DOM 遍历和修改
AJAX


Jquery包引用：
<head>

<script type="text/javascript" src="/js/jquery-1.3.2.js"></script>
</head>

函数入口：
防止文档在完全加载之前运行Jquery代码。

 $(document).ready(function(){

});

  $(function(){

});


1. Jquery选择器：
基础选择器：
this 当前的HTML元素 $(this).hide 
id选择器 $("#id")
类选择器 $(".className")
标签选择器 $("TagName")
交集选择器 $(selector1selector2)
并集选择器 $(selector1,selector2) 

层级选择器：
后代选择器：$(selecotor1 selector2)
子代选择器：$(selector1>selector2)

过滤选择器（odd even eq）

例子：
jquery 01.html

筛选选择器(children(selector)、find(selector)、next()、siblings(selector)、parent()、eq(index))
$(this).children(selector)获取当前元素的子代标签
$(this).find(selector)  //在当前元素的后代元素中寻找和selector对应的元素
$(this).next()   //获取当前元素的下一个元素
$(this).siblings(selector) //获取当前元素的兄弟元素
$(this).parent()  //获取当前元素的父级元素

$(this).eq(index))  //获取当前元素的索引位置

2. jquery事件：
事件函数，放到<head>部分事件处理
例如：
$("button").click(function(){
$("p").hide();
});
单独文件中的函数，放在head中引用。
<script type="text/javascript" src="my_jquery_functions.js"></script>

将函数绑定到文档的就绪事件（当文档完成加载时）： $(document).ready(function)
触发或将函数绑定到被选元素的点击事件：$(selector).click(function)
触发或将哈数绑定到被选元素的双击事件：$(selector).dbclick(function)
触发或将函数绑定到被选元素的获得焦点事件：$(selector).focus(function)
触发或者将函数绑定到被选元素的鼠标悬停事件：$(selector).mouseover(function)


3. jquery效果：
jquery显示和隐藏：hide() show()
$(selector).hide(speed,callback);
$(selector).hide(speed,callback);
speed规定隐藏、显示的速度，可以取slow fast或者毫秒
toglle()方法可以用来切换hide和show()方法
例如：
$("button").click(function(){
$("p").toggle();
});

jquery淡入淡出：
fadeIn():
淡入已隐藏的元素 
$(selector).fadeIn(speed,callback);
fadeOut():
淡出可见元素
$(selector).fadeOut(speed,callback);
fadeToggle():
切换淡入和淡出效果
$(selector).fadeToggle(speed,callback);
fadeTo():
渐变为给定的不透明度
$(selector).fadeTo(speed,opacity,callback);

jquery滑动：
slideDown():
向下滑动元素
$(slector).slideDown(speed,callback);
slideUp():
向上滑动元素
$(selector).slideUp(speed,callback);
slideToggle():
切换向下滑动和向上滑动方法
$(selector).slideToggle(speed,callback);

jquery动画：
animate()方法：自定义动画
$(selector).animate({params},speed,callback)
params定义形成动画的css属性

jquery停止动画或者效果：
stop() 滑动：
stop() 动画：
$(selector).stop(stopAll,goToEnd);

jquery Callback:
Callback函数在当前动画100%完成之后执行。
$("p").hide(1000,function(){
alert("This paragraph is now hidden!");
});

jquery多条执行：
$("p1").css("color","red")
.slideUp(2000)
.slideDown(2000);


4. jquery HTML
jquery中最重要的部分，就是操作DOM的能力。
DOM=document object model 文档对象模型

获得内容：text() html() val()
text() 设置或返回所选元素的文本内容
html() 设置或返回所选元素的内容
val() 设置或返回表单字段的值

获取属性值：attr()
attr() 方法用户获取对应属性的值
例如：$("selector").attr("href")

设置内容：text() html() val()
text() 设置或返回所选元素的文本内容
html() 设置或返回所选元素的HTML内容
val() 设置或返回表单字段的值

设置属性：attr()
attr() 设置/改变属性值
例如：
单个设置：
$("test").attr("href","http://baidu.com");
多个设置：
$("#test").attr(
"href":"http://baidu.com",
"title":"W3schooljquery Tutorial"
);

添加新元素/内容：
append():在被选元素的结尾插入内容
prepend():在被选元素的开头插入内容
after():在被选元素之后插入内容
before():在被选元素之前插入内容

删除元素/内容：
remove():删除被选元素（及其子元素）
empty():从被选元素中删除子元素

获取并设置css类：
addClass():向被选元素添加一个或多个类
removeClass():从被选元素删除一个或多个类
toggleClass():对被选元素进行添加/删除类的切换操作
css():设置或返回样式属性

css()方法：
设置或返回被选元素的一个或多个样式属性
例如：
返回元素样式属性：$("p").css("background-color");
设置1个元素样式属性:   $("p").css("background-color","yellow");
设置多个元素样式属性:   $("p").css("background-color":"yellow","font-size":"200%");













写入需要的功能：
$符号开始，本质就是一个函数
第一种用法：传入字符串css选择器，获取页面上的元素
例如 $("#id") $(selector)

第二种用法：传入DOM对象，把DOM对象转成jquery对象
例如 $(document) $(DOMObj)

第三种用法：传入一个function，入口函数
例如 $(function)


Jquery对象和DOM对象

  <script>
    $(document).ready(function(){
//        dom对象通过js方法获取到的元素 就是DOM对象
       var  son1=document.getElementById("son1");
          son1.style.backgroundColor="pink";
//        son1.css("backgroundColor","green");//错误  dom也不能调用jauary方法
     //jquary对象通过jQuery方法获取到的元素 就是jQuery对象
        var $lis=$("li");
        $lis.css("backgroundColor","green");
//        $lis.style.backgroundColor="pink";//错误  jquary不能调用dom方法    });
</script>













jquery 语法
$(this).hide(）隐藏当前元素；
$(p).hide(）隐藏所有段落；$(.test).hide(）隐藏所有class=test的所有元素；
$(#test).hide(）隐藏所有id=test的所有元素；
AJAX:
post是发送，get是获取
比如你要将记录保存到服务器用post
如果你要从数据库中读取记录用get
例子代码网页：http://www.cnblogs.com/acles/articles/2385648.html
http://blog.csdn.net/iouxyz/article/details/5691050

http://blog.csdn.net/smartsmile2012/article/details/17220413



freeCodeCamp:
最流行的javascript库jquery
1.learn how script tags and document ready work
<script>
  $(document).ready(
  function(){
  });
</script>

2.target html  elements wiht selectors using jquery
所有jquery方法都是$开始的，通常称为美元符号或者bling。
jquery通过选择器来选择一个元素，然后操作元素做出改变。
$("button").addClass("animated bounce");

3.target elemets by class using jquery
$(".well").addClass("animated shake");

4.target elements by id using jquery
$("#target3").addClass("animated fadeOut");

5.remove classes from an element with jquery
jquery的addClass()方法给元素添加class
jquery的removeClass()方法去掉元素上的class

6.change the css of an element using jquery
jquery改变HTML的css样式
$("#target1").css("color","red");

7.disable an element using jquery
jquery有一个.prop()的方法来调整元素的属性
$("button").prop("disabled",true);

8.change text indside an element using jquery
jquery的.html()方法可以添加html标签和文字到元素，而元素之前的内容都会被方法的内容所替换掉。
<em>标签重写和强调标题文本
$("#target4").html("<em>#target4</em>");

9.remove an element using jquery
jquery来移除页面上的HTML元素
$("#target4").remove();

10.use appendTo to move elements with jquery
尝试把元素从一个div里移到另外div里
jquery有一个appendTo()方法可以把选中的元素加到其他元素中。
$("#target2").appendTo("#right-well");

11.clone an element using jquery
jquery的clone()方法可以拷贝元素
2个jquery的方法合在一起使用，就叫做方法链function chaining
$("#target5").clone().appendTo("#left-well");

12.target the parent of an element using jquery
jquery有一个方法parent(),他允许你访问指定元素的父元素。
$("#target1").parent().css("background-color","red");

13.target the children of an element using jquery
html元素都有children(子元素)，每个子元素都从父元素那里继承了一些属性。
jquery有个方法叫children()，它允许你访问的指定元素的子元素；
$("#right-well").children().css("color","orange");

14.target a specific chlid of an element using jquery
jquery用css选择器来选取元素，target:nth-child(n) 
css选择器允许你按索引顺序（从1开始）选择目标元素的所有子元素。

15.target even numbered elements using jquery
获取class为target且索引为奇数的所有元素，并给他们添加class。
jquery里的索引是从0开始的，也就是说:odd选择2,4,6才是对应的target索引1,3,5
$(".target:even").addClass("animated shake");---class为target且索引偶数
$(".target:odd").addClass("animated shake");---class为target且索引奇数
```

