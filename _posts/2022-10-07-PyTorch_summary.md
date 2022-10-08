---
layout: post
title: PyTorch summary
date: 2022-10-07
categories: Programming
tags: [PyTorch]
---

## About the dimension

In most cases, system throws a warning because you made a wrong data dimension operation.

Watch out the dimension of specific data, you can use the following code to test.

```python
w1 = torch.tensor([[1, 2, 1]]) # torch.Size([1, 3])
w3 = torch.tensor([1, 2, 1])   # torch.Size([3])
w2 = w1.view(-1)  # in fact, w2 = w3
```

So there is a tiny difference between [1,3] and [3].

### View

```python
ww = torch.arange(12)
print(ww.view(3,-1))
print(ww.view(-1,4))
```

### Transpose

And notice the difference between transpose and view.

> [[1, 2, 1]] to [1, 2, 1] after view(-1), to [[1],[2],[1]] after t.()

When w1 = torch.Size([1,3]), transpose can take effect.
w1 = torch.Size([3]), no difference after t.()

## Basic operation

- ​* 和 torch.mul()​ ​等同，矩阵点乘
- ​@ 和 torch.mm(a, b) ​​等同，矩阵乘法
- .dot() ​​向量乘法
- ​.t()​​矩阵转置
-  ​torch.mv(a, w1)​ ​矩阵乘向量
-  ​​@ 和 \*​​ ​代表矩阵的两种相乘方式：​​@​​​表示常规的数学上定义的矩阵相乘；​​\* ​​表示两个矩阵对应位置处的两个元素相乘。

## For machine learning

Know what is the input and output.

For logistic model, the outputs can be the probability vector, or the specific label(-1,1) for two classes.

And for SVM model, the output should be (-1,1), so input is 28*28 pixels, output's dimension is one.

