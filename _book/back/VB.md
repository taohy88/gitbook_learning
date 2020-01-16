# VB

#### 注释：单引

#### 声明变量 dim i as integer

#### 调试：debug.print a 立即窗口

运行程序 F5 逐语句调试 F8   

立即窗口 ctrl+G 开发界面中 输入 ?Asc("A")出现 ascii码   

调试报信息 msgbox   

添加监视，要在作用范围内，打断点然后监视   

rnd 随机数0-1   

错误处理：on error goto Line1  line1：语句



#### 数据类型：

字符型 string 定长字符型 dim stuID as string * 4
整型 integer 整数 +-n[%]  long 长整数 +-n& 除了十进制还可以表示 八进制&O 十六进制&H
浮点型 单精度 single 双精度 double +-n.n#
字节 byte 0-255 以一字节的无符号二进制
日期 date #
自定义数据类型 private type end type  声明放在最上面
符号常量 const max as integer=100,min=max-10 const PI#=3.14.15926



#### 数组：

默认下标为0 如果要从1开始 声明 Option Base 1
dim a[1 to 10] as integer 等价于 dim a%(1 to 10)
LBound UBound 获取数组下标



#### 运算符：

浮点除法 / 3/2=1.5
整点除法 \ 3\2=1
取模  Mod
不等于 <>
相等  =
逻辑非 not
逻辑与 and



#### 对象：

clipboard对象：
剪切板上的文本和图形
clipboard.settext  
clipboard.gettext



#### 方法：

show 的第一个参数 0 代表无模式 表示父窗口是活动的； 1代表有模式 表示父窗口是不可以活动的。
      
print的表达式为字符串 每次执行都会换行 如果要在同行显示，末尾增加分号或者逗号。
     Tab(n) 例如 print "姓名";tab(8);"年龄";tab(16);"籍贯"
     space(n)或者spc(n) print "计算机";space(10);"学习"

cls 清除屏幕上的图形或者文字



#### 窗口事件：

mousedown if button=2 then endif 如果鼠标右击按下去，触发事件。





#### 数据转换函数：

val函数：字符转换成数值 返回包含在字符内的数字，字符串是一个适当类型的数值。val(string)
str函数：数值转换成字符 返回数值 str（number）字符串的第一个位一定是空格或是正负号
hex(x)函数：十进制转换成十六进制
oct(x)函数：十进制转换成八进制
chr(x)函数：x转换成ASCII字符 chr(x)=A
asc(x)函数：返回x中第一个字符的ascii码 asc("ABC")=65
Cbool(x)函数：转换为逻辑型数据 cbool(1)=true
Cdate(x)函数：转换成日期数据 cdate("May 1,2010")=2010-5-1
cstr(x)函数：不止能转换数字，还能将其他类型也转换成字符串（比如Boolean,Error类型）
a = StrConv(S, vbFromUnicode) '字符串转换为字节数组 字符表示 中文两个字节 英文一个字节
S1 = StrConv(a, vbUnicode) '字节数组转换为字符串



#### 字符串函数：

LTrim(S) 去掉字符串左边的空格
RTrim(S) 去掉字符串右边的空格
Trim(S) 去掉字符串左右两边的空格
Left(S,n) 取字符串左边n个的字符
Right(S,n) 取字符串右边n个的字符
Mid(S,p,n) 取字符串右边n个的字符
Len(S)   测试字符串的长度
LenB(s)   测试字符串的字节长度
Instr(n,s1,s2) 从s1的第n个位置中查找s2的出现位置
Space(n)  返回由只指定数目空格字符串组成的字符串
String(n,s) 返回字符串s中的第一个字符重复指定次数的字符串 string(3,"ABC")="AAA"
Lcase(s) 小写字母组成的字符串
Ucase(s) 大写字母组成的字符串
instr(start,string1,string2,compare)=variant(long) 指定一字符串在另一字符串中最先出现的位置



#### 日期时间函数：

Now 返回系统日期/时间 2013-1-1 00:10:00
Time 返回系统时间 00:10:00
Timer 返回从午夜零点开始已过的秒数



#### 格式输出函数：

format(123.45,"0000.00") 输出0123.45 0显示一位数字或者零
format(123.45,"####.##") 输出123.45  #显示一位数字或者什么都不显示



