---
title: double integral over elementary regions
created: Monday 11th August 2025 14:00
last_modified: Tuesday 29th July 2025 00:44
aliases: 
tags:
  - calculus/integral
  - calculus/multivariable
course:
  - MATB41
---
Let $D$ be an elementary region in the plane, for any rectangle $R$ that contains $D$.
Then, for $f:D\to \mathbb{R}$ continuous on $D$, we define
$$
\iint_{D}f(x,y)dA=\iint_{R}f^*(x,y)dA
$$
where
$$
f^*(x,y)=\begin{cases}
f(x,y),&(x,y)\in D \\
0,&(x,y)\in R/D
\end{cases}
$$
