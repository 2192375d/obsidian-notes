---
title: conditional PMF
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:58
tags:
  - probability/conditional
  - probability/PMF
course: STAB52
LEC: 7
---

# quick recap
For discrete RVs $X,Y$, if $X,Y\in A$, then
$$
\forall s\in S, (X(s),Y(s))\in A
$$

# conditional PMF
For discrete RVs $X,Y$, the conditional probabilities can be found as 
$$
P((X,Y)\in A|(X,Y)\in B)=\sum_{{(x,y)\in A}}P(X=x,Y=y|(X,Y)\in B)
$$
where $$P(X=x,Y=y|(X,Y)\in B)=\frac{P(\{X=x,Y=y\}\cap\{(X,Y)\in B\})}{P((X,Y)\in B)}$$is the __conditional PMF__ of $X,Y$ given $(X,Y)\in B$

# conditioning PMF with one RV on a specific value
Usually, we condition on specifc value of one RV (e.g. $Y=y$) and look at probabilities of the other

For example, __conditional PMF__ of $X$ given $Y=y$ is:
$$p_{X|Y}(x|y)=P(X=x|Y=y)=\frac{P(X=x,Y=y)}{P(Y=y)}=\frac{p_{X,Y}(x,y)}{p_{Y}(y)}$$
(Note that this is just a univariate function)

# Requirement to be a Conditional PMF
Conditional PMF $p_{X|Y}(x|y)$ must be a __proper PDF__, which means the followings
- $\rho_{X|Y}(x|y)\geq 0$
- $\sum_{\forall x}\rho_{X|Y}(x|y)=1$
must be as satisfied 