#### 语句：

```

iif语句：
iif(条件，语句1，语句2)
true执行语句1
false执行语句2
 
do loop语句：
do while 条件
语句1
loop
或者
do
语句1
loop while 条件
 
while wend语句：
while 条件
语句1
wend
 
for next语句：
for i=1 to 100 step 1
语句1
next i
 
goto语句：
goto 行号或者标号
行号 1000 语句
标号 start:语句
 
for each    next语句：
专门用于数组和对象集合
for each  成员 in 数组
循环语句
next 成员
```



#### 过程：

```
子过程 public sub name()  end sub  调用时候用 call name()
函数过程 public function name (i as integer) as long  end function
值传递 byval
地址传递 byref (默认就是地址传递）
```



#### 控件：

```
text 文本框：
   属性：multiline 如果为true 呈多行显示
   属性：passwordchar 如果设置为* 输入后显示都为字符*
   属性：lock 设置为true 不能修改，只能选中和滚动显示
   属性：scrollbar 增加滚动条 只能在multiline属性启用多行时起作用
   常用事件：change keypress gotfocus lostfocus
             mousemove事件 在鼠标移动过程中，显示当前坐标的坐标位置
   控制输入只能输入数字：keypress事件中，输入keyascii为数字

command 命令按钮：
   属性：default 如果true 按下enter键 就是按下命令操作
   属性：cancel  如果true 按下esc键 就是按下命令操作
   属性：picture 要在style为1图形的时候起作用

option 单选按钮：
   属性：value 如果为true 就是选中状态

checkbox 复选按钮：
   属性：value如果为1 就是选中状态  如果为0 就是未选中状态 如果为2 就是禁止操作状态

listbox 列表框：
   属性: list  某项内容 从list(0)开始 例如 Me.List1.List(0) = "因子1"
   属性：listcount 列的个数
   属性：listindex 当前选中的列索引号 未选中为-1 然后从0开始
   属性：column 列属性 默认为0一列显示，设计时如果改成其他显示情况 可以多行显示
   属性：multiselcet 多重选择 0代表只能选中一个 1代表多个选中 2功能最强大 shift组合使用
   属性：style 类型 1代表标准型 2代表复选框型
   属性：selected 是否选中状态 true选中 false未选中 例如Me.List1.Selected (索引号)
   方法：additem 增加项目  例如：list1.additem "增加因子",1
   方法：removeitem 删除项目 例如：list1.removeitem(索引号)
   方法：clear 清除所有项目 例如：list1.clear

combobox 组合框：
   属性：style 类型 值为0时，下拉框组合可以输入文本；值为1时，文本输入的简单组合框；值为2时，下拉式列表框（不可输入）
   属性：text 文本 直接输入或编辑
   方法：同样支持listbox里面的additem removeitem clear方法

picturebox图形框：
   属性：picture 图片 me.picture=localpicture("路径")
   属性：autosize 自动显示 设置为true时，图像自动改变大小；false时，不具备自动调节功能

image图像框：
   属性：stretch 设置为true的时候自动调整
   区别：与图形框，图像框内存占用率更小，比较推荐使用

Hscrollbar vscrollbar水平垂直滚动条 ：
   属性：max min 最大最小值
   属性：val 数值 指定滚动条数值
   属性：smallchange 小改变 左右箭头单击的大小
   属性：largechange 大改变 滚动条单击的大小
   事件：scroll滑动过程中动态变化
   时间：change滚动到最后的值

timer 时间控件：
   属性：enabled 如果为true表示能做出反应 为false表示不能做出反应
   属性：interval 时间间隔 以毫秒为单位 最大为一分多钟

drivelistbox 磁盘列表框：
   属性：drive 运行时显示驱动器的名称  Me.Drive1.Drive = "E:"

dirlistbox 文件夹列表框：
   属性：path运行时显示当前文件夹的路径  Me.Dir1.Path = "E:\LNG监控系统\"

filelistbox 文件夹列表框：
   属性：filename 运行时文件清单  Me.File1.FileName = "E:\LNG监控系统\01_文档区\力控开发说明\*.xls"
```



高级控件：

工程--部件--控件--增加ACTIVEX

