---
title: data error and computational error
created: Friday 22nd August 2025 23:12
last_modified: Friday 22nd August 2025 23:12
aliases: []
tags:
  - computer-science/approximation/error
course: CSCC37
---
# total error, data error and computational error
Consider an input data $x$, who's desired result is $f(x)$ for some $f:\mathbb{R}\to\mathbb{R}$.
Suppose that we must work with an inexact input $\hat{x}$, with corresponding function $\hat{f}$, then
$$
\begin{align}
\text{Total error}&=\hat{f}(\hat{x})-f(x) \\
&=(\hat{f}(\hat{x})-f(\hat{x}))&+&&(f(\hat{x})-f(x)) \\
&=\text{computational error}&+&&\text{propagated data error}
\end{align}
$$
