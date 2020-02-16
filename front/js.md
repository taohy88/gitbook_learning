# JavaScript

DOM

JSON

Fetch API（Request/Response/Ajax)

Modern JS(ES6)



规范：web服务器对大小写敏感，文件夹和文件名使用小写。文件名如果要分离单词，最好使用横线，而不用下划线。网站结构：index.html：通常包括主页内容，第一次进入网页的地址。images：保存图片scripts：保存jsstyles：样式css



```
<script>部分没必要非要放在文档头部；实际上，把它放在文档给的尾部，在</body>标签之前是一个更好的选择，这样可以确保加载脚本之前浏览器已经解析了HTML内容。
初始化变量：建议尽可能多使用let，而不是var
变量命名规则：小写驼峰命名法 myName

<script>部分没必要非要放在文档头部；实际上，把它放在文档给的尾部，在</body>标签之前是一个更好的选择，这样可以确保加载脚本之前浏览器已经解析了HTML内容。
初始化变量：建议尽可能多使用let，而不是var
变量命名规则：小写驼峰命名法 myName
```

```
字符型转换为整型 parseInt(value,类型) 类型可以是2,8,10,16

整型转换为字符型 a.toString(类型)

AJAX:
post是发送，get是获取
比如你要将记录保存到服务器用post
如果你要从数据库中读取记录用get

手册：
https://developer.mozilla.org/zh-CN/docs/Web

CSDN学院视频：
http://edu.csdn.net/course/play/3091/51864

lesson1：
.JS特效--鼠标提示框
属性 div的dislay none和block
方法 mouseover mouseout
操作方法 document.getElementById('div1').display='none'
函数：script里面
function 函数名()
{
//代码        
}
重用：document.getElementById('div1')直接赋予一个变量
          var oDiv=document.getElementById('div1');

lesson2：
 css控制

 <link id="link1" rel="stylesheet" type="text/css" href="css1.css" />
  if语句
  =赋值
  ==判断是否相等
   classname

lesson3：
函数传参
操作属性方法：第一种方法：.属性   第二种方法：['value']
变量和字符串的区别：变量不固定 字符串是固定的

lesson4：
style  1.从style加样式--加在行间样式  2.从style取样式-- 行间
style和className：style优先级高  一般修改一种
提取事件：js设置onclick事件 oBtn.onclick=函数名；
事件：1.函数名 然后加到对应按钮   2.匿名函数 直接事件后面跟上
js代码放在body和head：head里面执行的时候，还未找到对应的控件
window.onload：页面加载完毕后执行
window.onload=function () {


 oBtn.onclick = function () {

            alert('点击了按钮')

        };
};
行为 样式 结构 三者分离
获取一组元素：getElementsByTagName 结果数组
循环 for while 初始化 条件 自增 语句
true/false：布尔值



lesson5：
选项卡
this：当前发生事件的元素
innerHTML：设置html元素
字符串相加：alert('a'+12+5+'cd') 输出 a125cd
数组：var a=[1,2,3,4]; a.length a[0]
为html加index

lesson6:
JS组成：
     ECMAScript翻译--核心解释器 --几乎没有兼容性问题
     DOM：documnet object model  赋予操作HTML的能力  文件documnet
                  有一些操作不兼容
     BOM：browser object model 赋予操作浏览器的能力   窗口window
                   完全不兼容
变量类型：typeof  有：number string bool object 
变量类型转换：parseInt 转成整型
                     //NaN   not a number 非数字
                    parseFloat 转成浮点型
强制类型转换--显示类型转换
隐式类型转换--自动转换
变量作用域：局部变量 全局变量 
闭包：子函数可以使用父函数的变量
命名规范：可读性；变量取名：类型前缀+首字母大写  oDivUserLogin 
     i interger； o object；a array；b bool；f float；
     fn function；re regexp 正则表达式；v variant变体变量
运算符：算术+ - * / %  其中%取模 实例隔行变色
               赋值：=，-=，++：i=i+1; i+=1;
               关系：> < == !=  <= >= ===
               逻辑：&& || ！ 与或非
流程控制：判断 if switch ?:
               ?: 三目运算符 条件？语句1 : 语句2
                  循环：while for 数组循环 for 0-len ；json for ( in )
                  跳出：break continue
                  真假：
JSON：{a:12,b:5,c:'abc'}  json['a'] 循环 for(var i in json)

lesson8:
函数返回值：return 没有return等
函数传参：
          arguments 可变参数 
          css(oDiv,'width') 获取样式
          css(oDiv,'width','200px') 设置样式
获取非行间样式：style操作行间样式
           IE: currentStyle获取费非行间样式
           chrome firefox: getComputedStyle(oDiv, false).width);
            css样式：复合样式、单一样式
数组高级用法：
     length 既可以获取又可以设置 例如快速清零
     添加：
          push 末尾开始添加
          unshift 头部添加
     删除：
          pop 末尾开始删除
          shift 头部删除
     插入：
          splice(开始 长度) 删除元素
          splice(开始 长度 'a’'b'）先删除再插入
     连接：
          concat：a.concat(b)
          join：a.join('a') 连接符号
                    var arr=[1,2,3] arr.join('-') 输出 1-2-3-4
     排序：
          sort：arr.sort(); 数字排序的依据是首字母
                    arr.sort(function(n1,n2){
                             //语句
                                   });

lesson9:
定时器：
          setInterval(show,1000);每隔1s调用show函数，一直执行
          setTimeOut(show,1000);执行一次
          停止定时器：
          clearInterval(定时器名);
          clearTimeOut(定时器名);      
          例子：数码时钟--每隔一秒 时间改变 

时间日期：
var oDate=new Date();
getFullYear() 获取年
getMonth() 获取月 //获取月份少了1
getDate() 获取日
getDay() 获取星期// 0 周日 1 周一----6 周六
getHours() 获取小时数据
getMinutes() 获取分钟数据
getSeconds() 获取秒

字符串  var sting1=‘1234’; string1[0] 获取1 这种方法不兼容低版本
               charAt(i) 兼容所有版本  time.charAt(i)


延时提示框：qq头像资料框

lesson10:
无缝滚动：div动态 设置 position:absolute;left:100px;
                    this.offsetLeft获取div最终的位置的left
                    this.offsetTop width height
                    定时器调用，是图片运动

lesson11：
DOM：标签CSS 元素JS 节点DOM-document
兼容性  IE 10%  Chrome 60%  Firebox 99%
元素属性操作：
     子节点 childNodes ---包括元素和文本
                children--只包括元素
                firstChild---首节点 包括元素和文本
                firstElementChild---首节点 只包括元素

     nodeType 子节点类型  ==3 文本节点； ==1 元素节点
     父节点 parentNode---查找元素的父节点
     offsetParent 获取页面的实际位置

    元素属性操作：
    第一种：oDiv.style.display='block';
    第二种：oDiv.style['display']='block';
    第三种：dom的方式
            获取元素 oTxt.getAttribute('value');
            设置元素 oTxt.setAttribute('value','abc');
            删除元素 oTxt.removeAttribute('value');
   DOM批量选取元素：className  封装函数getByClass

lesson12：
DOM操作应用
    创建DOM元素：createElement('标签名')  
                              appendChild(子节点)  添加到父节点末尾，原来的删掉
     插入DOM元素：insertBefore(子节点，在谁之前) 父级
     删除DOM元素：父节点.removeChild(具体节点)
        
文档碎片：
创建：document.createDocumentFragment  不常用

lesson13:
表格：
    tbody：自动会增加---一般主动写上 <td>列 <tr>行
                tHead 唯一表头
                tFoot 唯一表尾
                tBodies 找到所有tbody 不添加时会自动增加
                rows 找到所有行
                cells 找到所有列
       表格的添加、删除一行：
       表格搜索：大小写转换 toLowerCase
                         模糊搜索 search 找到并且返回字符串出现的位置 -1没找到
                         模糊搜索 split
                            高亮  筛选
        表格排序：li排序 sort(function(li1,li2){ })


lesson15：
JS运动基础：
    运动框架--1.在开始运动前，关闭已有定时器；2.把运动好停止用if/else隔开
            例子：分享到  淡入淡出图片（获取透明度：alpha）
    缓冲运动：控制速度 
                   Math.ceil(3.01)---向上取整---4
                   Math.floor(4.5)---向下取整---4
                    例子：滚动条抖动
                                document.clientHeight 屏幕可视区域
                                右侧悬浮框和对联

lesson20：
JS事件：
event对象：鼠标位置和键盘按键 function(ev)
                    document:chlidNodes[0].tagName
                    点击的坐标：event.clientX ---横坐标
                                         event.clientY ---纵坐标
                                不兼容 火狐浏览器 ev
            兼容写法         
            var oEvent = ev || event;   
                           事件流：事件冒泡
                                          取消：oEvent.cancelBubble=true;                           
鼠标事件：鼠标坐标 onmouseover onmousemove
                  event.clientX --可视区域的X
                  event.clientY --可视区域的Y
                  div的高度，是整个页面的高度 clientX +scrollTop 
                  scrollTop  =document.scrollTop||body.scrollTop

键盘事件：KeyCode
                onkeydown---键盘按下
                ctrlKey---ctrl按下
                shiftKey---shift按下
                altKey---alt按下

  默认行为：浏览器自带的行为
                    1.右键菜单 屏蔽  contextmenu  阻止 return false
                    2.自定义右键菜单 先阻止，然后自定义
                    3.只能输入数字的输入框
                         onkeydown 键盘按下阻止 return false
                        keyCode 0-48 9-57

   拖拽：鼠标按下 onmousedown
              鼠标移动 onmousemove
              鼠标松开 onmouseup---取消移动事件

JS事件高级应用：
    事件绑定：
                    attachEvent（事件名字，函数）---绑定事件---不兼容chrome
                    addEventListener(事件名，函数，false)---不兼容IE
                    if(oBtn.attachEvent){}else{}

    高级拖拽：
    自定义滚动条：

lesson24:
AJAX: js读取服务器的数据
            读取静态文件，编码方式注意utf8
            缓存：浏览器访问的缓存 IE特别严重 
                       阻止缓存：文件后面？时间戳
            读取动态数组：eval（str）字符串转成数组
            读取json：[{x:0,y:50,z:80}]
HTTP请求方式:
            get ：通过网址 容量小 安全性差 有缓存  获取数据
            post：不通过网址  容量大2G 安全性好一点 没有缓存 上传数据
自己编写ajax：（类似打电话 手机 连接 说 听）
            1.创建ajax对象--
       非IE6： var oAjax = new XMLHttpRequest();
       IE6：    var oAjax = new ActiveXObject("Miscrosoft.XMLHTTP");
            2.连接到服务器--
            3.告诉服务器，要啥文件，发送请求--
            4.接收返回值--

lesson25:
变量和属性：全局变量  a ==window.a









W3C:
http://www.w3school.com.cn/js/index.asp


freecodecamp：
网站学习
https://freecodecamp.cn/challenges/comment-your-javascript-code

1.comment your javascript code
注释代码
//  单行注释
/*  */  多行注释

2.decalre javascript variables
js提供七种不同的data types数据类型：
undefined 未定义
null 空
boolean 布尔型
string 字符串
symbol 符号
number 数字
object 对象

3.understanding case sensitivity in variables
JS中所有变量都是大小写敏感的。
使用驼峰命名法来书写变量，变量的第一个单词首写字母小写，后面的单词第一个字母大写。
var thisName="Tina";

4.quoting strings with single quotes
JS中的字符串用单引号或双引号来包裹它。
双引号包裹的时候，需要用斜杠双引号来转义，有时难以阅读；
这时候可以用单引号包裹，双引号就不用转义。
var myStr = '<a href="http://www.example.com" target="_blank">Link</a>';

5.escape sequences in strings
字符串中的转义序列
\' 单引号 \" 双引号 \\反斜杠 \n换行符 \r回车符 \t制表符 \b退格符 \f换页符

6.find the length of a string
通过字符串变量或字符串后面写上.length来获取到字符串变量的长度。
lastNameLength=lastName.length;

7.store multiple values i on variable using JavaScript Arrays
数组：在一个地方存储多个数据
var sandwich=["butter","milk",12];

8.nest one array within another array
多维数组 
var ourArray = [["the universe", 42], ["everything", 101010]];
             
9.mainpulate arrays with push
将数据追加到一个数组的末尾，通过push()函数
var arr = [1,2,3];
arr.push(4);
// 现在arr的值为 [1,2,3,4]

10.mainpulate arrays wiht pop
改变数组中数据的另一种方法使用.pop()函数
.pop()是用来抛出一个数组末尾的值

11.mainpulate arrays with shift
改变数组中数据的另一种方法使用.shift()函数
.shift()是用来移出数组的第一个元素

12.mainpulate arrays with unshift
改变数组中数据的另一种方法使用.unshift()函数
.shift()是用来移入一个元素到数组的第一个位置
myArray.unshift(["Paul",35]);

13.write resuable javascript with functions
在JS中，我们可以把代码的重复部分抽出来，放到一个函数（functions）中。
function functionName() {
console.log("Hello World");
}

14.passing values to functions with arguments
形参即形式、实参即内容。
function testFun(param1, param2) {
console.log(param1, param2);
}

15.global vs local scope in functions
一个程序中有可能具有相同姓名的局部变量和全局变量。
在这种情况下，局部变量优先于全局变量。
var someVar = "Hat";
function myFun() {
var someVar = "Head";
return someVar;
}

16.comparison with the strict equality operator
=== 严格等于 例如 1===“1”false
==等于  例如1==“1”true

17.bulid javascript objects
对象和数组很相似，数组是通过索引来访问和修改数据。
对象是通过属性来访问和修改数据的。
var myDog = {
  "name":"myDog",
  "legs":4,
  "tails":1,
  "friends":[1,3,5]
};

18.accessing objects projecties wiht the Dot operator
两种方式访问对象属性，一个是点操作. 一个是中括号操作[]
var myObj = {
prop1: "val1",
prop2: "val2"
};
var prop1val = myObj.prop1; // val1
var prop2val = myObj.prop2; // val2

19.accessing objects properties with variables
中括号操作符的另一个使用方法是用变量来访问一个属性。
var myDog = "Hunter";
var dogs = {
Fido: "Mutt", Hunter: "Doberman", Snoopie: "Beagle"
}
var breed = dogs[myDog];
console.log(breed)// "Doberman"

20.delete properties form a javascript object
delete myDog.tails;

21.using objects for lookups
对象和字典一样，可以用来存储键/值对。
var alpha = {
1:"Z",
2:"Y",
3:"X",
4:"W",
...
24:"C",
25:"B",
26:"A"
};
alpha[2]; // "Y"
alpha[24]; // "C"

var value = 2;
alpha[value]; // "Y"

22.testing objects for properties
检查对象属性是否存在，可以用.hasOwnProperty(propname)

23.introducing javascript object notation json
简称JSON，它使用js对象来存储数据。
var ourMusic = [
{
"artist": "Daft Punk",
"title": "Homework",
"release_year": 1997,
"formats": [
"CD",
"Cassette",
"LP" ],
"gold": true
}
];

24.accessing nested arrays in json
json对象可以嵌套对象和数组。与访问嵌套对象一样，用中括号操作同样可以嵌套数组。
// 初始化变量
var myPlants = [
  {
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }  
];

var secondTree = myPlants[1].list[1]; // 请修改这一行

25.generate random fractions with javascript
计算机行为只有两种，确定性和随机性。
Math.random()用来生成0-1包括0不包括1之间的随机小数。

26.generate random whole numbers with javascript
Math.random()随机小数 例如*20 
Math.floor()向下取整     例如0-19之间的整数

27.generate random whole numbers within a range
生成随机数在0到某个数之间，我们要生成的随机数是在2个指定数之间
function ourFunction(ourMin, ourMax) {

  return Math.floor(Math.random() * (ourMax - ourMin + 1)) + ourMin;
}

ourFunction(1, 9);

28.shift through text with regular expressions
regular expressions 正则表达式被用来根据某种匹配模式来寻找string中的某些单词
regular expressions分成几段：
/ 头部
the 匹配的模式
/ 尾部
g 代表global全局，意味着返回所有的匹配而不仅仅是第一个
i 代表着忽略大小写
例如：
// 初始化变量
var testString = "Ada Lovelace and Charles Babbage designed the first computer and the software that would have run on it.";

// 举例
var expressionToGetSoftware = /software/gi;
var softwareCount = testString.match(expressionToGetSoftware).length;

29.find numbers with regular expressions
正则表达式中使用特殊选择器来选择特殊类型值
其中一个就是数字选择器\d，意思用来获取一个字符串的数字
在JS中类似于 /\d/g  
/\d+/g 它允许这个正则表达式匹配一个或者更多数字
例如：
// 初始化变量
var testString = "There are 3 cats but 4 dogs.";
var expression = /\d+/g;  // 请修改这一行
// 用 digitCount 存储 testString 中匹配到 expression 的次数
var digitCount = testString.match(expression).length;

30.find whitespace wiht regular expressions
使用正则表达式\s来选择一个字符串的空白
空白字符有 " "空字符 \r回车符 \n换行符 \t制表符  \f换页符
空白正则表达式类似于：/\s+g 
例如：
var testString = "How many spaces are there in this sentence?";
var expression = /\s+/g;  // 请修改这一行
// 用 spaceCount 存储 testString 中匹配到 expression 的次数
var spaceCount = testString.match(expression).length;

31.invert regular expression matches with javascript
可以用正则表达式选择器的大写版本来转换任何匹配
\s陪陪任何空白字符 \S匹配任何非空白字符
例如：
// 初始化变量
var testString = "How many non-space characters are there in this sentence?";
var expression = /\S/g;  // 请修改这一行
// 用 nonSpaceCount 存储 testString 中匹配到 expression 的次数
var nonSpaceCount = testString.match(expression).length;



构造函数object oriented and functional programming
1.construct javascript objects whth functions
用构造函数来创建对象
构造函数 通常使用大写字母开头，以便跟其他普通函数区分
var Car = function() {
  this.wheels = 4;
  this.engines = 1;
  this.seats = 1;
};

2.declare javascript objects as variables
js创建对象
var car = {
  "wheels":4,
  "engines":1,
  "seats":5
};

```

