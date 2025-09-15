---
title: numerical quadrature
created: Saturday 30th August 2025 17:44
last_modified: Saturday 30th August 2025 17:44
aliases: []
tags:
  - calculus/integral/quadrature
  - computer-science/approximation
course: CSCC37
---
# numerical quadrature
The numerical approximation of definite integrals is caleld __numerical quadrature__

# quadrature rule
An $n$-point quadrature formula has the form
$$
I(f)=\int_{a}^b f(x)dx=\sum_{i=1}^nw_{i}f(x_{i})+R_{n}
$$

where:
- the points $x_{i}$ at which the function $f$ is evaluated are called __nodes__ or __abscissas__
- the multipliers $w_{i}$ are called __weights__
- $R_{n}$ is the __remainder__ or __error__
