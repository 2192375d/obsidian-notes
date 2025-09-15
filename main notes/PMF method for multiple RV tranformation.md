---
title: PMF method for multiple RV tranformation
created: Before 28th July, 2025
last_modified: Monday 7th July 2025 01:03
tags:
  - probability/PMF
  - probability/method
course: STAB52
LEC: 7
---
For discrete RVs $X,Y$, with joint PMF $p_{X,Y}(x,y)$, we calculate joint PMF of $Z=h_{1}(X,Y)$,$W=h_{2}(X,Y)$ as
$$
p_{Z,W}(z,w)=P(Z=z,W=w)=\sum_{(x,y)\in h^{-1}(z,w)}p_{X,Y}(x,y)
$$
