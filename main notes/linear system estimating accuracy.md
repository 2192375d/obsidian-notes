---
title: linear system estimating accuracy
created: Thursday 28th August 2025 10:11
last_modified: Thursday 28th August 2025 10:11
aliases: []
tags:
  - computer-science/approximation
  - math/linear-algebra/matrix
course: CSCC37
---

# estimating accuracy
To find the relative accuracy of a linear system $Ax=b$, where the solution achieved is $\hat{x}$
we make use of condition to bound the relative error of solution $\hat{x}$, with $A \hat{x}=\hat{b}$
$$
\frac{||\hat{x}-x||}{||x||}\leq cond(A)\frac{||\hat{b}-b||}{||b||}
$$

A similar result holds if $Ax=b$ and $(A+E)\hat{x}=b$
$$
\frac{||\hat{x}-x||}{||x||}\leq cond(A)\frac{||E||}{||A||}
$$

(to be proven...)
