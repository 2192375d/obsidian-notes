---
title: PDF method for multiple RV transformation
created: Before 28th July, 2025
last_modified: Monday 7th July 2025 01:13
tags:
  - probability/PDF
  - probability/method
course:
  - STAB52
LEC: 7
---
# PDF method
For X,Y with joint PDF $f_{X,Y}(x,y)$ and differentiable 1-to-1 transform $(Z,W)=h(X,Y)$, the joint PDF of $(Z,W)$ is given by
$$
f_{Z,W}(z,w)=\frac{f_{X,Y}(h^{-1}(z,w))}{|J(h^{-1}(z,w))|}
$$
where $J(x,y)$ is absolute Jacobian of $h$:
$$
J(x,y)=\begin{bmatrix}
\frac{\partial h_{1}(x,y)}{\partial x} & \frac{\partial h_{1}(x,y)}{\partial y}  \\
\frac{\partial h_{2}(x,y)}{\partial x} & \frac{\partial h_{2}(x,y)}{\partial y}  \\
\end{bmatrix}
$$
