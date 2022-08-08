---
layout: post
title: Leetcode Framework with Java
date: 2022-08-08
categories: Programming
tags: [Java]
---

Reference: https://zhangnai.xin/2016/09/20/LeetCode-Framework/

The post is used to record the leetcode framework by using Java.

1. At the beginning, I don't know how to program with Java. 

In order to improve the efficiency, we should formulate the procedure when we write the code.

2. Notice that there are two parts: test examples and algorithm realization.

You could put these two parts in one file, or write two java file to include them seperately.

## Example

-1. Create the package 'pid96';

-2. Create new class: Main.java, then a new method: main and test;

-3. Create new class: Solution.java, write your own algorithm code here and add the return value

Remark: that is the body code you need to write when you are playing leetcode. 

-4. Create the text examples in 'main' method, and call 'test' method repeatly.

-5. Instantiate Solution class in test method, run the algorithm and give the running time.

