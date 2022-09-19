---
layout: post
title: Python issue
date: 2022-06-20
categories: Programming
tags: [Python]
description: 
---

## 四舍六入五成双/单

ieee754

round(1.315,2) = 1.31

round(7.55,1) = 7.5

## python判断某个模块是否有某个方法

```python
import requests
hasattr(requests,'get')
```

## 查看方法

```python
import typing
help(typing.List)
print(dir(typing))
typing.__file__
print(typing.__doc__)
```

## 查看源代码

inspect 一个Python内置的标准库
drill 是一个第三方库

> import inspect

> from bs4 import BeautifulSoup

先看看BeautifulSoup的文档定义

> inspect.getdoc(BeautifulSoup)

再来看看BeautifulSoup存放的路径

> inspect.getsourcefile(BeautifulSoup)

查看源代码的时候，可以用

> inspect.getsourcelines(BeautifulSoup)

> import dill

获得源代码文件路径

> dill.source.getsourcefile(BeautifulSoup)

获得源代码

> dill.source.getsourcelines(BeautifulSoup)

以上的输出和inspect一样，还有findsouce()函数

> dill.source.findsource(BeautifulSoup)