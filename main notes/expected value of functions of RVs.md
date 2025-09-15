---
title: expected value of functions of RVs
created: Before 28th July, 2025
last_modified: Saturday 26th July 2025 13:23
tags:
  - probability/expected-value
course:
  - STAB52
LEC: 8
---
Let RV $Y=g(X)$, for some RV $X$, then
$$
E(Y)=\sum_{y}yp_{Y}(y)=\sum_{x}g(x)p_{X}(x)=E(g(X))
$$
(Same applies to multivariate function $Z=g(X,Y)$, where $X,Y$ are discrete)
$$
E(Z)=E[g(X,Y)]=\sum_{x}\sum_{y}g(x,y)p_{X,Y}(x,y)
$$
(Similarly, this works for continuous RVs)
_example_
Two processes run in parallel on two computers and they take i.i.d. $Geometric\left( \frac{1}{2} \right)$ times to complete.
Find the average time until it takes for both processes to complete
![[Drawing 2025-07-08 18.16.55.excalidraw]]


