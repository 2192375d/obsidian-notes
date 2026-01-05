---
title: prove a set of connectives is complete
created: Saturday 29th November 2025 11:28
last_modified: Saturday 29th November 2025 11:28
aliases: []
tags:
  - math/logic
course:
  - CSCB36
LEC:
  - "11"
---

## uoc
We use __uoc__ as an  abbreviation for "uses only connectives in"
eg. "$F$ uoc $C$" means "$F$ uses only connectives in $C$"

# prove a set of connectives is complete
Steps:
1. Use structural induction to define the set $\mathcal{G}$ that uoc $\{ \neg,\wedge \}$ or $\{ \neg,\vee \}$
2. Use structural induction to prove that for every formula $F\in\mathcal{G}$, there exists a formula $F'$ S.T. $F'$ uoc $C$ and $F' \ \text{\small LEQV}\ F$