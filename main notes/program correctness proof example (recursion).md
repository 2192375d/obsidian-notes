---
title: program correctness proof example(palindrome)
created: Friday 19th September 2025 14:25
last_modified: Friday 19th September 2025 14:25
aliases: []
tags:
  - computer-science/computation-logic/program-correctness
course:
  - CSCB36
LEC:
  - "3"
---
# program correctness proof sample (palindrome)
Consider this program and its specification:
- pre: `x` is a string
- post: return `True` iff `x` is a palindrome

`isPal(x)`:
```
1. if `len(x) < 2`, return `True`
2. if `x[0] != x[len(x)-1]`, return `False`
3. return `isPal(x[1:len(x)-1])`
```

## proof
Define the predicate $Q$ on $N$, $Q(n):$ "if `x` is a string and `n = len(x)`, then `isPal(x)` return `true` iff `x` is a palindrome"

We will use PCI to prove that $Q(n)$ holds for every $n$ in $\mathbb{N}$

basis case: We consider cases $n=0$ and $n=1$
For both cases, `isPal(x)` returns True \[line 1\]
This is correct because every string of length $<2$ is a palindrome

induction step: Let $n>1$,
Suppose $Q(j)$ holds whenever $0\leq j<n$ \[IH\]
WTP: $Q(n)$ holds

We consider 2 cases: `x[0] != x[len(x) - 1]` and `x[0] = x[len(x) - 1]`

If `x[0] != x[len(x) - 1]`, then
`isPal(x) returns False` \[line 2\]

This is correct because...