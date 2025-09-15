---
title: marginal distribution of multivariate normal
created: Before 28th July, 2025
last_modified: Wednesday 9th July 2025 11:09
tags:
  - probability/marginal
  - probability/distribution/continuous/normal
course: STAB52
LEC: 9
---

Normal distribution has some very important properties
1. marginal distributions of multivariate normal are normal
2. linear transformations of normal RVs are normal
3. conditional distributions of multivariate normal are normal

Marginal distributions for any joint normal are also normal
$$
\begin{bmatrix}
X \\
Y
\end{bmatrix}\sim N\left(\mu=\begin{bmatrix}
\mu_{X} \\
\mu_{Y}
\end{bmatrix},
\sigma=\begin{bmatrix}
\sigma_{X}^2 &\sigma_{X,Y} \\
\sigma_{X,Y} &\sigma_{Y}^2
\end{bmatrix}
\right)
\begin{matrix}
\to X\sim N(\mu_{X},\sigma_{X}^2) \\
\to Y\sim N(\mu_{Y},\sigma_{Y}^2)
\end{matrix}
$$