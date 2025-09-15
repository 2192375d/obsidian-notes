---
title: variance and covariance properties
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:15
tags:
  - probability/variance
course:
  - STAB52
LEC: 8
---
# theorem 
- $Cov(X,X)=V(X)$
- $Cov(X,Y)=E(XY)-\mu_{X}\mu_{Y}$
- $V(X+Y)=V(X)+V(Y)+2Cov(X,Y)$
- if $X\perp Y$, then $Cov(X,Y)=0$ (note that the converse is not the case, from the uniform disk example)
- $V(aX)=a^2V(X)$

# theorem
Covariance is linear
$$\displaystyle Cov\left( \sum_{i=1}^n a_{i}X_{i},\sum_{j=1}^mb_{j}Y_{j}\right)=\sum_{i=1}^n\sum_{j=1}^ma_{i}b_{j}Cov(X_{i},Y_{j})$$
However, note that variance is not linear.
_example_
Two processes run serially w/i.i.d $Geometric(0.5)$ times
- Find the variance of the time until both complete
	$E(X+Y)=E(X)+E(Y)=2+2=4$

