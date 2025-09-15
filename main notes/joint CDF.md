---
title: joint CDF
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:50
tags:
  - probability/CDF
  - probability/joint
course: STAB52
LEC: 6
---

We use joint CDF primarily for finding the area of a rectangular region ($X,Y$ are not bounded by each other)
To deal with non rectangular region, we use joint PDF instead
# joint CDF
Let $X,Y$ be RVs, joint CDF provides probabilities of type $$F_{X,Y}(x,y)=P(X\leq x,Y\leq y)=P(\{X\leq x\}\cap\{Y\leq y\})$$
Note that joint CDF can be used to find marginal CDFs
- $F_{X}(x)=\lim_{ y \to \infty }f_{X,Y}(x,y)=F_{X,Y}(x,\infty)$
- $F_{Y}(y)=\lim_{ x \to \infty }f_{X,Y}(x,y)=F_{X,Y}(\infty,y)$

You can find CDF by integrating PDF
- $\displaystyle F_{X,Y}(x,y)=\int_{-\infty}^x \int_{-\infty}^y f_{X,Y}(s,t)dtds,\forall x,y\in \mathbb{R}$

# joint CDF for product space
Consider $B=(x_{1},x_{2}]\times(y_{1},y_{2}])\subset \mathbb{R}$, using joint CDF, we can get
$$
\begin{align}
P((X,Y)\in B)&=P(x_{1}<X\leq x_{2},y_{1}<Y\leq y_{2}) \\
&=F_{X,Y}(x_{2},y_{2})-F_{X,Y}(x_{2},y_{1})-F_{X,Y}(x_{1},y_{2})+F_{X,Y}(x_{1},y_{1})
\end{align}
$$