---
title: Riemann integral in 2D
created: Monday 11th August 2025 13:58
last_modified: Tuesday 29th July 2025 00:44
aliases: 
tags:
  - calculus/multivariable
  - calculus/integral/riemann-sum
course:
  - MATB41
---
# definition
Let $R=[a,b]\times[c,d]$ be a rectangle and $f:R\to \mathbb{R}$. Consider partitions $\{ x_{i} \}_{i=0}^n$$\{ y_{i} \}_{i=0}^n$ , where $x_{0}=a,x_{n}=b,y_{0}=c,y_{n}=d$, 
Let $R_{i,j}$ be rectangle $[x_{i},x_{i+1}]\times[y_{i},y_{i+1}]$, and let $\mathbf{c}_{i,j}$ be any point in $R_{i,j}$.
Then, the __double integral__ of $f$ over rectangle $R$ is defined as
$$
\iint_{R}f(x,y)dA=\lim_{ n \to \infty }\sum_{i,j=0}^{n-1}f(\mathbf{c}_{i,j})\Delta x\Delta y
$$
If the limit above exists and is constant for any $\mathbf{c}_{i,j}$, then $f$ is __integrable__ over the rectangle $R$.

The set of points $\{ \mathbf{c}_{i,j} \}_{i,j=0}^n$ is called a set of __sample points__

_example_
Integrate $\iint_{R}(2x+3y)dxdy$ where $R=[0,1]\times[0,1]$ using a two-dimensional Riemann sum with lower-left corner sample points.