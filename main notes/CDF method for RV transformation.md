---
title: CDF method for RV transformation
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:46
tags:
  - probability/method
  - probability/CDF
course: STAB52
LEC: 6
---

# CDF method
Consider when you are only looking for the distribution of form $A=(-\infty,y],y\in\mathbb{R}$
For any continuous injective function $h$, inserse image is also half-lline. Which means we can use CDF of $X$ to find CDF of $Y$

ex: if h is strictly increasing, then$$
	\begin{align}
	F_Y(y)&=P(Y\leq y) \\ 
	&=P(X\in h^{-1}(-\infty,y]) \\
	&=P(X\in(-\infty,h^{-1}(y)]) \\
	&=P(X\leq h^{-1}(y)) \\
	&=F_X(h^{-1}(y))
	\end{align}
	$$

_example_
Let RV $U\sim Uniform(0,1)$ and find CDF of $X=-log(1-U)$
	$$P(U\leq u)=F_U(u)=\begin{cases}0,&u<0\\u,&0\leq u<1\\1,&u>1\end{cases}$$
	then, 
$$\begin{align}F_X(x)&=
P(X\leq x) \\
&=P(-log(1-U)\leq x) \\
&=P(log(1-U)\geq -x) \\
&=P(U\geq 1-10^{-x}) \\
&=F_U(1-10^{-x})\end{align}$$	
	$\forall x\in(0,\infty)$
	Note that this is CDF of $Exp(\lambda=1)$, if we have $10$ instead of $e$ as base