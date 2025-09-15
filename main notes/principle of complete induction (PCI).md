---
title: complete induction
created: Monday 4th August 2025 02:45
last_modified: Monday 4th August 2025 02:45
aliases: 
tags:
  - math/set-theory
  - theorem
course:
  - CSCB36
---
# principle of complete induction
![[complete induction 2025-08-04 02.45.48.excalidraw|100%]]

# complete induction proof
If we prove:
- basis step: $P(b),P(b+1),\dots,P(b+k-1)$
- induction step: $\forall n\geq b+k$, $(\forall b\leq j<n,P(j))\to P(n)$
Then we can conclude:
- $\forall n\geq b,P(n)$