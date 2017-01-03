---
title: "usage of wiki"
layout: page
date: 2016-12-13 19:42
---

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

[TOC]

# usage of the wiki #

## 公式 ##

手写转lax [https://webdemo.myscript.com/views/math.html#](https://webdemo.myscript.com/views/math.html#)

lax 由markdown转网页 [http://www.jeyzhang.com/how-to-insert-equations-in-markdown.html](http://www.jeyzhang.com/how-to-insert-equations-in-markdown.html)

用的MathJax插件，主要：

插入

```
<script type="text/javascript"
   src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
```

行间公式：

`$$ 插入公式 $$`

行内公式:

`\\( 此处插入公式 \\)`

（注意：markdown文件中的_前需要加上\转移符。）

或,使用Google Chart的服务器:

```
<img src="http://chart.googleapis.com/chart?cht=tx&chl= 在此插入Latex公式" style="border:none;">
```

例子：
(在本机实验时，均可以用，但是貌似在远程访问的情况下，第一种方法不能用，问题暂时不清楚，可能是这种方式不适合远程用？网页相关知识还在学习中)

$$x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$$

\\(x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}\\)

<img src="http://chart.googleapis.com/chart?cht=tx&chl=\Large x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" style="border:none;">

