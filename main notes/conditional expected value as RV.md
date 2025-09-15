---
title: conditional expected value as RV
created: Before 28th July, 2025
last_modified: Friday 18th July 2025 23:44
tags:
  - probability/expected-value
  - probability/conditional
course: STAB52
LEC: 9
---

# definition
For any value $X=x$, we can think of the conditional expectation $E(g(Y)|X=x)$ as a function

$$
h(x)=E(g(Y)|X=x)
$$
If $X$'s value is not specified, we can still define the conditional expectation as a function of X
$$
E[g(Y)|X]=h(X)
$$
(Essentially, $E[g(Y)|X]$ is a transformation of the RV $X$)

_example_
Consider RVs $X,Y$ uniformly distributed over area below:
![[Pasted image 20250708154044.png]]
The conditional expectation of $Y$ given $X$ is linear function of $X$ describing mean level of $Y$ based on $X$ (e.g. $E[Y|X]$ estimates $Y$ based on $X$)

This perspective is used in statistics (regression) for modeling behavior of $Y$ based on $X$
- e.g. Model average income $Y$ based on education level $X$.

_example_
For a take-out restaurant, define:
$X=\text{wait time to order}$
$Y=\text{total wait time}$	
Then, we get a joint PDF $f_{X,Y}(x,y)=\begin{cases}e^{-y},&0<x<y<\infty \\ 0,&o/w\end{cases}$
Find $E(X|Y)$ as a function of $Y$
- Consider $h(Y)=E(X|Y)$, where $h(Y)=e[X|Y=y],\forall y>0$
Then, ___boring___

