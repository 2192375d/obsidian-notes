---
title: sequence
created: Sunday 3rd August 2025 12:02
last_modified: Sunday 3rd August 2025 12:02
aliases:
  - initial segment
tags:
  - math/set-theory/sequence
course:
  - CSCB36
---
# initial segment
Let $\mathbb{N}$ be the set of natural numbers ($0,1,2,3\dots$), an __initial segment__ $I$ of $\mathbb{N}$ is a subset of $\mathbb{N}$ following this:
$$
\forall k\in I,k>0\to k-1\in I
$$
Thus, the initial segement is either an empty set or the set $\{ 1,2,3,\dots,k \}$, for some $k\in \mathbb{N}$

# sequence
Let $A$ be a set, then a __sequence over__ $A$ is a function $\sigma:I\to A$, where $I$ is the initial segment of $\mathbb{N}$.
When we say $\{ a_{0},a_{1},a_{2},\dots \}$ is a sequence, we meant $a_{0}=\sigma(0)$, $a_{1}=\sigma(1)$ and so on.

If $I=\emptyset$, then $\sigma$ is the __empty__ or __null__ sequence, denoted $\epsilon$, with length $0$ 
If $I=\mathbb{N}$, then $\sigma$ is an __inifinite__ sequence, with length $\infty$