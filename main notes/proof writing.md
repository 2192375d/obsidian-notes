---
title: proof writing
created: Wednesday 3rd September 2025 18:35
last_modified: Wednesday 3rd September 2025 18:35
aliases: []
tags:
  - math/proof
course:
  - CSCB36
LEC:
  - "1"
---
# Things to avoid when writing proofs
1. Do not equate a truth funciton with a numerical value (eg: $P(n) = f(n)=3$, where $P$ is a truth function is wrong, should be instead $P(n):f(n)=3$)
2. Do not quantify a predicate variable (eg: $P(n)$ is true for all $n\in\mathbb{N}$ is wrong, should be $\forall n\in\mathbb{N},P(n)$)
3. Do not "stack" (eg: $n=2,f(2)=2^2-2,2=2$ should instead be $f(n)=f(2)=2^2-2=2=n$)
4. Mention IH when necessary, and indicate where it is used