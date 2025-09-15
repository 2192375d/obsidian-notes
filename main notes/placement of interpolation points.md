---
title: placement of interpolation points
created: Saturday 30th August 2025 17:22
last_modified: Saturday 30th August 2025 17:22
aliases: []
tags:
  - math/application/interpolation
course: CSCC37
---
Polynomial interpolation for functions of large degree can work, but it usually "diverges" a little bit near the two ends (near $t_{1}$ and $t_{n}$). Thus, we need to consider the placement of interpolation points

# placement of interpolation points (Chebyshev points)
One way to deal with the problem above is by placing the points following the __Chebyshev points__
$$
t_{k}=-\cos\left( \frac{(2k-1)\pi}{2n} \right),k=1,\dots,n
$$
On the interval $[-1,1]$, or a suitable transformation of it for any interval