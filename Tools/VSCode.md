# VSCode

```
fedora系统：
语言设置--中文
ctrl+shift+P   搜索display language 按下Enter 修改local.json  把“en”改成“zh-CN”  保存
ctrl+P   复制  ext install MS-CEINTL.vscode-language-pack-zh-hans 点击安装


vscode:
设置python2和python3的环境
1.首先本地安装有不同的Python版本，比如2.7和3.5。mac下一般默认自带2.7版本。 
终端输入 python -V 则显示默认版本号。而python3 -V 则显示3.XX版本。 
2.终端输入查找需要即将使用的python版本的路径，如which python3。复制其路径，打开vscode。 
3.打开首选项，搜索python。setting.json里有很多关于python的配置，如果没有则需要安装python插件就好了。重点来了，找到 
// Path to Python, you can use a custom version of Python by modifying this setting to include the full path. 
"python.pythonPath": "python"，把之前复制的python路径复制到这替换,新建一个用户设置保存。如"python.pythonPath": "/usr/local/bin/python3"。 
4.新建一个test.py文件，右键run python file…即可使用python3



html文件输入!，直接生成html基本元素
```





### VSCode扩展程序：

参考资料：[youtube](https://www.youtube.com/watch?v=LdF2RcelRg0)

```
1. Live Server

2. Live Sass Compiler

   设置->settings->搜索sass->Live sass compiler->

3. HTML CSS Support

   编写css属性

4. Atuo Rename Tag

   修改开始的html元素，结束的元素也会随之改变

5. Prettier-Code formatter

   自动格式化代码，使用单引号，自动填充空格等。settings->搜索format on save->勾选settings->搜索Prettier->Jsx Single Quote->勾选settings->搜索Prettier->Single Quote->勾选

6. JavaScript(ES6) code snippets

   直接输入片段，会自动补齐imp -> import fs from 'fs';

7. Turbo Console Log

   调试的时候记录日志ctrl+alt+L

8. indent-rainbow

   缩进的时候，用不同颜色区域表示

9. Brackets Pair Colorizer

   不同层级的括号用不同颜色表示

10. REST Client

    处理Http请求getpot

11. GitLens-Git supercharged

    团队开发的时候，可以显示谁提交的信息

12. Atuo-Open Markdown Preview

    md文件，在vscode直接浏览

13. Vetur

    vue.js的插件
```

