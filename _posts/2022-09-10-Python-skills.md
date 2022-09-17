---
layout: post
title: Skills frequently used in Python
date: 2022-09-10
categories: Programming
tags: [Python]
---

[add on that](https://blog.csdn.net/qsmx666/article/details/115433624)

## Usage of Bisect

bisect是python内置模块，用于有序序列的插入和查找。

查找： bisect(array, item)
插入： insort(array,item)

```python
import bisect
 
a = [1,2,2,5,8]
position = bisect.bisect(a,7)#找到插入位置
print(position)
# 4
bisect.insort(a,4)#找到位置插入
print(a)
# [1, 2, 2, 4, 5, 8]
bisect.bisect_left(a,2)#插到左侧
# 1
bisect.bisect_right(a,2)#插到右侧
# 3
```

## Usage of Counter

Return Counter, which is a dictionary essentially.

```python
from collections import Counter
# For integer
li=[1,2,2,4,5,5]
cnt = Counter(li)
# For strings
colors = ['red', 'blue', 'red', 'green', 'blue', 'blue']
c = Counter(colors)
# If you want a dic
dict(c)

# Also
c = Counter(a=3, b=1)
d = Counter(a=1, b=2)
c + d                       # 相加
#Counter({'a': 4, 'b': 3})
```

## Initialize all zeros

```python
# First
li=[0]*length
# Second
li=[0 for i in range(length)]
# Two-dimension
li = [[0] * 3 for i in range(4)]
```

## Remove duplicate

```python
l1 = [1,4,4,2,3,4,5,6,1]
l2 = list(set(l1))
print(l2)    # [1, 2, 3, 4, 5, 6]
```

## Misc

### Reverse

```python
string='leetcode'
print(string[::-1])
```

### Difference between characters
```python
print(ord('b')-ord('a')) 
```

### Print

Sometimes 

```python
print(variable) 
```
will not work in VScode.

Please use
```python
print('variable is:', variable) 
```

Or use cmd to test the code instead.

That is not the problem of your code, that is the problem of your editor.