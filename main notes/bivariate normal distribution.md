---
title: bivariate normal distribution
created: Before 28th July, 2025
last_modified: Friday 25th July 2025 09:44
tags:
  - probability/joint
  - probability/variance
  - probability/distribution/continuous/normal
course: STAB52
LEC: 6
---

# definition
The pdf of a bivariate normal is:
$$
f_{X,Y}(x,y)=\frac{1}{\sqrt{(2\pi)^2\begin{vmatrix}\sigma_{X}^2 & \sigma_{X,Y} \\
\sigma_{X,Y} & \sigma_{Y}^2
\end{vmatrix}}}e^{{{-\frac{1}{2}}\begin{bmatrix}
x-\mu_{X} \\
y-\mu_{Y}
\end{bmatrix}^T\begin{bmatrix}
\sigma_{X}^2&\sigma_{X,Y} \\
\sigma_{X,Y}&\sigma_{Y}^2
\end{bmatrix}^{-1}\begin{bmatrix}
x-\mu_{X} \\
y-\mu_{Y}
\end{bmatrix}}}, \forall x,y\in\mathbb{R}
$$
Note that the term before $e$ is just a constant, while the power of $e$ is a $-\frac{1}{2}$ times a quadratic function.
