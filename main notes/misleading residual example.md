---
title: misleading residual example
created: Monday 20th October 2025 16:31
last_modified: Monday 20th October 2025 16:31
aliases: []
tags:
  - computer-science/approximation/error
course:
  - CSCC37
LEC:
  - "6"
---
# some example
Does that mean $\displaystyle \frac{||\hat{x}-x||}{||x||}$ is small?
Since we donnot know what $x$ is, we cannot directly calculate the relative error.

Consider
$$
\begin{bmatrix}
0.780&0.563 \\
0.913&0.659
\end{bmatrix}x=\begin{bmatrix}
0.217 \\
0.254
\end{bmatrix}
$$
From this, we can get two computed solutions:
$$
\hat{x}_{\alpha}=
\begin{bmatrix}
0.999 \\
-1.001
\end{bmatrix},
\hat{x}_{\beta}=\begin{bmatrix}
0.341 \\
-0.087
\end{bmatrix}
$$
To tell which one is the better solution, the best thing to do is by directly calculating the two residuals
$$
\begin{align}
r_{\alpha}&=b-A\hat{x}_{\alpha} =\begin{bmatrix}
-0.001243 \\
-0.001572
\end{bmatrix} \\
r_{\beta}&=b-A\hat{x}_{\beta}=\begin{bmatrix}
-0.000001 \\
0
\end{bmatrix}
\end{align}
$$
Note that clearly, using $\hat{x}_{\beta}$, we get a much smaller residual, which indicates $\hat{x}_{\beta}$ is the better solution

(Note that the "true" solution is $x=\begin{bmatrix}1 \\ -1\end{bmatrix}$)
Which indicates clearly, the above solution is wrong. Thus, residuals are __NOT__ a clear indication of which solution is better when __residuals are very very small__.

We need to figure out what is the relationship between $\displaystyle \frac{||r||}{||b||}$ and $\displaystyle\frac{||x-\hat{x}||}{||x||}$