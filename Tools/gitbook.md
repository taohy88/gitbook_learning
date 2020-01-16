# Gitbook

参考资料：[Youtube](https://www.youtube.com/watch?v=9ueZtU4S0t4&list=PLPn5f8o-k7JVlnm_xnByfv4IL_49VMbzu&index=2)

---

[TOC]



```
Git Doc参考:
https://docs.gitbook.com/integrations/github

Gitbook + Typora电子书：
https://blog.csdn.net/lu_embedded/article/details/81100704

Gitbook托管到Github:
https://yangjh.oschina.io/gitbook/UsingPages.html
```



### 前提

```
>>>npm --version 
#检查npm版本
>>>gitbook --version
#检查gitbook版本
#新建gitbook文件夹
```



### npm包

```
https://www.npmjs.com/package/gitbook
>>>npm install gitbook-cli -g
>>>gitbook init
>>>gitbook serve
>>>gitbook build
#初始化完成后，生成默认文件
SUMMARY.md   #gitbook目录
README.md  #gitbook介绍
```



### 自动生成文件

```
>>>gitbook init
#初始化完成后，默认生成2个文件
修改SUMMARY.md 目录文件，添加子目录等
>>>gitbook init
#重新初始化gitbook，目录中的文件会自动生成
```



### 打包



### 发布到Github

