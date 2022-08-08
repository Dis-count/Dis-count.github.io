---
layout: post
title: Java basics
subtitle: main method
categories: Programming
tags: [Java]
---

Java 基础之 main 方法解读：

一、深入理解 main 方法：（由java虚拟机调用）
解释 main 方法的形式：public static void main (String [] args){}

-1.Java虚拟机需要调用类的 main()方法，所以该方法的访问权限必须是 public；

-2.Java虚拟机在执行 main() 方法的时候不必创建对象，所以该方法必须是 static；

-3.该方法接收 String 类型的数组参数，该数组中保存执行 Java 命令是传递给所运行的类的参数；

-4.Java执行程序时，传入参数。

二、特别提示：

-1.在 main() 方法中，我们可以直接调用 main() 方法所在类的静态方法或静态属性。

-2.但是，不能直接访问类中的非静态成员，必须创建该类的一个实例对象后，才能通过这个对象去访问类中的非静态成员。

三、main 方法是我们学习 Java 语言学习的第一个方法, 也是每个 Java 使用者最熟悉的方法, 每个 Java 应用程序都必须有且仅有一个 main 方法。在eclipse里可以使用输入main, 在按住 Alt+/ 的方式快速创建 main 方法。