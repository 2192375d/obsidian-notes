---
title: normal linear transformation
created: Before 28th July, 2025
last_modified: Thursday 10th July 2025 06:29
tags:
  - probability/distribution/continuous/normal
course:
  - STAB52
LEC: 9
---
__Linear transformations__ of any __joint normal__ are also __normal__
#### theorem
if $\begin{bmatrix}X \\ Y\end{bmatrix}\sim N\left(\mu=\begin{bmatrix}\mu_{X} \\ \mu_{Y}\end{bmatrix},\sigma=\begin{bmatrix}\sigma_{X}^2 &\sigma_{XY} \\ \sigma_{XY}&\sigma_{Y}^2\end{bmatrix}\right)$, then
$$
a+bX+cY\sim N(a+b\mu_{X}+c\mu_{Y},a^2\sigma_{X}^2+b^2\sigma_{Y}^2+2bc\sigma_{XY})
$$
Note that $a+b\mu_{X}+c\mu_{Y}=E(a+bX+cY),a^2\sigma_{X}^2+b^2\sigma_{Y}^2+2bc\sigma_{XY}=V(a+bX+cY)$

_example_
Assume weight of random person is Normal with $\mu=70kg$ and $\sigma=10kg$. If an elevator has $250kg$ capacity, find the probability that a random and independent group of 3 people cannot take it.

![[normal linear transformation 2025-07-10 06.14.23.excalidraw]]
