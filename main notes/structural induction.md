---
title: structural induction
created: Friday 12th September 2025 14:14
last_modified: Friday 12th September 2025 14:13
aliases:
  - define curly E using structural induction
tags:
  - computer-science/computation-logic
  - math/induction
course:
  - CSCB36
LEC:
  - "2"
---
Structural induction is used for
- define sets
- prove some property about evrey element in a set that's defined by structural induction

# structural induction (intuition)
Consider when we want to define well formed algebraic expressions with variables $x,y,z$ and operators $+,-,\times,\div$.
The set of symbols (the __alphabet__) we want to use is $\Sigma=\{ x,y,z,+,-,x,\div,(,) \}$.
Then, $\Sigma^*$ is the set of all __finite strings__ with symbols from $\Sigma$

We want to use __structural induction__ to define $\Sigma^*$

# define $\mathcal{E}$ using structural induction
Let $\mathcal{E}$ be the smallest set S.T.
- basis: $x,y,z\in\mathcal{E}$
- induction step: if $e_{1},e_{2}\in\mathcal{E}$, then $(e_{1}+e_{2}),(e_{1}-e_{2}),(e_{1}\times e_{2}),(e_{1}\div e_{2})\in\mathcal{E}$