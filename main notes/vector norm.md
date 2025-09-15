---
title: vector norms
created: Monday 25th August 2025 01:28
last_modified: Monday 25th August 2025 01:28
aliases: []
tags:
  - math/linear-algebra/norm
course: CSCC37
---
# vector norm
For an integer $p>0$, the __norm__ of vector $x$ of dimension $n$ is defined by
$$
||x||_{p}=\left(\sum_{i=1}^n|x_{i}|^p\right)^{1/p}
$$

Note that $2$-norm is the dot product of the vector with itself
$$
||x||_{2}=\left(\sum_{i=1}^n|x_{i}|^2\right)^{1/2}
$$
We also have $\infty$-norm
$$
||x||_{\infty}=\max_{1\leq i\leq n}|x_{i}|
$$

We use $1$-norm or $\infty$-norm to analyze the sensitivty of solutions of ilnear systems.