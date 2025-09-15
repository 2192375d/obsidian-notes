---
title: multiple integral properties
created: Monday 11th August 2025 13:59
last_modified: Tuesday 29th July 2025 00:44
aliases: 
tags:
  - calculus/multivariable
  - theorem
  - calculus/integral
course:
  - MATB41
---
Let $f,g$ be functions integrable on rectangle $R$, then they follow:
- linearity
$$
\iint_{R}af(x,y)+bg(x,y)dA=a\iint_{R}f(x,y)dA+b\iint g(x,y)dA
$$
- monotonicity
if $f(x,y)\geq g(x,y)$, then
$$
\iint_{R}f(x,y)dA\geq \iint_{R}g(x,y)dA
$$
- additivity
Supposed that $R$ is the disjoint union of finitely many rectangles $\displaystyle R=\bigcup_{i=1}^n\iint_{R_{i}}f(x,y)dA$, then
$$
\iint_{R}f(x,y)dA=\sum_{i=1}^n\iint_{R_{i}}f(x,y)dA
$$
