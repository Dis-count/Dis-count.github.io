---
layout: post
title: How to create a virtual environment
date: 2022-08-19
categories: Programming
tags: [Python]
---

## Background

When developing software with Python, a basic approach is to install Python on your machine, install all your required libraries via the terminal, write all your code in a single .py file or notebook, and run your Python program in the terminal.

This is a common approach for a lot of beginners and many people transitioning from working with Python for data analytics.

This works fine for simple Python scripting projects. But in complex software development projects, like building a Python library, an API, or software development kit, often you will be working with multiple files, multiple packages, and dependencies. As a result, you will need to isolate your Python development environment for that particular project.

Consider this scenario: you are working on app A, using your system installed Python and you pip install packageX version 1.0 to your global Python library. Then you switch to project B on your local machine, and you install the same packageX but version 2.0, which has some breaking changes between version 1.0 and 2.0.

When you go back to run your app A, you get all sorts of errors, and your app does not run. This is a scenario you can run into when building software with Python. And to get around this, we can use virtual environments.

This tutorial will cover everything you need to know about virtual environments and how to set one up with `Virtualenv`.

[Tutorial](https://www.freecodecamp.org/news/how-to-setup-virtual-environments-in-python/)




1. Create a virtual environment(Named 'ancillary')

> conda create --name ancillary python=3.7

> conda create -n ancillary python=3.7

2. Check the envs.

~~~python
conda  info --envs
~~~

3. Activation

```python
conda activate ancillary
```

4. Check the packages

> pip list

5. install a new packages

pip install ipykernel

6. install jupyter menus

```python
python -m ipykernel install --user --name ancillary --display-name "Python (ancillary)"
jupyter lab
```

7. Test kernel

```python
import sys
print (sys.executable)
```