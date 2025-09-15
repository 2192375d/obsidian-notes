---
title: Hessian matrix
created: Tuesday 12th August 2025 01:45
last_modified: Tuesday 12th August 2025 01:45
aliases: 
tags:
  - calculus/derivative
  - calculus/multivariable
  - math/linear-algebra/matrix
course:
  - MATB41
---
# Hessian matrix
Let $f:U\to\mathbb{R}$ be a function with second-order continuous derivatives $\displaystyle\left(\frac{\partial^2f}{\partial x_{i}\partial x_{j}}\right)(x_{0})$ at $x_{0}\in U$, then __Hessian__ of $f$ at $x_{0}$ is the quadratic defined by
$$
\begin{align}
Hf(x_{0})(h)&=\frac{1}{2}\sum_{i,j=1}^n \frac{\partial^2f}{\partial x_{i}\partial x_{j}}(x_{0})h_{i}h_{j} \\
&=\frac{1}{2}[h_{1},\dots,h_{n}]
\begin{bmatrix}
\frac{\partial^2f}{\partial x_{1}\partial x_{1}} &\dots &\frac{\partial^2f}{\partial x_{1}\partial x_{n}} \\
\dots & & \dots \\
\frac{\partial^2f}{\partial x_{n}\partial x_{1}} &\dots &\frac{\partial^2f}{\partial x_{n}\partial x_{n}} \\
\end{bmatrix} 
\begin{bmatrix}
h_{1} \\
\dots \\
h_{n}
\end{bmatrix}
\end{align}
$$