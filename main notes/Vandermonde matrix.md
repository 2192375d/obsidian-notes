---
title: Vandermonde matrix
created: Thursday 18th September 2025 22:54
last_modified: Thursday 18th September 2025 22:54
aliases: []
tags:
  - math/linear-algebra/matrix
---
# Vandermonde matrix
Vandermonde matrix is a matrix of form
$$
V=\begin{bmatrix}
1&a_{0}&a_{0}^2&\dots&a_{0}^n \\
1&a_{1}&a_{1}^2&\dots&a_{1}^n \\
\vdots&\vdots&\vdots&\ddots&\vdots \\
1&a_{m}&a_{m}^2&\dots&a_{m}^n
\end{bmatrix}
$$
## Vandermonde matrix properties
The Vandermonde matrix' determinant is nonzero iff $a_{0}\neq a_{1}\neq \dots\neq a_{m}$, in other words, for the Vandermonde to have trivial solutions only, all $a$'s must be different values.