# Bootstrap

```
包内容：
基本结构：带有网格系统，链接样式，背景的基本结构。
CSS：全局CSS设置、基本的HTML元素样式、可扩展的class，以及先进的网格系统。
组件：十几个可重用组件，创建图像、下拉菜单、导航、警告框、弹出框。
js插件：十几个自定义的jquery插件
定制：定制bs的组件、less变量和jquery插件来得到自己的版本

CSS:
适应移动设备：
<meta name="viewport" content="width=device-width, initial-scale=1.0">
width属性控制设备的宽度。initial-scale=1.0确保网页加载时，以1:1的比例呈现，不会有任何缩放
响应式图像：
<img src="..." class="img-responsive" alt="响应式图像">
网格系统：
包含了一个响应式的、移动设备优先的、不固定的网格系统、可以随着设备的大小适当扩展到12列。
工作原理：行必须放在.container class内，获得适当的对齐alignment和内边距padding
        使用行来创建列的水平组
        内容应放置在列内，且唯有列可以是行的直接子元素
        预定义的网格类，比如.row .col-xs-4，可用于快速创建网格布局
        列通过内边距padding来创建内容之间的间隙。该内边距是通过.rows上的外边距margin取负，表示第一列和最后一列的偏移
        网格系统是通过您指定要横跨的十二个可用的列来创建的，例如：要创建三个相等的列，使用.col-xs-4



freeCodeCamp:
1.use responsive design with bootstrap fluid containers
响应式框架Bootstrap，根据屏幕的大小来调整HTML元素的大小。
<link rel="stylesheet" href="//cdn.bootcss.com/bootstrap/3.3.1/css/bootstrap.min.css"/>
HTML的所有内容放在class为container-fluid的div下。

2.make images mobile responsive
只要给图片添加class="img-responsive" 宽度就能自适应页面
<img class="img-responsive" src="/images/running-cat.jpg"/>

3.center text with bootstrap
bootstrap 居中头部元素，在class中添加text-center样式
<h2 class="red-text text-center">CatPhotoApp</h2>

4.create a bootstrap button
有它自己的button按钮风格，在button元素中添加class为btn的样式
<button class="btn">Like</button>

5.create a block element bootstrap button
将按钮伸展并填满页面整个水平空间，btn btn-block
<button class="btn btn-block">Like</button>


6.taste the bootstrap button color ranbow
深蓝色btn-primary是应用的主要颜色，用在那些用户主要操作上
<button class="btn btn-block btn-primary">Like</button>

7.button info
淡蓝色btn-info按钮
<button class="btn btn-info btn-block">Info</button>

8.warn your users of a dangerous action
红色btn-danger被用来提醒用户该操作具有“破坏性”,例如删除
<button class="btn btn-block btn-danger">Delete</button>

9.use the bootstrap grid to put elements side by side
响应式网格布局，可轻松实现将多个元素放入一行并指定各个元素的相对宽度需求。
bootstrap的12列网格布局

col-md-* 其中md是指中等大小的屏幕
col-xs-*   其中xs是指较小的屏幕
  <div class="row">
    <div class="col-xs-4">
      <button class="btn btn-block btn-primary">Like</button>
    </div>
     <div class="col-xs-4">
       <button class="btn btn-block btn-info">Info</button>
     </div>
     <div class="col-xs-4">
         <button class="btn btn-block btn-danger">Delete</button>
    </div>
  </div>

10.use span for inline elements
使用span标签来创建行内元素
<p>Things cats <span class="text-danger">love:</span></p>

11.create a custom heading
bootstrap的class都可以用在div的元素上
<div class="container-fluid">
  <div class="row">
    <div class="col-xs-8">
  <h2 class="text-primary text-center ">CatPhotoApp</h2>
    </div>
<div class="col-xs-4">
  <a href="#" ><img class="img-responsive thick-green-border " src="/images/relaxing-cat.jpg"></a>
    </div>
  </div>

12.add font awesome icons to our buttons
font awesome 图标库
<link rel="stylesheet" href="//cdn.bootcss.com/font-awesome/4.2.0/css/font-awesome.min.css"/>
<i class="fa fa-info-circle"></i>

13.House our page within a bootstrap container fluid div
确保页面所有内容都是响应式的
<div class="container-fluid"></div>

14.create bootstrap wells
bootstrap有一个class属性叫做well，作用是设定创造出一个视觉深度感。
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <div class="well"></div>
    </div>
    <div class="col-xs-6">
      <div class="well"></div>
    </div>
  </div>
</div>

15.apply the default bootstrap button style
bootstrap 有一种属于按钮的class btn-default
   <button class="btn btn-default"></button>

16.

```

