---
title: Monte Carlo integration
created: Tuesday 29th July 2025 01:52
last_modified: Tuesday 29th July 2025 01:52
tags:
  - probability/method
  - theorem
course:
  - STAB52
LEC: 12
---

Consider approximating a converging integral $\displaystyle\int_{a}^bg(x)dx$,
If you simulate i.i.d. RVs $X_{i}\in(a,b)$ with PDF $f_{X}(x)>0,\forall x\in(a,b)$, then you can approximate the integral by
$$
\int_{a}^bg(x)dx\approx M_{n}=\frac{1}{n}\sum_{i=1}^n \frac{g(X_{i})}{f(X_{i})}
$$
## proof
![[Monte Carlo integration 2025-07-29 15.10.46.excalidraw]]