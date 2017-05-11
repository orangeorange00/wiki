---
title: "python"
layout: page
date: 2017-1-6 15:48
---

[TOC]

#install and usage of python#

linux下安装比较简单，而windows下，可能因为我已经好久不用它工作了。。。觉得略麻烦。。。所以记录如下：

* 把python安装在自定义，比较好找的路径下。同时安装pip（某些版本包含在初始安装包中，在安装文件夹的Scripts文件下）。
* 然后把该路径加到系统path中。控制面板->系统和安全->系统->高级系统设置，双击系统变量框下的path变量，添加。
  这里我把pip的目录也加到系统路径下。即 pythong路径/Scripts
* 因为要实现python2 和python3共存，所以把python的exe分别修改成python27和python36，对应的srcipt也修改成对应名称。pip分别修改成pip27和pip36。

#language#

#little projects#

#difference between python2.7.x and python3.x#
没有详细对比，仅限于看到之后可以区别：(Python 3.x 介绍的 一些Python 2 不兼容的关键字和特性可以通过在 Python 2 的内置 __future__ 模块导入)

* python 3把print视为函数，python 2把print视为语句。python 3必须把输出语句用括号括起来，而python 2均可。

python 3

```
print('Hello World')
```

python 2
```
print 'Hello World'
print('Hello World')
```

* 不等于号<>被!=取代
