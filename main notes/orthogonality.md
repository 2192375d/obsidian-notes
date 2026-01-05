---
title: orthogonality
created: Tuesday 28th October 2025 07:25
last_modified: Tuesday 28th October 2025 07:25
aliases: []
tags:
  - math/linear-algebra/inner-product/norm
---
# orthogonal (definition)
Let $V$ be an inner product space
Two vectors $u,v\in V$ are called __orthogonal__ if $\langle u,v\rangle=0$

# orthogonal complement (definition)
Let $V$ be an inner product space, $S$ be a subset of $V$, then
$$
S^{\perp}=\{ u \in V,\langle u,v\rangle=0,\text{for any } v\in S\}
$$

## basic orthogonal complement properties
Let $V$ be a vector space, $U,W$ be subsets of $V$, then
- $U^{\perp}$ is a subspace of $V$
- $\{ 0 \}^{ \perp }=V$
- if $U\subset W$, then $W^{\perp}\subset U^{\perp}$

## orthogonal complement properties on subspace
Let $W$ be a subspace of $V$, then
- $W^{\perp}$ is a subspace
- $\dim(W^{\perp})=\dim(V)-\dim(W)$
- $(W^{\perp})^{\perp}=W$
- $W\cap W^{\perp}=\{ 0 \}$

## orthogonality and 0
- $0$ is orthogonal to every vector in $V$
- $0$ is the only vector in $V$ that is orthogonal to itself

## Pythagorean Theorem
Let $u,v$ be orthogonal vectors in $V$, then
$$
||u+v||^2=||u||^2+||v||^2
$$

### proof

## orthogonal decomposition
Let $u,v\in V$, with $v\neq 0$
Set $\displaystyle c=\frac{\left\langle  u,v \right\rangle}{||v||^2}$ and $\displaystyle w=u- \frac{\left\langle  u,v \right\rangle}{||v||^2}v$, then
$$
\langle w,v\rangle=0 \text{ and } u=cv+w
$$
