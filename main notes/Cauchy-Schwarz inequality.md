---
title: Cauchy-Schwarz inequality
created: Before 28th July, 2025
last_modified: Tuesday 22nd July 2025 13:08
tags:
  - probability/moment/inequality
  - theorem
  - math/linear-algebra
course:
  - STAB52
LEC: 10
---
# Cauchy-Schwarz inequality (probability)
Let $X,Y$ be RVs, then the expectation of their product is the geometric average of their 2nd moments
$$
|E(XY)|\leq \sqrt{ E(X^2)E(Y^2) }
$$

This can be used to find the covariance of RVs:
Let $X'=X-\mu_{X}$ and $Y'=Y-\mu_{Y}$, then, by __Cauchy-Schwarz inequality__, 
$$
|Cov(X,Y)|\leq \sqrt{ V(X)V(Y) }
$$
we can also calculate the correlation $\rho_{XY}$ using this:
$$
\rho_{XY}=\frac{Cov(X,Y)}{\sqrt{ V(X)V(Y) }}
$$
, ranges in $[-1,1]$

# Cauchy-Schwarz inequality (linear algebra)
Let $V$ be an inner product space and let $\mathbf{v},\mathbf{w}\in V$, then $|\langle \mathbf{v},\mathbf{w}\rangle|\leq ||\mathbf{v}||||\mathbf{w}||$