---
title: uniform distribution
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:36
tags:
  - probability/distribution/continuous
course:
  - STAB52
LEC: "5"
---
# definition
If uniform RV $X$ takes values in interval $[l,u], \forall l<u\in\mathbb{R}$, then any subinterval $(a,b)$ is proportional to its length $$P(a<X<b)=\frac{b-a}{u-l}, \forall l\leq a\leq b\leq u$$
Denoted $X\sim\mathrm{Uniform}(l,u)$
calculation using PDF: $f(x)=\begin{cases}\dfrac{1}{u-l},&l\leq x\leq u\\0,&\text{otherwise}\end{cases}$
calculation using CDF: $F(x)=\begin{cases}0,&x<l\\\dfrac{x-l}{u-l},&l\leq x\leq u\\1,&x>u\end{cases}$
