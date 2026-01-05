---
title: condition of matrix
created: Wednesday 27th August 2025 13:35
last_modified: Wednesday 27th August 2025 13:35
aliases: []
tags:
  - math/linear-algebra/matrix
  - computer-science/approximation
course: CSCC37
---
# condition of matrix
The __condition number__ of a square nonsingular matrix $A$ with respect to a give norm is defined as
$$
cond(A)=||A||\cdot||A^{-1}||
$$

For singular matrix $A$, we define the __condition number__ as $cond(A)=\infty$ since
$$
||A||\cdot||A^{-1}||=\left(\max_{x\neq 0} \frac{||Ax||}{||x||}\right)\cdot\left(\min_{x\neq 0} \frac{||Ax||}{||x||}\right)^{-1}
$$
## purpose of matrix condition
purposes of matrix condition
- indicate how close matrix is to been singular
- indicate how accurate the relative residual indicates the relative error

### relative residual part
note that $1=||I||=||AA^{-1}||\leq ||A|| \ ||A^{-1}||=cond(A)$
If $cond(A)$ is very large, then the problem is __poorly conditioned__ and small relative residual does not necessarily mean a small relative error
if $cond(A)$ is not too large then the problem is __well conditioned__ and a small relative residual is a reliable indicator of small relative error

### singular part

Condition number of a matrix measures how close a matrix is been singular, where the large the condition, the closer the matrix is to singular.

Note that the determinant does NOT indicate how close the matrix is to been singular. E.g. a very non-singular matrix can have a nearly $0$ determinantj



## compute matrix condition
To compute matrix condition, $||A||$ can be computed easily,  but $||A^{-1}||$ is challenging to do so.
Hence, instead, we take advantage of matrix norm properties
$$
\text{if }Az=y,\text{ then }\frac{||x||}{||y||}\leq||A^{-1}||
$$
We want to pick a $y$ S.T. $\displaystyle \frac{||x||}{||y||}$ has the largest ratio possible. A cheap way of doing this is to choose $y$ from the system $A^{T}y=c$ where $c$ is a vector with component vectors $\pm1$

## 2-matrix condition
From what's in matrix norm ([[matrix norms]]), for orthogonal $A$, $||A||_{2}= ||A^{-1}||_{2}=1$
Thus, $cond_{2}(A)=1$, and similarly,
$$
\frac{||x-\hat{x}||_{2}}{||x||_{2}}\leq cond_{2}(A) \frac{||r||_{2}}{||b||_{2}}=\frac{||r||_{2}}{||b||_{2}}
$$
Thus, relative residual is the upper bound for relative error ofr a perfectly well conditioned problem