---
title: diagonalization
created: Friday 21st November 2025 02:14
last_modified: Friday 21st November 2025 02:14
aliases:
  - similar matrix
tags:
  - math/linear-algebra/eigenvalue
---
# diagonalization
Let $T\in\mathcal{L}(V)$, then $T$ is __diagonalizable__ if there is a basis $\alpha$ of $V$ consisting of eigenvectors of $T$

## characterization of diagonalizable
Let $T \in\mathcal{L}(V)$, then 
- $T$ is diagonalize if and only if $\displaystyle [T]_{\alpha}^{\alpha}$ is similar to a diagonal matrix

## properties of diagonalizable
Supposed $T\in\mathcal{L}(V)$ has $n$ distinct real eigenvalues, then $T$ is diagonalizable

# similar matrix
Let $A,B\in\mathcal{M}(\mathbb{F}^n)$, then $A$ is __similar__ to $B$ if for some invertable matrix $P$,
$$
B=PAP^{-1}
$$

## diagonalization and algebraic
Let $T\in\mathcal{L}(V)$, suppose it has real eigenvalues $\lambda_{1},\dots,\lambda{k}$
Let $m_{i}$ be the algebraic multiplicity of the eigenvalue $\lambda_{i}$

Then, $T$ is diagonalizable if and only if
- $\dim(V)=m_{1}+\dots +m_{k}$
- $\dim(E_{\lambda_{i}})=m_{i}$

## diagonalization
To diagonalize a matrix $M\in\mathcal{M}(\mathbb{F}^n)$, you can do
1. Find all the eigenvalues of $M$
2. For each eigenvalue, find the basis of the eigenspace
3. Then, $M=PDP^{-1}$, where $P=[v_{1},\dots,v_{n}]$ has all the eigenvectors in the order, and $D$ has the eigenvalues in the order.