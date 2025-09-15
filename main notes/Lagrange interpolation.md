---
title: Lagrange interpolation
created: Friday 29th August 2025 01:42
last_modified: Friday 29th August 2025 01:42
aliases: []
tags: []
course: CSCC37
---
# Lagrange interpolation
Consider a set of data points $(t_{i},y_{i}),1\leq i\leq n$, the __Lagrange basis functions__ are given by
$$
l_{j}(t)= \frac{\Pi_{k=1,k\neq j}^n(t-t_{k})}{\Pi_{k=1,k\neq j}^n(t_{j}-t_{k})}
$$
Note that the Lagrange basis functions are continuous functions that satisfy:
$$
l_{j}(t_{i})=\begin{cases}
1,i=j \\
0,i\neq j
\end{cases}
$$
The interpolating polynomial end up been
$$
p(t)=y_{1}l_{1}(t)+\dots+y_{n}l_{n}(t)
$$