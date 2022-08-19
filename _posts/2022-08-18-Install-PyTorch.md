---
layout: post
title: How to install PyTorch
date: 2022-08-18
categories: Programming
tags: [PyTorch]
---

## How to install PyTorch

1. enter anaconda base

2. conda create -n PyTorch python=3.9  
创建一个 python 的虚拟环境， PyTorch 是环境变量名（可以是任意英文）

Next time, you can activate this virtual environment directly.

Remark: conda env remove ***(PyTorch)

3. conda activate PyTorch
激活虚拟环境

(base) \to (PyTorch)  （开发环境）

4. 进入官网根据配置选择安装 GPU or CPU, 在(PyTorch) 环境下 run the command.

Remark: GPU only NVIDIA under Windows, 

5. type 'python', 'import torch'