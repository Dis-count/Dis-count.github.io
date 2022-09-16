---
layout: post
title: Matrix Derivative
date: 2022-09-15
categories: MachineLearning
tags: [MachineLearning]
---

## Different notations
Notice that if we think $f$ expands in a column way, i.e.,

$\frac{\partial f}{\partial x}=\left[\begin{array}{cccc}\frac{\partial f_1}{\partial x_1} & \frac{\partial f_2}{\partial x_1} & \cdots & \frac{\partial f_m}{\partial x_1} \\ \frac{\partial f_1}{\partial x_2} & \frac{\partial f_2}{\partial x_2} & \cdots & \frac{\partial f_m}{\partial x_2} \\ \vdots & \vdots & \ddots & \vdots \\ \frac{\partial f_1}{\partial x_p} & \frac{\partial f_2}{\partial x_p} & \cdots & \frac{\partial f_m}{\partial x_p}\end{array}\right]$

Then, 
$\begin{aligned} \frac{\partial \mathbf{x}^T \mathbf{a}}{\partial \mathbf{x}} &=\frac{\partial \mathbf{a}^T \mathbf{x}}{\partial \mathbf{x}}=\mathbf{a} \\ \frac{\partial \mathbf{a}^T \mathbf{X} \mathbf{b}}{\partial \mathbf{X}} &=\mathbf{a b}^T \end{aligned}$.

If $f$ expands in a row way, then take the transpose form.

Commonly, we use the first notation by default.


## Skills

Always remember that 

$\left[\frac{\partial \mathbf{x}}{\partial y}\right]_i=\frac{\partial x_i}{\partial y} \quad\left[\frac{\partial x}{\partial \mathbf{y}}\right]_i=\frac{\partial x}{\partial y_i} \quad\left[\frac{\partial \mathbf{x}}{\partial \mathbf{y}}\right]_{i j}=\frac{\partial x_i}{\partial y_j}$

Then you will not make a mistake again.

Find http://matrixcookbook.com for more details.
