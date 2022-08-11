---
layout: post
title: Mistakes in LaTex
date: 2022-06-27
categories: Programming
tags: [LaTex]
description:
---

## About the equation.

When you use a wrong combination, the program will have errors.

For example, if you use begin aligned seperately, you will encounter some problems.

- begin align

end align

- begin equation

begin aligned

end aligned

end equation

- \\[
begin split
end split
\\]

## About the text

You could use \\mbox{content} or \\text{content}

## Special Symbol

\\mathbf: bold font, denote the vector

\\mathbb: blackboard-bold, denote the set

\\mathcal: mathematical fonts, denote the space

The main one is in the fact that \mathrm{xyz} behaves like an ordinary letter(math mode with no spaces), while \operatorname{xyz} behaves like function names such as \sin.

## About debug

You'd better run the file while writing, then you can notice any changes causing errors.

But if not, you should comment some right chapters, just debug the suspicious parts.

##  Misc

Always use $ $ enclose \keyword. 
Find whether you lack the pair of some symbols.
This one will be ignored easily.

Use a good editor to help you find some inconspicuous errors.