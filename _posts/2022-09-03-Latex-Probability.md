---
layout: post
title: Some useful LaTex commands you could define
date: 2022-09-03
categories: Programming
tags: [LaTex]
description: 
---

# LaTeX Reference for Probability

## Shortcuts

These are commands you would define in the preamble.

```tex
\documentclass{article}
\usepackage{amsmath}

% COMMANDS GO HERE

\begin{document}
```

### Absolute Value

```tex
\newcommand{\abs}[1]{\lvert #1 \rvert}
\newcommand{\bigabs}[1]{\Bigl \lvert #1 \Bigr \rvert}
```

* `\abs{x}` becomes $$\lvert x \rvert$$
* `\bigabs{\frac{x}{2}}` becomes $$\Bigl \lvert \frac{x}{2} \Bigr \rvert$$

### Bigger Brackets


```tex
\newcommand{\bigbracket}[1]{\Bigl [ #1 \Bigr ]}
```

* `\bigbracket{\frac{1}{2} x^2}_{x=0}^{x=1}` becomes $${\Bigl [ \frac{1}{2} x^2 \Bigr ]}_{x=0}^{x=1}$$

### Bigger Parentheses

```tex
\newcommand{\bigparen}[1]{\Bigl ( #1 \Bigr )}
```

* `\bigparen{1 + \frac{1}{n}}^n` becomes $${\Bigl ( 1 + \frac{1}{n} \Bigr )}^n$$

### Ceiling and Floor

```tex
\newcommand{\ceil}[1]{\lceil #1 \rceil}
\newcommand{\bigceil}[1]{\Bigl \lceil #1 \Bigr \rceil}
\newcommand{\floor}[1]{\lfloor #1 \rfloor}
\newcommand{\bigfloor}[1]{\Bigl \lfloor #1 \Bigr \rfloor}
```

* `\ceil{\log_2 n}` becomes $$\lceil \log_2 n \rceil$$
* `\bigfloor{\frac{n}{2}}` becomes $$\Bigl \lfloor \frac{n}{2} \Bigr \rfloor$$

### Norms

```tex
\newcommand{\norm}[1]{\| #1 \|}
\newcommand{\bignorm}[1]{\Bigl \| #1 \Bigr \| #1}
```

* `\norm{x}_2^2` becomes $${\| x \|}_2^2$$
* `\bignorm{(X^T X)^{-1} X^T y}` becomes $${\Bigl \| (X^T X)^{-1} X^T y \Bigr \|}_2^2$$

### Inner Product

```tex
\newcommand{\inner}[1]{\langle #1 \rangle}
```

* `\inner{u, v}` becomes $$\langle u, v \rangle$$

### Sets

```tex
\newcommand{\set}[1]{\{ #1 \}}
```

* `\set{0, 1}^n` becomes $$\{ 0, 1 \}^n$$

### Style Files
To avoid defining these commands in the preamble of every document, you can make
.sty file that contains these commands. For example, add this file
[eecs.sty](/assets/eecs.sty) to an Overleaf project and then add the following
command in the preamble.

```tex
\documentclass[11pt]{article}
\usepackage[margin=1in]{geometry}

\usepackage{eecs}

\begin{document}
```

If you don't use Overleaf, just make sure `eecs.sty` is in the same directory as
your `.tex` file. You can also have it in a parent folder, and reference it like
this

```tex
\usepackage{../eecs}
```

## Sets / Probability

### Intersection / Union

```tex
$P(A \cap B)$
```

becomes $$P(A \cap B)$$

```tex
$P(\cup_{i=1}^n A_i)$
```

becomes $$P(\cup_{i=1}^n A_i)$$

### Complement

* `\overline` or `\complement`
* `$P(\overline{A})$` becomes $$P(\overline{A})$$
* `$P(A^\complement)$` becomes $$P(A^\complement)$$

### Set Subtraction

```tex
$A^\complement = \Omega \setminus A$
```

becomes $$A^\complement = \Omega \setminus A$$

### Subset

```tex
$A \subset B$ or $A \subseteq B$
```

becomes $$A \subset B$$ or $$A \subseteq B$$.

### Conditional Probability

```tex
$P(A \mid B)$
```

becomes $$P(A \mid B)$$

## Symbols in Distributions

### Sim

The squiggly `\sim` i.e. $$\sim$$

```tex
X_i \stackrel{iid}{\sim} U[0, 1]
```

becomes $$X_i \stackrel{iid}{\sim} U[0, 1]$$

### Choose / nCr

* Like found in binomial distribution formula
* `binom{n}{k}` becomes $$\binom{n}{k}$$

```tex
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
```

becomes $$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$

### Fancy Expectation

* `\mathbb{E}`
* Need the `amssymb` package.

```tex
$E[X]$ vs. $\mathbb{E}[X]$
```

* becomes $$E[X]$$ vs $$\mathbb{E}[X]$$.
* Use shortcut if you go with it

```tex
\newcommand{\E}{\mathbb{E}}
```

`\mathbb` is also used for things like

* Real Numbers: `\mathbb{R}^n` becomes $$\mathbb{R}^n$$
* Integers: `\mathbb{Z}^+` becomes $$\mathbb{Z}^+$$

### Fancy Normal

* `\mathcal{N}`
* Needs the 'amssymb' package.

```tex
$X \sim N(0,1)$ vs. $X \sim \mathcal{N}(0, 1)$
```

* becomes $$X \sim N(0,1)$$ vs. $$X \sim \mathcal{N}(0,1)$$
* Use shortcut if you go with it

```tex
\newcommand{\N}{\mathcal{N}}
```

`\mathcal` is also used for things like

* The set of values an RV can take i.e. `\mathcal{X}` or $$\mathcal{X}$$

  ```tex
  E[X] = \sum_{x \in \mathcal{X}} x \cdot P(X = x)
  ```

  becomes $$E[X] = \sum_{x \in \mathcal{X}} x \cdot P(X = x)$$.

### w.p.

```tex
\begin{equation}
  X =
  \begin{cases}
    1 & \text{w.p. $p$} \\
    0 & \text{w.p. $1-p$}
  \end{cases}
\end{equation}
```

* becomes $$\begin{equation} X = \begin{cases} 1 & \text{w.p. $p$} \\ 0 & \text{w.p. $1-p$} \end{cases} \end{equation}$$
* `&` symbols are used to separate columns, `\\` are used to make new lines

<!--
## Markov Chains

```tex
\begin{equation}
  P =
  \begin{bmatrix}
    1-p & p \\
    p & 1-p
  \end{bmatrix}
\end{equation}
```
* becomes $$P = \begin{equation} \begin{bmatrix} 1-p & p \\ p & 1-p \end{bmatrix} \end{equation}$$
* For graphing, you need the `tikzpicture` library.
```tex
\documentclass{article}
\usepackage{tikz}

\begin{center}
  \begin{tikzpicture}
    \node[state] 
  \end{tikzpicture}
\end{center}
-->