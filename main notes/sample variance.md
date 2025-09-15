---
title: sample variance
created: Wednesday 30th July 2025 12:00
last_modified: Wednesday 30th July 2025 12:00
tags:
  - probability/variance
  - probability/application
course:
  - STAB52
LEC: 12
---
When using CLT, the accuracy of $\overline{X}_{n}$ relies on variance $\sigma^2$, but often times, the variance is unknown and also must be estimated

We can estimate $\sigma^2$ by __sample variance__
$$
S_{n}^2=\frac{1}{n-1}\sum_{i=1}^n(X_{i}-\overline{X}_{n})
$$