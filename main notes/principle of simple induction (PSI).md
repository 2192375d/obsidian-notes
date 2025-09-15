---
title: simple induction
created: Monday 4th August 2025 02:17
last_modified: Monday 4th August 2025 02:17
aliases:
  - simple induction
tags:
  - math/set-theory
  - theorem
course:
  - CSCB36
---
# simple induction
![[simple induction 2025-08-04 02.38.42.excalidraw|100%]]

# proof by simple induction
Let $b\in\mathbb{N}$, $P$ be a predicate on $\mathbb{N}$
If we prove:
- basis step: $P(b)$
- induction step: $\forall n\geq b$, $P(n)\to P(n+1)$
Then we can conclude:
- $\forall n\geq b,P(n)$

_example_
Given $n$, find $k,l\in\mathbb{N}$ S.T. $4k+7l=n$
Let $P()$