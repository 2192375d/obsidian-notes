---
title: big Theta notation
created: Monday 29th September 2025 13:43
last_modified: Monday 29th September 2025 13:43
aliases: []
tags:
  - computer-science/algorithm
course:
  - CSCC37
LEC:
---
# formal definition
Let $g\in\mathcal{F}$, $\theta(g)$ is the set of functions $f\in\mathcal{F}$ S.T.
$$
f(n)\in O(g)\cap \Omega(g(n))
$$
for some $d\in\mathbb{R}^+, c\in\mathbb{R}^+,t\in\mathbb{N}$, and for any $n\in\mathbb{N},n\geq t$
(eg $d\cdot g(n)\leq f(n)\leq c\cdot g(n)$)