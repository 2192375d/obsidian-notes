---
title: properties of floating point system
created: Sunday 24th August 2025 00:55
last_modified: Sunday 24th August 2025 00:55
aliases: []
tags:
  - computer-science/floating-point-system
course: CSCC37
---
# properties of floating point system
The total number of normalalized floating point numbers is
$$
2(\beta-1)\beta^{t-1}(U-L+1)+1
$$
The smallest positive normalized floating point number is
$$
\text{underflow level}=\text{UFL}=\beta^L
$$
which has $1$ as the leading digit and 0 for the remeaning digits of the mantissa, and the smallest value possible for exponent

The largest positive normalized floating point number is
$$
\text{overflow level}=\text{OFL}=\beta^{U+1}(1-\beta^{-t})
$$
which has $\beta-1$ as the value of each digit of mantissa and largest possible value for the exponent
