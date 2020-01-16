# 正则表达式

参考资料：[wiki维基-正则表达式 ](https://zh.wikipedia.org/wiki/%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F)

```
 基本语法：
选择：
| 最低优先级。例如 gray|grey 可以匹配grey或者gray
数量限定 ：
+ 代表前面的字符必须至少出现一次。（1次或者多次）例如 goo+gle 可以匹配 google goooogle等
？代表前面的字符最多只可以出现一次。（0次或1次）例如 colou?r 可以匹配colour或者color
* 代表前面的字符不可以出现。（0次 1次 多次）例如  0*42可以匹配42、042、0042、000042等
匹配：
（）可以用来定义操作符的范围和优先度。例如 gr(a|e)y等价于gray|grey,(grand)?father匹配father和grandfather
```

