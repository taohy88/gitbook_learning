# MVC

```
http://www.runoob.com/aspnet/mvc-intro.html

Model 模型
处理数据逻辑部分，负责在数据库中存取数据

View 视图
处理数据显示部分，依据模型数据创建

Controller 控制器
处理用户交互的部分，负责从视图中读取数据，控制用户输入、向模型发送数据

MVC文件夹：
应用程序信息：
Properties
References
应用程序文件夹：
App_Data文件夹  储存应用程序数据，SQL数据存入
Content文件夹       存放静态文件，例如CSS，png，site.css
Controllers文件夹  处理用户输入和响应的控制器类 ，要求所有的文件以"Controller"结尾
Models文件夹        应用程序模型的类
Scripts文件夹         存储应用程序的js文件
Views文件夹     存储与应用程序的显示相关的html文件，用户界面。包含每一个控制器对应的文件夹。Shared文件夹存储控制器分享的视图（母版页和布局页）。Home文件夹存放例如home页和about页之类的应用程序页面。Account文件夹包含用户账号注册和登录页面。
配置文件：
Global.asax
packages.config
Web.config

添加样式和统一布局：
views文件夹下面shared文件夹下，Layout.cshtml内容修改；
```

