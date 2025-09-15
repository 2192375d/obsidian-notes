---
title: MGF (moment generated function)
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 15:09
tags:
  - probability/moment
course:
  - STAB52
LEC: 10
---
The __moment generating function__ (MGF) of RV $X$ is given by
$$
m(t)=E(e^{tX})
$$
Note that the function is well-defined when $m(t)$ is finite $\forall t<\epsilon$, for some $\epsilon>0$

MGF provides another way to characterize a distribution, by allowing calculation of all moments of $X$
$$
E(X^k)=m^{(k)}(0)= \frac{d^k}{dt^k}m(t)\text{ at t = 0}
$$
_example_
![[MGF (moment generated function 2025-07-15 14.33.53.excalidraw)]]

_example_
![[________________________-]]