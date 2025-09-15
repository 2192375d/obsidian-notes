---
title: interpolating a function
created: Saturday 30th August 2025 17:03
last_modified: Saturday 30th August 2025 17:03
aliases: []
tags:
  - math/application/interpolation
course: CSCC37
---
# polynomial interpolation for function
Consider interpolating sufficiently smooth function $f$ at $n$ points $t_{1},\dots,t_{n}$ and $\theta$ is some unknown point in $[t_{1},t_{n}]$
One way to do __polynomial interpolation__ is by using a polynomial $p_{n-1}$:
$$
f(t)-p_{n-1}(t)= \frac{f^{(n)}(\theta)}{n!}(t-t_{1})(t-t_{2})\dots(t-t_{n})
$$
Since $\theta$ is unknown, this is kind of useless unless we have a bound on the appropriate derivative of $f$

Another form of polynomial interpolation is done using a truncated Taylor series
$$
p_{n}(t)=f(a)+f'(a)(t-a)+\frac{f''(a)}{2}(t-a)^2+\dots+\frac{f^{(n)}(a)}{n!}(t-a)^n
$$

