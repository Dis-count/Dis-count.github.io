---
layout: post
title: How to change the address of Jyputer Notebook.
date: 2022-08-28
categories: Programming
tags: [Python]
description: 
---

## Change the default address

1. Find the folder which is used to store 'config':
 
In `cmd`, input `jupyter notebook --generate-config`

2. find the file: 'jupyter_notebook_config.py', open it.

3. `c.NotebookApp.notebook_dir = 'specified path' `
delete the comment #

4.  reboot, done.

Remark:

'c.NotebookApp.browser' can change the browser.

the path should use `\\` rather than `\`.