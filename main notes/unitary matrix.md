---
title: unitary matrix
created: Friday 12th December 2025 20:01
last_modified: Friday 12th December 2025 20:01
aliases:
  - Schur's theorem
  - spectral theorem
tags:
  - math/linear-algebra/matrix
course:
  - MATB24
LEC:
---
# unitary matrix
Let $U\in \mathcal{M}(\mathbb{C}^n)$ is __unitary__ if its column vectors are orthogonal unit vectors

In other words, $U^*U=I$

## properties of unitary matrix
$U\in\mathcal{M}(\mathbb{C}^n)$ is unitary if and only if
- $U$'s column vectors form an orthonormal basis of $\mathbb{C}^n$ under the complex dot product
- $U$'s row vectors form an orthonormal basis of $\mathbb{C}^n$ under the complex dot product
and also product of unitary matrices is unitary

## orthogonal equivalence
$A,B\in\mathcal{M}(\mathbb{C}^n)$ are orthogonally equivalent if there is an orthogonal matrix $M$ S.T.
$$
B=M^{-1}AM
$$

## unitary equivalence
$A,B\in\mathcal{M}(\mathbb{C}^n)$ are unitarily equivalent if there is an unitary matrix $U$ S.T.
$$
B=U^{-1}AU
$$

## Schur's theorem
Let $A\in\mathcal{M}(\mathbb{F}^n)$ be S.T. its characteristic polynomial splits over $\mathbb{F}$ (in other words, the polynomial factors into linear functions), then
- if $\mathbb{F}=\mathbb{C}$, then $A$ is unitarily equivalent to a complex upper triangular matrix
- if $\mathbb{F}=\mathbb{C}$, then $A$ is orthogonally equivalent to a real upper triangular matrix

## spectral theorem (for Hermitian matrices)
Let $A\in\mathcal{M}(\mathbb{C}^n)$ be a Hermitian, then there exists an unitary matrix $U$ S.T. $U^{-1}AU$ is a diagonal matrix, with real eigenvalues

In other words, 
- if $A\in\mathcal{M}(\mathbb{R}^n)$, then $A$ is symmetric if and only if $A$ is orthogonally diagonalizable
- if $A\in\mathcal{M}(\mathbb{C}^n)$, then if $A$ is Hermition, $A$ is unitarily diagonaliable

## Hermitian matrix eigenvectors are orthogonal
The eigenvectores of a Hermitian matrix corresponding to distinct eigenvalues are orthogonal.