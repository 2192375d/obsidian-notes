---
title: normal conditional expectated value
created: Before 28th July, 2025
last_modified: Thursday 10th July 2025 07:01
tags:
  - probability/distribution/continuous/normal
  - probability/conditional
  - probability/expected-value
course:
  - STAB52
LEC: 9
---
For __2D normal__, __conditional distribution__ is also __normal__
#### theorem
if $\begin{bmatrix}X \\ Y\end{bmatrix}\sim N\left(\mu=\begin{bmatrix}\mu_{X} \\ \mu_{Y}\end{bmatrix},\sigma=\begin{bmatrix}\sigma_{X}^2 &\sigma_{XY} \\ \sigma_{XY}&\sigma_{Y}^2\end{bmatrix}\right)$, then
$$
Y|(X=x)\sim N\left(\mu_{Y}+ \frac{\sigma_{XY}}{\sigma_{X}^2}(x-\mu_{X}),\sigma_{Y}^2-\frac{\sigma_{XY}}{\sigma_{X}^2}\right)
$$
Where the conditional expectations/variances for a normal are:
$$
\begin{align}
E(Y|X)=\mu_{Y}+\frac{\sigma_{XY}}{\sigma_{X}^2}(X-\mu_{X}) \\
V(Y|X)=\sigma_{Y}^2-\frac{\sigma_{XY}^2}{\sigma_{X}^2}
\end{align}
$$
