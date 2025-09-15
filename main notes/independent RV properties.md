---
title: independent RV properties
created: Before 28th July, 2025
last_modified: Thursday 17th July 2025 11:34
tags:
  - probability/independence
course:
  - STAB52
LEC: 7
---
Let $X,Y$ be independent RVs, then their corresponding CDF/PMF/PDF factorizations are:
$$
X\perp Y\leftrightarrow\begin{cases}
F_{X,Y}(x,y)=F_{X}(x)F_{Y}(y) & \text{ (any functions)} \\
f_{X,Y}(x,y)=f_{X}(x)f_{Y}(y) & \text{ (continuous functions only)} \\
p_{X,Y}(x,y)=p_{X}(x)p_{Y}(y) & \text{ (for discontinuous functions)} \\
\end{cases}
$$