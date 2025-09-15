---
title: probability density function (PDF)
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:34
tags:
  - probability/PDF
course:
  - STAB52
LEC: "5"
---
# definition 
For continuous RV $X$, its __PDF__ is a function $f(*)$ such that$$P(X\in[a,b])=\int_a^bf_X(x)dx$$
## PDF properties
- $0\leq f_X(x),\forall x\in\mathbb{R}$
- $\displaystyle \int_{-\infty}^{+\infty}f_X(x)\textrm{d}x=1$
- $\displaystyle F_X(x)=\int_{-\infty}^xf_X(u)\textrm{d}u\rightarrow f_X(x)=\frac{\textrm{d}}{\textrm{d}x}F_X(x)=F_X'(x)$       (PDF is CDF's derivative)