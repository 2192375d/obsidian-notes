---
title: truncation error and rounding error
created: Friday 22nd August 2025 23:18
last_modified: Friday 22nd August 2025 23:18
aliases: []
tags:
  - computer-science/approximation/error
course: CSCC37
---

The computational error can be broken down as __truncation error__ and __computational error__
# truncation error
Truncation error occurs when a computation with $N$ or $\infty$ terms is done performed by only dealing with a $N_{0}<N<\infty$ terms. This often happens when dealing with infinite series, integrals, or replacing an arbitrary function by a polynomial

An example of this is that approximating $e^x$ using only the first 3 terms, we will get $\displaystyle e^x\approx1+x+\frac{x^2}{2}$, thus, the truncation error will be $\displaystyle e^x-1-x-\frac{x^2}{2}=\frac{x^3}{3!}+\frac{x^4}{4!}+\frac{x^5}{5!}+\dots$

# rounding error
title