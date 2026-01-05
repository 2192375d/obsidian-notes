---
title: floating-point rounding
created: Sunday 24th August 2025 12:31
last_modified: Sunday 24th August 2025 12:31
aliases: []
tags:
  - computer-science/floating-point-system
  - computer-science/approximation
course: CSCC37
---
# rounding
If a real number $x$ cannot be exactly representable as a floating point number, then it will be approximated by some nearby floating point number, denoted as $fl(x)$.

The process of choosing the $fl(x)$ is called __rounding__, and the error introduced by the approximation is called __rounding error__, or __roundoff error__

## chop and round to nearest
We have two most commonly used rounding rules:
- __chop__: The base $\beta$ expansion of $x$ is truncated after the $(t-1)$'th digit. We also call this __round to zero__
- __round to nearest__: $fl(x)$ is the closest floating point number to $x$; in case of a tie, we choose the number that is even. We also call this __round to even__

## relative error for chopping and rounding
[[truncation error and rounding error]]