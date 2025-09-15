---
title: marginal PDF
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:51
tags:
  - probability/PDF
  - probability/marginal
course: STAB52
LEC: 6
---

# marginal PDF
For RVs $X,Y$, with joint PDF $f_{X,Y}$, the __marginal PDF__ is of $X$ and $Y$ are given by
- $\displaystyle f_{X}(x)=\int_{-\infty}^\infty f_{X,Y}(x,y)dy$
- $\displaystyle f_{Y}(y)=\int_{-\infty}^\infty f_{X,Y}(x,y)dx$

if we restrict $x,y\in[a,b]$, then this will be
- $\displaystyle f_{X}(x)=\int_{x}^{b}f_{X,Y}(x,y)dy$
- $\displaystyle f_{Y}(y)=\int_{y}^{b}f_{X,Y}(x,y)dx$
