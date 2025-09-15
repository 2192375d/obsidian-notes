---
title: cumulative distribution function (CDF)
created: Before 28th July, 2025
last_modified: Thursday 17th July 2025 03:42
tags:
  - probability/CDF
course:
  - STAB52
LEC: "5"
---
# definition
distribution of any RV $X$ is determined by its CDF, defined as 
$$F_X(x)=P(X\leq x)=P({s\in S:X(s)\leq x}), \forall x\in\mathbb{R}$$
This is the probability of RV $X$ being less or equal to x, we also have
$$P(a<X\leq b) = P(\{X\leq b\}-\{X\leq a\}) = P(\{x\leq a\}\cap \{x\leq a\}^c)$$
## CDF properties
- $\displaystyle F_x(-\infty) \coloneqq\lim_{(x\rightarrow-\infty)}F_X(x)=0$ 
- $\displaystyle F_x(\infty) \coloneqq \lim_{(x\rightarrow\infty)}F_X(x)=1$
- $\forall x_1<x_2\in\mathbb{R}\rightarrow F_X(x_1)\leq F_X(x_2)$
Those follows directly from axioms of probability

<b>Note that if a function satisfies the above props, the function is a CDF (Used in proving a function is CDF</b>