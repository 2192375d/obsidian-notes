---
title: permutation matrix
created: Sunday 24th August 2025 13:04
last_modified: Sunday 24th August 2025 13:04
aliases: []
tags:
  - math/linear-algebra/matrix
course: CSCC37
---
# permutation matrix
A __permutation matrix__ is a square matrix that has exactly one 1 on each row and column, and zero everywhere else.
e.g
$$
P=\begin{bmatrix}
0&0&1 \\
1&0&0 \\
0&1&0
\end{bmatrix}
$$
A permutation matrix is always nonsingular (note that $P^{-1}=P^T$)

Consider the system $APx=b$, we can solve the system by
$$
x=(AP)^{-1}b=P^{-1}A^{-1}b=P^T(A^{-1}b)
$$

Note that for a square matrix $A$, $AP$ is just $A$ with it's rows rearranged to an order based on $P$