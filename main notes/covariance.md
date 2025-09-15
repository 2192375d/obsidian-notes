---
title: covariance
created: Before 28th July, 2025
last_modified: Saturday 26th July 2025 13:43
tags:
  - probability/variance
course:
  - STAB52
LEC: 8
---
# definition
Let $X,Y$ be RVs with means and variances $\begin{cases}\mu_{X}=E(X), \mu_{Y}=E(Y) \\ \sigma_{X}^2=V(X),\sigma^2_{Y}=V(Y)\end{cases}$
The covariance of $X$ and $Y$ is defined as
$$
Cov(X,Y)=E[(X-\mu_{X})(Y-\mu_{Y})]
$$
The correlation of $X$ and $Y$ is defined as
$$
\rho_{X,Y}= \frac{Cov(X,Y)}{\sigma_{X}\sigma_{Y}},p_{X,Y}\in[-1,1]
$$

Note that covariance can be negative
# covariance and linear dependence
Consider the joint distribution of RVs $X,Y$ is uniform over a disk centered at $(\mu_{X},\mu_{Y})$
![[Pasted image 20250703113925.png]]
if $Cov(X,Y)>0$, then on average $X \uparrow$ as $Y \uparrow$, and vice versa
if $Cov(X,Y)<0$, then on average $X \downarrow$ as $Y \uparrow$, and vice versa
![[Pasted image 20250703114134.png]]
