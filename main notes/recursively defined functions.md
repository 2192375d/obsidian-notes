---
title: recursively defined functions
created: Wednesday 10th September 2025 04:11
last_modified: Wednesday 10th September 2025 04:11
aliases: []
tags:
  - math/set-theory/function/recursion
---
# Principle of function definition by recursion
Let $b\in\mathbb{Z}$ and $g:\mathbb{N}\times\mathbb{Z}\to\mathbb{Z}$ be a function, then there is an unique function $f:\mathbb{N}\to\mathbb{Z}$ that satisfies the following equation
$$
f(n)=
\begin{cases}
b,&n=0 \\
g(n,f(n-1)),&n>0
\end{cases}
$$
Here, $f$ is defined based on simple induction

# Principle of function definition by complete recursion
Let:
- $k,l$ be positive integers, 
- $b_{0},b_{1},\dots,b_{k-1}$ be arbitrary integers, 
- $h_{1},h_{2},\dots,h_{l}:\mathbb{N}\to\mathbb{N}$ be function such that $h_{i}(n)<n$ for each $1\leq i\leq l$ and $n\geq k$
- $g:\mathbb{N}\times\mathbb{Z}^l\to\mathbb{Z}$ be a function
Then, there is a unique function $f:\mathbb{N}\to\mathbb{Z}$ that satisfies
$$
f(n)=
\begin{cases}
b_{n},&0\leq n<k \\
g(n,f(h_{1}(n)),f(h_{2}(n)),\dots,f(h_{l}(n))),&n\geq k
\end{cases}
$$

Functions that fit this pattern is called __recurrence equation__/__recurrence relation__/__recurrences__
_example_
Consider $F:\mathbb{N}\to\mathbb{N}$ defined as
$$
F(n)=
\begin{cases}
0,&n=0 \\
1,&n=1 \\
f(n-1)+F(n-2),&n>1
\end{cases}
$$
(This is just the Fibonacci sequence)

Here $F$ is defined using complete induction