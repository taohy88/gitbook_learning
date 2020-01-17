# Python





### Web2py框架

```
http://www.web2py.com/books/default/chapter/35/02/python

1.python
help()对象
dir()方法
类型：没有变量，type(a) 值有类型

字符串：ASCII字符串 '...'   "..."   '''...'''   """...""" 
               Unicode字符串  u开始
               例如：Unicode 转换成字符串
               b=u"This is a Unicode String"
               a=b.encode('utf8')
               变量转成字符串：
               >>>print "number is " + str(3)
               >>>print "number is %s" % (3)
               >>>print "number is %(number)s" % dict(number=3)
              
列表：主要方法 append insert del len 数据可修改
               例如：>>> a=[1,2,3]
               >>>a.append(8)
               >>>a.insert(2,7)
               >>>del a[0]
               >>>print a
               [2,7,3,8]
               >>>print len(a)
               4
               切片：
               >>>print a[:3]
               >>>[2,7,3]
               >>>print a[1:]
               >>>[7,3,8]
               >>>print a[-2:]
               >>>[3,8]
               遍历：
               >>>a=[1,2,3]
               >>>for i in a:
                              print i
               >>>1
               >>>2
               >>>3
               例如：
               >>> a = [1,2,3,4,5,6]
               >>>b=[]
               >>> for x in a:
                              if x%2==0:
                                   b.append(x*3)
               >>>b
               [6,12]
               简单写法：
               >>>a=[1,2,3,5,6]
               >>>b=[x*3 for x in a if x%2==0]
               >>>b
               [6,12]

元组：数据不可修改
          >>>a = (1,2,3)
          >>>a = (1,) #一个元素构成的元组必须以逗号结尾
          高效封装对象,括号是可选的
          >>>a=2,3，"hello"
          >>>x, y, z = a
          >>>piint x
          2
          >>>print z
          hello

字典：哈希表 将键对象映射成值对象
     >>> a = {"k1":"v","k2":3}
     >>>a["k1"]
     >>>v
     >>>a["k2"]
     >>>3
     >>>a.has_key["k1"]
     >>>True
     >>>a.has_key["k2"]
     >>>False
     例如：dict声明字典
     >>>a = dict(k1="v",k2=3)
     >>>a["k1"]
     >>>v
     >>>print a
     >>>{"k1":"v","k2":3}
     实用方法：has_key keys values items
     >>>a = dict(k1="v", k2=3)
     >>>print a.keys()
     >>>["k1","k2"]
     >>>print a.values()
     >>>["v",3]
     >>>print a.items()
     >>>[{"k1":"v","k2":3}]
     hash运算符将对象转换成整数，并得到整数数值储存地址：
     >>>hash("hello world")
     >>>-15008076455

for in:
     >>>for i in xrange(0,4):
     >>>     print i
     >>> 0
     >>> 1
     >>> 2
     >>> 3

enumerate:循环的同时计数
     >>>a=[0,1,"a","b"]
     >>>for i , j in enumerate(a)
     >>>      print i j
     >>> 0 0
     >>> 1 1
     >>> 2 a
     >>> 3 b

try...except...else...finally:
     >>>try:
     >>>     a= 1/0
     >>>except Exception,e:
     >>>     print "oops:%s" %e
     >>>else:
     >>>     print "no problem here"
     >>>finally:
     >>>     print "done"


函数申明：def...return...
     >>>def f(a,b):
     >>>     return a+b
     >>>print f(4,2)
     >>> 6
     
     例如：     
     *a  元组 **b 列表
     >>>def f(*a, **b)
     >>>     return a,b
     >>>x,y=f(3,"hello",c=4,test="world")
     >>>print x
     >>>(3,"hello")
     >>>print y
     >>>{"c":4,"test":"world"}

lambda函数：
     >>> a= lambda b:b+2
     >>> print a(3)
     >>>5
     例如：map 创建新列表
     >>>a=[1,7,2,5,4,8]
     >>>map(lambda x:x+2,a)
     >>>[2,9,4,7,6,10]

类：
     >>> class MyClass(object):
     >>>      z=2          #类变量
     >>>     def __init__(self,a,b):      #构造函数 self当前对象
     >>>           self.x=a, self.y=b
     >>>      def add(self):
     >>>           return self.x+self.y+self.z
     >>> myinstance=MyClass()
     >>> print myinstance.add()
     >>> 9

类的特殊属性、方法和运算符：
双下划线开头 __len__  __getitem__ __setitem__
     >>> class MyList(object):
     >>>     def __init__(self,*a): self.a=list(a)
     >>>     def __len__(self): return len(self.a)
     >>>       def __getitem__(self,i):return self.a[i]
     >>>     def __setitem__(self,i,j):self.a[i]=j
     >>>b=MyList(3,4,5)
     >>>print b[1]
     >>>4
     >>>b.a[1]=5
     >>>print b.a
     >>>[3,5,5]


文件输入、输出：
>>> file = open("myfile.txt","w")
>>> file.write("hello world")
>>> print file.read()
>>> file.close()
方式：rb二进制模式下读取，wb二进制模式下写入，a附加模式下打开
>>>print file.seek(6)  #跳转到对应位置
>>>print file.read()
>>>world


import:
python调用其他库模块
>>>import random
>>>print random.randint(0,9)
>>>5
          
          局部导入：
>>>from random import randint
>>>print randint(0,5)

os模块：
提供一个操作系统API接口
     >>>import os
     >>>print os.environ  #访问系统的环境变量

sys模块：
包含许多变量和函数，使用最多的是sys.path
     >>>import sys
     >>>sys.path.append("path/to/my/modules")

     >>>path = "path/to/my/modules"
     >>>if not path in sys.path:
     >>>     sys.path.append(path)



 datatime模块：
     >>>import datetime
     >>>print datetime.datetime.today()
     >>>2017-11-28
     >>>print datetime.datetime.utcnow()
     >>>2017-11-28 06:31:26.104260
     时间模块中包含：date datetime time medelta
   
time模块：表示时间从纪元1970年开始的秒数
     >>>import time
     >>>t=time.time()
     >>>1511850802.6035957
             
```

