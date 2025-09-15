---
title: polynomial evaluation
created: Thursday 28th August 2025 19:04
last_modified: Thursday 28th August 2025 19:04
aliases:
  - Horner's method
tags:
  - computer-science/approximation
  - math/application
course: CSCC37
---
# Horner's method
A polynomial $p(t)=x_{0}+x_{1}t+\dots+x_{n-1}t^{n-1}$ can be evaluated efficiently using the __Horner's method__, also known as __nested evaluation__ or __synthetic division__

This is done by rewriting it as
$$
p(t)=x_{1}+t(x_{2}+t(x_{3}+(\dots(x_{n-1}+x_{n}t)\dots)))
$$

In such form, we only need $n$ additions and $n$ multiplications.

We can also make use of this when forming Vandermonde matrix