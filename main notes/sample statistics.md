---
title: sample statistics
created: Tuesday 29th July 2025 15:42
last_modified: Tuesday 29th July 2025 15:42
tags:
  - probability/application
course:
  - STAB52
LEC: 12
aliases:
  - sample mean
---
# sample statistics
__Statistical analysis__ relies on probability model for sample data.
- We assume sample data are i.i.d. RVs from "population" distribution.
$$
X_{1},X_{2},\dots,X_{n}\sim^{i.i.d}F_{X}(x)
$$
__Sample Statistics__ are functions (literally just transformations) of sample data, related to model parameters.
- e.g. __sample mean__:
$$
\overline{X}_{n}=\frac{1}{n}(X_{1}+\dots+X_{n})=\frac{1}{n} \sum_{i=1}^nX_{i}
$$
(literally the same as average...?)

# sample distribution
Sample statistics can be used to estimate model parameters
- E.g. We know that $\overline{X}\to^P\mu$ as $n\to \infty$ (by WLLN)
- But how accurate is estimation for finite $n$?

Using sample mean, we get
$$
\overline{X}_{n}\sim Normal\left( \mu, \frac{\sigma^2}{n} \right) \text{ by CLT}
$$
Thus, the accuracy of estimation improves with sample size $n$ at rate $\displaystyle\frac{1}{\sqrt{ n }}$