---
title: expected value for continuous RV
created: Before 28th July, 2025
last_modified: Wednesday 9th July 2025 11:00
tags:
  - probability/expected-value
course:
  - STAB52
LEC: 8
---
# definition
For continuous RV $X$ with PDF $f_{X}(x)$, the expected value is given by
$$
E(X)=\int_{-\infty}^\infty xf_{X}(x)dx
$$
For function of multiple RVs $X,Y$ with joint PDF $f_{X,Y}(x,y)$, the expected value is given by
$$
E[g(X,Y)]=\int_{-\infty}^\infty\int_{-\infty}^\infty g(x,y)f_{X,Y}(x,y)dxdy
$$

Note that all properties of expectations hold in continuous case:
$$
\begin{align}
E(aX+bY)=aE(X)+bE(Y) \\
X\perp Y\to E(XY)=E(X)E(Y) 
\end{align}
$$

_example_
Find the expected value of the $Exponential(\lambda)$ distribution

_example_
