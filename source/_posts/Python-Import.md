---
title: Python Import
date: 2019-10-25 16:51:25
tags:
---

# Python Import 的一些问题

一直没认真研究过Python的import机制，最近遇到个问题

```
ValueError: attempted relative import beyond top-level package...
```

发现是相对路径import引起的

搜索了几篇不错的博客，在此记录一下（最好还是再看下官方文档）

1. import 的机制 [https://blog.csdn.net/weixin_38256474/article/details/81228492](https://blog.csdn.net/weixin_38256474/article/details/81228492)
2. import 绝对路径和相对路径用法的区别 [https://zhuanlan.zhihu.com/p/63143493](https://zhuanlan.zhihu.com/p/63143493)