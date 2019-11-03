---
title: Terminal Proxy
date: 2019-10-29 14:22:18
tags:
---

# Mac OSX 终端设置代理
使用mac下的brew安装软件时实在龟速，搜索发现普遍的解决方案为为终端配置代理，找到一篇讲得很好的博客来操作

*参考文章[https://github.com/mrdulin/blog/issues/18](https://github.com/mrdulin/blog/issues/18)，以下为摘录*

##关键步骤(以zsh为例)

```
~ vim ~/.zshrc

# proxy list
alias proxy='export all_proxy=socks5://127.0.0.1:1080'
alias unproxy='unset all_proxy'

~ source ~/.zshrc
```

