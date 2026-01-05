---
title: propositional logic
created: Wednesday 12th November 2025 15:19
last_modified: Wednesday 12th November 2025 15:19
aliases: []
tags:
  - math/logic
course:
  - CSCB36
LEC:
  - "10"
---
# propositional logic
proposition: A true/false statement

## connectives
- not: $\neg$
- and: $\wedge$
- or: $\vee$
- conditional: $\implies$
- biconditional: $\iff$

## propositional variables
Consider $PV$ to be set of all propositional variables
Then, we can define the set of all __propositional formulas__ using structural induction

Let $\mathcal{F}$ be the smallest set S.T.
- basis: for every $x\in PV,x\in\mathcal{F}$
- induction step: if $P_{1},P_{2}\in\mathcal{F}$, then $\neg P_{1},(P_{1}\wedge P_{2}),(P_{1}\vee P_{2}),(P_{1}\implies P_{2}),(P_{1}\iff P_{2})\in\mathcal{F}$

## example
Consider $(x \wedge y)$, true or false?
The answer is: It depends on the truth value of $x$ and $y$

## truth assignment
A __truth assignment__ (lowercase t.a.) is a function $\tau:PV\to \{ 0,1 \}$ where $0$ stands for `False` and $1$ stands for `True`

An __extended true assignment__ (extend t.a.) is a function $\tau^*:\mathcal{F}\to \{ 0,1 \}$
And we can define extended t.a. using a t.a.
- $\tau^*(x)=\tau(x)$
- $\tau^*(\neg P_{1})=1-\tau(P_{1})$
- $\tau^*((P_{1}\wedge P_{2}))=\tau(P_{1})*\tau(P_{2})=\min(\tau(P_{1}),\tau(P_{2}))$
- $\tau^*((P_{1}\vee P_{2}))=\max(\tau(P_{1}),\tau(P_{2}))$
- $\displaystyle\tau^*(P_{1}\implies P_{2})=\begin{cases}1 &\text{if } \tau(P_{1})=0\text{ or }\tau (P_{2})=1\\0 &\text{otherwise} \end{cases}$
- $\displaystyle\tau^*(P_{1}\iff P_{2})=\begin{cases}1 &\text{if } \tau(P_{1})=\tau(P_{2})\\0 &\text{otherwise} \end{cases}$

## tautology/contradiction
Let $F$ be a formula, $\tau$ be a t.a.
- $\tau$ __satisfies__ $F$ means $\tau^*(F)=1$
- $\tau$ __falsifies__ $F$ means $\tau^*(F)=0$

$F$ is a __tautology__ means every t.a. satisfies $F$ (eg. $x\vee \neg x$)
$F$ is __satisfiable__ means some t.a. satisfies $F$
$F$ is __unsatisfiable__ means every t.a. falsifies $F$ (eg. $x\wedge \neg x$)
$F$ is __faltisfiable__ means some t.a. falsifies $F$

Note that tautology is also called __valid formula__, unsatisfiable $F$ is also called a __contradiction__

## logical implication/equivalence
Let $F_{1},F_{2}$ be formulas, then
- $F_{1}$ __logically implies__ $F_{2}$ means every t.a. that satisfies $F_{1}$ also satisfies $F_{2}$ (eg a contradiction logically implies every formula)
- $F_{1}$ is __logically equivalent__ to $F_{2}$ means every $F_{1}$ logically implies $F_{2}$ and $F_{2}$ logically implies $F_{1}$

Notation: 
- $F_{1}\text{\small LIMP}F_{2}$ for $F_{1} \implies F_{2}$
- $F_{1}\text{\small LEQV}F_{2}$ for $F_{1}\iff F_{2}$

## theorem: logical implication/equivalence
- $F_{1} \small \text{LIMP}F_{2}$ iff $F_{1}\to F_{2}$ is a tautology
- $F_{1}\text{\small LEQV}F_{2}$ iff $F_{1}\leftrightarrow F_{2}$ is a tautology

## conventions
- omit outermost parentheses
- precedence (high to low)
  $\neg$
  $\wedge$
  $\vee$
  $\implies,\iff$
  where for equal precedence, we follow __right associate__
  for example, $x\to y\iff z$ means $(x\to(y\iff z))$, $x\wedge y\wedge z$ means $(x\wedge(y\wedge z))$
