---
title: machine precision
created: Sunday 24th August 2025 12:40
last_modified: Sunday 24th August 2025 12:40
aliases: []
tags:
  - computer-science/approximation
course: CSCC37
---

# machine precision
The accuracy of a floating point system can be characterized by a quantity known as the __unit roundoff__/__machine precision__/__machine epsilon__, denoted as $\epsilon_{mach}$

For chopping,
$$
\epsilon_{mach}=\beta^{1-t}
$$

For rounding to nearest
$$
\epsilon_{mach}=\frac{1}{2}\beta^{1-t}
$$

This is important because it determines the maximum posible relative error of a real number $x$ in a floating point system
$$
\left|\frac{fl(x)-x}{x}\right|\leq \epsilon_{mach}
$$
Another way to see the unit roundoff is that $\epsilon_{mach}$ is the smallest epsilon S.T.
$$
fl(1+\epsilon)>1
$$

Note that in all practical floating point systems
$$
0<\text{UFL}<\epsilon_{mach}<\text{OFL}
$$