---
title: polynomial interpolation
created: Thursday 28th August 2025 18:52
last_modified: Thursday 28th August 2025 18:52
aliases: []
tags:
  - computer-science/approximation
  - math/application/interpolation
course: CSCC37
---
# polynomial interpolation
Polynomial interpolation is the simplest and commonest type of interpolation that uses polynomials.

Consider when we have $n$ data points $(t_{i},y_{i}),1\leq i\leq n$, the interpolating polynomial is in form of
$$
p(t)=x_{0}+x_{1}t+\dots+x_{n-1}t^{n-1}
$$
Where it's coefficients are determined by the $n\times n$ linear system
$$
\begin{bmatrix}
1&t_{1}&\dots&t_{1}^{n-1} \\
1&t_{2}&\dots&t_{2}^{n-1} \\
\dots&\dots&\dots&\dots \\
1&t_{n}&\dots&t_{n{^{n-1}}}
\end{bmatrix}
\begin{bmatrix}
x_{0} \\
x_{1} \\
\dots \\
x_{n-1}
\end{bmatrix}
=
\begin{bmatrix}
y_{1} \\
y_{2} \\
\dots \\
y_{n}
\end{bmatrix}
$$

To find the polynomial, we just have to solve each $x$.

Note that polynomial interpolation is just inverse of polynomial evaluation. And finding such polynomial only requires $O(n^3)$ to work