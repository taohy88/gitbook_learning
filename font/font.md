# 前端知识体系

### 前端三要素

1. 结构层 HTML

   超文本标记语言，决定网页的结构和内容。

2. 表现层 CSS

   层叠样式表，设定网页的表现样式。什么是CSS预处理器？用一种专门的编程语言，进行Web页面样式设计，再通过编译器转化成正常的CSS文件，以供项目使用。
   常用的CSS预处理器有哪些？----SASS和LESSSASS：基于Ruby，通过服务端处理，功能强大。解析效率高。需要学下Ruby语言，上手难度高于LESS。LESS：基于NodeJS，通过客户端处理，使用简单。功能比SASS简单，解析效率也低于SASS,但在实际开发中足够了，所以我们后台人员如果需要的花，建议使用LESS。

   常用的CSS预处理器有哪些？----SASS和LESSSASS：基于Ruby，通过服务端处理，功能强大。解析效率高。需要学下Ruby语言，上手难度高于LESS。LESS：基于NodeJS，通过客户端处理，使用简单。功能比SASS简单，解析效率也低于SASS,但在实际开发中足够了，所以我们后台人员如果需要的花，建议使用LESS。

3. 行为层 JavaScript

   是一种弱类型脚本语言，其源代码不需要经过编译，而是由浏览器解释运行，用于控制网页的行为。Native原生JS开发：原生JS开发，也就是让我们按照ECMAScript标准的开发方式，简称ES，特点是所有浏览器都支持。
   TypeScript微软的标准：是一种由微软开发的自由和开源的编程语言。它是JavaScript的一个超集，而且本质上向这个语言添加了可选的静态类型和基于类的面向对象编程。会导致很多浏览器不直接支持TypeScript语法，需要编译后成JS才能被浏览器正确执行。
   JavaScript框架：jQuery：大家熟知的JavaScript框架，有点是简化了DOM操作，缺点是DOM操作太频繁，影响前端性能。在前端眼里，使用它仅仅是为了兼容IE6,7,8;Vue：一款渐进式JavaScript框架，所谓渐进式就是逐步实现新特性的意思，如实现模块化开发、路由、状态管理等新特性。其特点是综合了Angular(模块化)和React(虚拟DOM)的优点。
   UI框架：ElementUI：饿了么出品，基于Vue的UI框架。Bootstrap：Twitter推出的一个用于前端开发的开源工具包。
   JavaScript构建工具：Babel：JS编译工具，主要用于浏览器不支持ES的新特性，比如用于编译TypeScript。WebPack：模块打包器，主要作用是打包、压缩、合并及按序加载。



### 当前主流前端框架

[Vue.js](font/vue.md)

iView：主要特点是移动端支持较多ElementUI：主要用于开发PC端的页面，是一个质量比较高的Vue UI组件库。主要特点桌面端支持较多。



| TodoList       |                       |      |
| -------------- | --------------------- | ---- |
| HTML           |                       |      |
| CSS            | sass scssstylus       |      |
| CSS框架        | BootStarpLayUI        |      |
| JavaScript     | 基础语法进阶ES6       |      |
| JavaScript框架 | VueReactAngularjQuery |      |
| Node           | 常用API对象池异常处理 |      |
| 静态编译       | FlowTypeScript        |      |
| 打包工具       | webpackgluprollup     |      |
| 工具           | npmyarn               |      |