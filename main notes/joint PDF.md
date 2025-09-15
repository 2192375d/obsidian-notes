---
title: joint PDF
created: Before 28th July, 2025
last_modified: Wednesday 16th July 2025 10:34
tags:
  - probability/joint
  - probability/PDF
course: STAB52
LEC: 6
---

# definition
Let $X,Y$ be continuous RVs, then the __joint PDF__ is a function $f_{X,Y}(x,y)$ S.T.
$$
P((X,Y)\in \mathbb{R})=\iint_{\mathbb{R}^2}f_{X,Y}(x,y)dxdy
$$
(Same applies when you have $\geq 3$ RVs)

You can find __joint PDF__ using joint CDF via partial derivatives:
$$
f_{X,Y}(x,y)=\frac{\partial^2}{\partial x\partial y}F_{X,Y}(x,y)
$$

# joint PDF properties
- $\forall x,y\in \mathbb{R},f_{X,Y}(x,y)\geq 0$
- $\displaystyle\int\int_{\mathbb{R}^2}f_{X,Y}(x,y)dxdy$
