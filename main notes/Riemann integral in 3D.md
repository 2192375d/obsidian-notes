---
title: Riemann integral in 3D
created: Monday 11th August 2025 14:01
last_modified: Tuesday 29th July 2025 00:44
aliases: 
tags:
  - calculus/integral/riemann-sum
  - calculus/multivariable
course:
  - MATB41
---
Let $B=[a,b]\times[c,d]\times[p,q]$ be a rectangular prism, $f:B\to\mathbb{R}$ be a bounded function, then we define the __Riemann sum__ as
$$
S_{n}=\sum_{i,j,k=0}^{n-1}f(c_{ijk})\Delta x\Delta y\Delta z
$$
If $\lim_{ n \to \infty }S_{n}$ exists and is independent of the choice of $c_{ijk}$, then we say $f$ is __integrable__ on $B$ and define the __triple integral__ of $f$ over $B$ as the limit of the Riemann sums:
$$
\iiint_{B}fdV=\lim_{ n \to \infty } S_{n}=\sum_{i,j,k=0}^{n-1}f(c_{ijk})\Delta x\Delta y\Delta z
$$