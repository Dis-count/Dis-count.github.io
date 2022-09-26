---
layout: post
title: Update Python and Conda
date: 2022-09-21
categories: Python
tags: [Python]
---

```python
word = "Hello"
print('word =', word)
print(f'word = {word}')
print(f'{word = }')
```

```python
conda update conda
conda update anaconda
```

## setting of jupyter notebook

[package](https://github.com/dunovank/jupyter-themes)

> pip install jupyterthemes

or

> conda install -c conda-forge jupyterthemes
> conda update jupyterthemes

```cmd
jt -t chesterish -f iosevka -fs 140 -altp -tfs 13 -nfs 115 -lineh 165 -cursc p -ofs 14 -cellw 75% -T
```

jt -r: 恢复默认

option: chesterish/ monokai/ 

t: theme

option: anka/anonymous/aurulent/bitstream/bpmono/'code'/'consolamono'/cousine/dejavu/
droidmono/fira/firacode/generic/hack/hasklig/inconsolata/inputmono/'iosevka'/
liberation/meslo/office/'oxygen'/roboto/saxmono/source/sourcemed/ptmono/ubuntu

f: code font

fs: code font-size

tfs: Text/MD Cell Fontsize

nfs: Notebook Font Size

altp: Alt Prompt Layout	

ofs: Output Area Fontsize

cellw: Cell Width

T: Toolbar Visible

lineh: Line Height

options: b (blue), o (orange), r (red), p (purple), g (green), x (font color)

cursc: Cursor Color 

altout: Alt Output BG Color