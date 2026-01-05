---
title: residual of solution
created: Thursday 28th August 2025 09:57
last_modified: Thursday 28th August 2025 09:57
aliases: []
tags:
  - computer-science/approximation
course: CSCC37
---
# solution residual
The __residual vector__ $r$ of an approximate solution $\hat{x}$ to the $n\times n$ linear system $Ax=b$ is defined as
$$
r=b-A \hat{x}
$$

If $A$ is nonsingular, then the error $||\hat{x}-x||=0$ iff $||r||=0$

# relative residual
If the computed solution $\hat{x}$ satisfies
$$
(A+E)\hat{x}=b
$$
We define __relative residual__ as
$$
\frac{||r||}{||A||\cdot||\hat{x}||}
$$

It is used in the inequality
$$
\frac{||r||}{||A||\cdot||\hat{x}||}\leq \frac{||E||}{||A||}
$$
This inequality is relating the __relative residual__ to the relative change in matrix.
Thus, a large relative residual implies a large backward error in the matrix, which means the algorithm used to compute the solution is unstable.