---
title: floating point numbers
created: Sunday 24th August 2025 00:32
last_modified: Sunday 24th August 2025 00:32
aliases: []
tags:
  - computer-science/floating-point-system
course: CSCC37
---
# floating point systems
A __floating point system__ is characterized by 4 integers:
- $\beta$: base of radix
- $t$: precision
- $[L,U]$: exponent range

# floating point numbers
Where __floating point number__ $x$ in the system are represented as
$$
x=\pm\left( d_{0}+\frac{d_{1}}{\beta}+\frac{d_{2}}{\beta^2}+\dots+\frac{d_{t-1}}{\beta^{t-1}} \right)\beta^e
$$
where
[]()$$
0\leq d_{i}\leq \beta-1,0\leq i\leq t-1
$$
and
$$
L\leq e\leq U
$$
We call the base-$\beta$ digits $d_{0}d_{1}\dots d_{t-1}$ the __mantissa__ or __significand__ and $e$ the __exponent__ or __characteristic

Note that the most commonly used two systems are __IEEE SP__ and __IEEEE DP__, where SP follows $\beta=2,t=24,L=-126,U=127$, DP follows $\beta=2,t=53,L=-1022,U=1023$.
For example, C's float datatype uses SP and double datatype uses DP