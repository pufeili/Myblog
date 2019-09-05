---
layout: post
title: "Python高级特性之列表生成式、生成器、迭代、可迭代对象与迭代器"
subtitle: ""
catalog: true
author: "WangW"
header-style: text
tags: 
    - python
    - iterable
    - generator
---


## 引言
在Python有几种高级特性比较重要，比如切片，迭代，列表生成式子，可迭代对象，生成器以及迭代器。本文主要讲解后面四种高级特性。  <!--break-->

迭代:
:    如果给定一个list或者tuple，我们可以通过``for``循环来遍历这个list或者tuple,这种遍历我们称为迭代（Iteration）.

列表生成式:
:    列表生成式即List Comprehensions, 是Python内置的非常简单却强大的可以用来创建list的生成式.

生成器:
:    字面意思就是生成数据的，可以看下文例子理解 (Generator)

迭代器:
:    可以被``next()``函数调用并不断返回下一个值的对象称为迭代器（Iterator）

可迭代对象:
:    可以直接作用于``for``循环的对象统称为可迭代对象（Iterable）

## 关系
首先，可以看的出来，迭代（Iteration）是一个概念，描述了一个循环遍历过程；不理解概念的可以先看后面例子帮助理解；

#### 列表生成式,可迭代对象,迭代器,生成器之间的关系

- **生成器既是可迭代对象，也是迭代器**：首先，生成器可以被``next()``调用，所以是迭代器；其次，生成器可以用于``for``循环，所以也是迭代器；
- **迭代器一定是可迭代对象，但是可迭代对象不一定是迭代器**：比如list, dict, str等集合数据类型是可迭代对象，但不是迭代器，但是他们可以通过``iter()``函数生成一个迭代器对象。
- **生成器包括生成式比如``(x*x for x in range(10))``,和带有``yield``的伸成函数**,仔细看，能够看的出来生成式和就是将列表生成式的中括号改成括号。

## 实例以及参考
- [Python之列表生成式、生成器、可迭代对象与迭代器](https://www.cnblogs.com/yyds/p/6281453.html)
- [廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1016959663602400/1017269809315232)