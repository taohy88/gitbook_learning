# VS

```
加断点 F10下一步 F5整个结束
js调试 debugger；
调整格式 ctrl+k+d
显示函数 ctrl+j
后台代码中 #region 说明文字  #endregion
code.toupper 转化成大写字母
code.tolower 转化成小写字母
@page中
Inherits 定义当前Web窗体所继承的代码隐藏类system.web.ui.page
Src 指定代码隐藏文件在文件系统中的位置 便于框架动态编译找到  Inherits就是指明的类
CodeBehind 只是vs.net的一个属性，自动找到后台代码
 
XML 被设计用来传输和存储数据的 独立于软件和硬件的信息传输工具  W3C 的推荐标准
HTML 被设计用来显示数据


vs学习：
解决方案里面 db  src  vendor
db存放数据库
src存放webui还有app_data，webui中有webconfig文件
 
各文件后缀名：
.sln 解决方案问价 为解决方案资源管理器提供显示管理文件的图形接口所需的信息。
.csproj 项目文件 创建应用程序所需的引用、数据连接、文件夹和问价信息。
.html 页面文件
.aspx web窗体页 分两部分：视觉元素（html txt 服务器控件）和该页的编程逻辑。两部分分别存储在一个单独的文件中。
.aspx.cs web窗体页的编辑逻辑位于一个单独类文件
.cs 类模块代码文件，业务逻辑处理层代码
.asax global.asax文件（也叫做asp.net应用程序文件）是一个可选的文件，该文件包含响应 asp.net和http模块印发的应用程序级别事件的代码。
.config web.config 文件向他们所在的目录和所有子目录提供配置信息。
.aspx.resx 资源文件，资源在逻辑上应用程序部署的任何非可执行数据。
.css 样式文件，为Web窗体页的视觉元素设定初始显示样式
 
 
webconfig文件：
xml文本文件，存放asp.netweb应用程序的配置信息
数据库配置信息： <property name="connection.connection_string">server=.\SQL2008;uid=sa;pwd=frdb**..123;database=frdb_kyl</property>
 
app_data文件夹：
应该包含应用程序的本地数据存储。
app_code文件夹：
在创建网站时，系统为类自动放的位转瞬，存储所有应当作为应用程序的一部分动态编译的类文件。
 
 
 
新建项目或者网站的区别？
新建项目：建立winform项目，如EXE软件；web应用程序，主要做BS系统，default.aspx有两个源文件 default.aspx.cs和default.aspx.designer.cs ；有重新生成和发布两项。和一般的winform没有区别，都引用命名空间；可以作为类库被引用；添加asp.net文件夹中不包括bin app_code ；源文件是default.aspx.cs，还多了一项system.collections空间引用。
web网站：建立webform项目，如asp.net网站；default.aspx有1个源文件 default.aspx.cs；只发布一个网站；引用后出现在bin文件夹中存放dll和pdb文件；不可以作为类库别引用；添加asp.net文件夹中包括bin app_code ；源文件只有default.aspx.cs。
 
 
aspx是前台页面，cs是后台里面可以写方法之类
 
default.aspx文件：
protal.aspx文件：总页面
login.aspx文件：登陆页面
 
default.aspx文件:
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
此标签可告知浏览器文档使用哪种 HTML 或 XHTML 规范，文档使用主要命名空间
 
default.aspx.cs文件:添加了对程序集的引用，此程序集内的命名空间才能被using
using System.Data 来自文件 system.data.dll


VS下使用CL
1.\Common7\Tools 运行vsvars32.bat
2.环境变量中path设置\VC\bin
3.\Common7\IDE\msobj80.dll、mspdb80.dll、mspdbcore.dll、mspdbsrv.exe这四个文件拷贝至VC\bin下
4.在环境变量里添加变量INCLUDE，包含进VC\Include和VC\PlatformSDK\Include两个目录
5.添加变量LIB，包含进VC\lib和VC\PlatformSDK\LIB两个目录
成功
1.使用-GX选项时，2005的编译器会提示GX已过时，使用-EHsc代替
cl : Command line warning D9035 : option 'GX' has been deprecated and will be re
moved in a future release
cl : Command line warning D9036 : use 'EHsc' instead of 'GX'

vs调试：
加断点 F10下一步 F5整个结束
js调试 debugger；
调整格式 ctrl+k+d
显示函数 ctrl+j
后台代码中 #region 说明文字  #endregion
code.toupper 转化成大写字母
code.tolower 转化成小写字母
@page中
Inherits 定义当前Web窗体所继承的代码隐藏类system.web.ui.page
Src 指定代码隐藏文件在文件系统中的位置 便于框架动态编译找到  Inherits就是指明的类
CodeBehind 只是vs.net的一个属性，自动找到后台代码
XML 被设计用来传输和存储数据的 独立于软件和硬件的信息传输工具  W3C 的推荐标准

HTML 被设计用来显示数据

vs学习：
解决方案里面 db  src  vendor
db存放数据库
src存放webui还有app_data，webui中有webconfig文件
各文件后缀名：
.sln 解决方案问价 为解决方案资源管理器提供显示管理文件的图形接口所需的信息。
.csproj 项目文件 创建应用程序所需的引用、数据连接、文件夹和问价信息。
.html 页面文件
.aspx web窗体页 分两部分：视觉元素（html txt 服务器控件）和该页的编程逻辑。两部分分别存储在一个单独的文件中。
.aspx.cs web窗体页的编辑逻辑位于一个单独类文件
.cs 类模块代码文件，业务逻辑处理层代码
.asax global.asax文件（也叫做asp.net应用程序文件）是一个可选的文件，该文件包含响应 asp.net和http模块印发的应用程序级别事件的代码。
.config web.config 文件向他们所在的目录和所有子目录提供配置信息。
.aspx.resx 资源文件，资源在逻辑上应用程序部署的任何非可执行数据。
.css 样式文件，为Web窗体页的视觉元素设定初始显示样式
webconfig文件：
xml文本文件，存放asp.netweb应用程序的配置信息
数据库配置信息： <property name="connection.connection_string">server=.\SQL2008;uid=sa;pwd=frdb**..123;database=frdb_kyl</property>
app_data文件夹：
应该包含应用程序的本地数据存储。
app_code文件夹：
在创建网站时，系统为类自动放的位转瞬，存储所有应当作为应用程序的一部分动态编译的类文件。

新建项目或者网站的区别？
新建项目：建立winform项目，如EXE软件；web应用程序，主要做BS系统，default.aspx有两个源文件 default.aspx.cs和default.aspx.designer.cs ；有重新生成和发布两项。和一般的winform没有区别，都引用命名空间；可以作为类库被引用；添加asp.net文件夹中不包括bin app_code ；源文件是default.aspx.cs，还多了一项system.collections空间引用。
web网站：建立webform项目，如asp.net网站；default.aspx有1个源文件 default.aspx.cs；只发布一个网站；引用后出现在bin文件夹中存放dll和pdb文件；不可以作为类库别引用；添加asp.net文件夹中包括bin app_code ；源文件只有default.aspx.cs。
aspx是前台页面，cs是后台里面可以写方法之类
default.aspx文件：
protal.aspx文件：总页面
login.aspx文件：登陆页面
default.aspx文件:
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
此标签可告知浏览器文档使用哪种 HTML 或 XHTML 规范，文档使用主要命名空间
default.aspx.cs文件:添加了对程序集的引用，此程序集内的命名空间才能被using
using System.Data 来自文件 system.data.dll


说明：组合键是同时按，非组合键是按住Ctrl依次按后面的键
1.格式化
  格式化全部代码       Ctrl+A+K+F
  格式化选中的代码     Ctrl+K+F


2.注释代码
  注释代码             Ctrl+K+C（comment）
  反注释代码           Ctrl+K+U


3.代码录入智能提示
  组合键  Ctrl+J
  组合键  Alt+→

4.移动调整代码
  1）调整一行：按住Alt键同时，按方向键上或下可以调整代码的顺序
  2）同时移动多行：
a）先按住Shift+Alt 然后按上或下选中多行，有条竖线产生；
b）然后只松开Shift键，按上下方向键移动多行。

5.快速隐藏或显示当前代码段   
  组合键：Ctrl+M,M 按两次M


6.全屏显示/退出全屏显示 
  组合键 SHIFT + ALT + ENTER


7.剪切复制粘贴删除
  删除，复制，剪切一行代码不需要选中，只需要光标在这一行就是了
  复制 Ctrl+C
  剪切 Ctrl+X
  粘贴 Ctrl+V
  删除 Ctrl+L


8.在光标所在行的上面或下面插入一行 
  配合5使用，效果更佳
  在当前行的上面插入一个空行 组合键：Ctrl+Enter 
  在当前行的下面插入一个空行 组合键：Ctrl+Shift+Enter


9.查找和替换 
  查找  组合键：Ctrl+F 
  替换  组合键：Ctrl+H


10.大小写转换 
  转小写  组合键：Ctrl+ U 
  转大写  组合键：CTRL + SHIFT + U 


11.快速切换窗口 
  组合键：Ctrl+Tab


12.跳转到指定的某一行 
  组合键：Ctrl+G

13.矩形区域选择
  组合键：Shift+Alt+鼠标拖动  （很适合区域代码块选择）

```

