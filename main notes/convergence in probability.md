---
title: types of convergence in probability field
created: Before 28th July, 2025
last_modified: Tuesday 22nd July 2025 15:37
tags:
  - probability/convergence
course:
  - STAB52
LEC: 11
---
# convergence in probability
Consider sequence of continuous RVs $X_{1},X_{2},\dots$ and RV $Y$, then
- $X_{n}$ __converges in probability__ to $Y$ if
$$
\lim_{ n \to \infty } P(|X_{n}-Y|\geq \epsilon)=0
$$
or
$$
\lim_{ n \to \infty } P(|X_{n}-Y|< \epsilon)=1
$$
, $\forall \epsilon>0$

Denoted $X_{n}\to^PY$
Used in WLLN, where $\overline{X}_{n}$ converges to constant $\mu$
Note that to calculate this probability, simply having the marginal distributions of $X$ only or $Y$ only won't help, we need both the joint distribution of $X$ and $Y$

This means, we need to find the probability of the following area
![[types of convergence in probability field 2025-07-22 15.31.26.excalidraw]]

, $\forall x\in\mathbb{R}$
- $X_{n}$ __converges in distribution__ to $Y$ if
$$
\lim_{ n \to \infty } P(X_{n}\leq x)=P(Y\leq x)
$$
Denoted $X_{n}\to^DY$

Note that if a sequence converges in probability, it converges in distribution.