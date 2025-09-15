---
title: iterated integrals for x and y-simple regions
created: Monday 11th August 2025 14:00
last_modified: Tuesday 29th July 2025 00:44
aliases: 
tags:
  - calculus/integral
  - calculus/multivariable
  - theorem
course:
  - MATB41
---
# theorem (iterated integrals for x-simple region)
Let $D$ be $x$-simple, then $D=\{ (x,y):c\leq y\leq d \text{ and } \psi_{1}(y)\leq x\leq \psi_{2}(y) \}$ and
$$
\iint_{D}f(x,y)dA=\int_{c}^d\left[ \int_{\psi_{1}(y)}^{\psi_{2}(y)}f(x,y)dx \right]dy
$$

Same applies to $y$-simple region

# theorem (iterated integral for simple region)
Let $D$ be a simple region, then
$$
\iint_{D}f(x,y)dA=\int_{a}^b\int_{\varphi_{1}(x)}^{\varphi_{2}(x)}f(x,y)dydx=\int_{c}^d\int_{\psi_{1}(y)}^{\psi_{2}(y)}f(x,y)dxdy
$$
