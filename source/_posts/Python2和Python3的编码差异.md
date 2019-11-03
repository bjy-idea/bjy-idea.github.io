---
title: Python2和Python3的编码差异
date: 2019-11-01 18:01:51
tags:
---


# Python2和Python3的编码差异

## 1. 了解字符集和字符编码知识

参考链接[https://www.cnblogs.com/skynet/archive/2011/05/03/2035105.html#_3.4.UTF-8](https://www.cnblogs.com/skynet/archive/2011/05/03/2035105.html#_3.4.UTF-8)

*以下为自己的一些理解*

### 基础概念

1. 编码 将我们看到的字符已某种规则存储为二进制数据
2. 解码  将存储于计算机的二进制数据解析显示出来 解码错误即产生乱码
3. 字符集 抽象字符的集合 可以包括如文字，标点符号等等
4. 字符编码 将字符集合和数字集合建立关系的规则
5. 常见字符集名称 ASCII 字符集、GB2312 字符集、BIG5 字符集、GB18030 字符集、Unicode 字符集等。

## 2. Python2和Python3的编码差异

明确：str是文本，bytes是字节

参考链接
1. [https://blog.csdn.net/zengchen73/article/details/75302301](https://blog.csdn.net/zengchen73/article/details/75302301)
2. [https://www.cnblogs.com/20120810bubu/archive/2013/04/22/3036132.html](https://www.cnblogs.com/20120810bubu/archive/2013/04/22/3036132.html)

*以下为自己的一些理解*

### Python2
Python2 默认编码为ASCII，Unicode类型是单独的

```
Ptyhon2 中没有专门的bytes类型
>>> type(b'a')
<type 'str'>

>>> b'a'.encode('gb2312')
'a'  （字节encode之前会先进行decode,这在Python3中已经被取消）
```


```
a='nihao中国'
a  
'nihao\xe4\xb8\xad\xe5\x9b\xbd'
这里默认的编码为ascii，中文内容无法显示，所以输出实际字节内容
```

```
str(u'hello') 将unicode字符串转换为ascii字符串
```

### Python3

python2中是不区分bytes和str类型的，在python3中bytes和str中是区分的，str的所有操作bytes都支持

在python2中 u'a' 是 Unicode 对象
在python3中 u'a'就是Str对象

## 补充

str 编码得到 bytes
bytes 解码得到 str

