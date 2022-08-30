---
layout: post
title: How to open Jyputer Notebook with a specified environment.
date: 2022-08-29
categories: Programming
tags: [Python]
description: 
---

0. `conda install nb_conda`

1. Check the environment.

`conda env list`

2. Enter into the environment.

`conda activate env`

3. install a package at your new env

`conda install ipykernel` or

`conda install -n your_env ipykernel`

`python -m ipykernel install --env` 

