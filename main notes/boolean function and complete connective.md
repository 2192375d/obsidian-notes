---
title: complete connective
created: Friday 14th November 2025 14:45
last_modified: Friday 14th November 2025 14:45
aliases: []
tags:
  - math/logic
course:
  - CSCB36
LEC:
  - "10"
---
# boolean functions
Let $n\in\mathbb{Z},n>0$, then a __boolean function__ (of $n$ inputs) is a function that takes $n$ binary values as input and returns one binary value as output
In other words, it's a function maps from $\{ 0,1 \}^*$ to $\{ 0,1 \}$

# represent boolean function
A propositional formula $F$ with propositional variables $x_{1},\dots,x_{n}$ is said to represent a boolean functiiion $f$ of $n$ iff:

For every truth assignment $\tau$, 
- $\tau$ satisfies $F$ whenever $f(\tau(x_{1}),\dots,\tau(x_{n}))=1$
- $\tau$ falsifies $F$ whenever $f(\tau(x_{1}),\dots,\tau(x_{n}))=0$
Notice that logically equivalent formulas always represent the same boolean function

# completeness
A set $C$ of connectives is said to be __complete__ iff every boolean function can be represented by a propositional formula that uses only connectives in $C$

For example, 
- $\{ \neg,\wedge,\vee \}$ is complete
- $\{ \neg,\wedge \}$ and $\{ \neg,\vee \}$ are both complete as ($P\vee Q$) ($P\vee Q\text{\small LEQV}\neg(\neg(P\wedge \neg Q))$)
