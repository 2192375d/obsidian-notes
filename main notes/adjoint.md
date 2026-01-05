---
title: adjoint
created: Friday 21st November 2025 02:54
last_modified: Friday 21st November 2025 02:54
aliases: []
tags:
  - linear-algebra/inner-product/adjoint
---
# adjoint (Hermitian adjoint)
Let $T\in\mathcal{L}(V,W)$, then the __adjoint__ of $T$ is the function $T^*:W\to V$ S.T.
$$
\langle Tv,w\rangle=\langle v,T^*w\rangle
$$

## adjoint is linear map
if $T\in\mathcal{L}(V,W)$, then $T^*\in\mathcal{L}(W,V)$

## adjoint properties
Let $S,T\in\mathcal{L}(V,W)$, $\lambda\in\mathbb{F}$, then
1. $(S+T)^*=S^*+T^*$
2. $(\lambda T)^*=\bar{\lambda}T^*$
3. $(T^*)^*=T$  for all $T\in\mathcal{L}(V,W)$
4. $I^*=I$

Let $S\in\mathcal{L}(V,W),T\in\mathcal{L}(W,U)$, then
5. $(ST)^*=T^*S^*$

## nullspace and range of $T^*$
Let $T\in\mathcal{L}(V,W)$, then
1. $\mathrm{range}(T^*)=(\mathrm{null} \ T)^{\perp}$ 
1. $\mathrm{null}(T)=(\mathrm{range} \ T^*)^{\perp}$ 
1. $\mathrm{range}(T)=(\mathrm{null} \ T^*)^{\perp}$ 

## conjugate transpose and adjoint
Let $A\in\mathbb{F}^{m,n}$, then the transformation produced by the conjugate transpose of $A$ is adjoint to the transformation produced by $A$

# self adjoint (Hermitian)
Let $T\in\mathcal{L}(V)$, then $T$ is __self-adjoint__ if $T=T^*$, in other words, $T$ is self-adjoint if
$$
\langle Tv,w\rangle=\langle v,Tw\rangle
$$

## diagonal entries of self adjoint matrix
Let $A\in\mathcal{L}(\mathbb{C}^n)$, $A$ be self-adjoint, then $A$'s diagonal entries are real