---
title: Cayley Hamilton theorem
created: Friday 12th December 2025 21:17
last_modified: Friday 12th December 2025 21:17
aliases: []
tags:
  - math/linear-algebra
---
# Cayley Hamilton theorem
Let $A\in\mathcal{M}(\mathbb{F}^n)$
Then, if $A$ is simialr to a diagonal matrix $D$, i.e. $D=P^{-1}AP$ where $P$ is an $n$ by $n$ invertible matrix, then
$$
A^k=PD^kP^{-1}
$$

Also, if $A$ has this characteristic polynomial
$$
\det(A-\lambda I)=a_{0}+a_{1}\lambda+\dots+a_{n}\lambda^n
$$
Then,
$$
a_{0}I+a_{1}A+\dots+a_{n}A^n=0
$$
