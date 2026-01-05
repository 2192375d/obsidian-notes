---
title: matrix norms
created: Sunday 24th August 2025 14:15
last_modified: Sunday 24th August 2025 14:15
aliases: []
tags:
  - math/linear-algebra/inner-product/norm
course: CSCC37
---
# matrix norms
Given a vector norm (eg. the $p$ value), the __matrix norm__ of a matrix $A$ is
$$
||A||=\max_{ x \neq 0 }  \frac{||Ax||}{||x||}
$$
This matrix norm is said to be __subordinate__ to the vector norm
Intuitively, the matrix norm measures the maximum stretching the matrix does to any vector.

## 1-matrix norm
The 1-matrix norm can be derived as
$$
||A||_{1}= \max_{j} \sum_{i=1}^n|a_{ij}|
$$
(eg the maximum absolute value sum of the matrix from some column $j$ in $A$)

## 2-matrix norm
The 2-matrix norm can be derived as
$$
||A||_{2}=\sqrt{e(A^TA)}
$$
where $e(M)$ is the biggest eigenvalue of $M$

We call $e(A^TA)$ is the spectral radius of $A$

If $A$ is orthogonal, then $\sqrt{ e(A^TA) }=\sqrt{ e(I) }=1$
and $||A^{-1}||=\sqrt{ e((A^{-1})^{T}A^{-1}) }=\sqrt{ e(AA^{-1}) }=\sqrt{ e(I) }=1$

## $\infty$-matrix norm
The $\infty$-matrix norm can be derived as:
$$
||A||_{\infty}=\max_{i}\sum_{j=1}^n|a_{ij}|
$$
(eg the maximum absolute value sum of the matrix from some row $i$ in $A$)