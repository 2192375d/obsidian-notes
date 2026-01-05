---
title: Jordan canonical form
created: Friday 12th December 2025 21:39
last_modified: Friday 12th December 2025 21:39
aliases:
  - block diagonal matrix
tags:
  - math/linear-algebra/Jordan
course:
  - MATB24
LEC:
  - "12"
---
# block diagonal matrix
A square matrix $A$ is a __block diagonal matrix__ if $A$ has form
$$
A=\begin{bmatrix}
A_{1}&O&O&\dots&O \\
O&A_{2}&O&\dots&O \\
O&O&A_{3}&\dots&O \\
\vdots&\vdots&\vdots&\ddots&\vdots \\
O&O&O&\dots &A_{k}
\end{bmatrix}
$$
where each $A_{i}$  is a square matrix and the diagonal of each $A_{i}$ is on the diagonal of $A$, and $O$ is a zero matrix of apprioate size.

For example
![[Pasted image 20251212214354.png]]

# Jordan block
A __Jordan block__ $J_{i}$ with value $\lambda$ is a square upper triangular matrix whose entries are all $\lambda$ on the diagonal, all $1$ imeediately above diagonal and $0$ elsewhere

Denoted as $J_{i}=[\lambda]$
where
$$
J_{i}=\begin{bmatrix}
\lambda&1&0&\dots&0&0 \\
0&\lambda&1&\dots&0&0 \\
\vdots&\vdots&\vdots&\ddots&\vdots&\vdots \\
0&0&0&\dots&\lambda&1 \\
0&0&0&\dots&0&\lambda
\end{bmatrix}
$$