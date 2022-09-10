---
layout: post
title: Basic elements convert in Python
date: 2022-09-09
categories: Programming
tags: [Python]
---

## List to Dictionary

```python
a = ['a1','a2','a3','a4']
b = ['b1','b2','b3']
d = zip(a,b)
print(dict(d))  # {'a1': 'b1', 'a2': 'b2', 'a3': 'b3'}
```

### Use counter to obtain a aggregated form from List

```python
from collections import Counter
counter_dic = Counter(counter_list)
```

## Dictionary to List

```python
list(dit) # key

list(dit.values())  # value
```

## List to Numpy array

```python
import numpy as np
np.array(mylist)
```

## Numpy array to List

```python
list(nparray)

nparray.tolist()
```

## String to int or the reverse

```python
int(string)

str(int)
```

## String to list
```python
li=['a','b','c']
print(' '.join(str(i) for i in li))
```

Notice that List will store the address, thus it can contain different types. 
For np array, all elements are the same type.