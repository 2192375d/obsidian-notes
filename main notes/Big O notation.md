---
title: Big O notation
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 01:11
tags:
  - computer-science/algorithm
course:
  - CSCA48
  - CSCC37
---
# big O notation (CSCA48)
To state that $f(N)=O(g(N))$, which is to say that a function $f(N)$ has a __big O complexity__ of $g(N)$ means that $f(N)\leq c*g(N)$, for a sufficiently large value of $N$ (usually stated as $N>N_{0}$).

We call it run-time $f(x)$ of some algorithm is of order $O(g(x))$

_example_
- Linear search with a complexity of $O(N)$ read as "the complexity of linear search is of order $N$"

Note that we assume $f(N),c,g(N)$ are positive

_example_
- for $0.75*N$, if $N=10$, then the implementation runs in $7.5$ seconds
- for $0.75*N+0.25$, same as previous, but the implementation has a startup time of $0.25$ second.

# formal definition (CSCC37)
We say that
$$
f(n)=O(g(n))
$$
if there exists a positive constant $C$ S.T. for sufficiently large $n$
$$
|f(n)|\leq C|g(n)|
$$

for example, for $\displaystyle f(h)=\frac{1}{1-h}$, we say
$$
f(h)=1+h+h^2+h^3+\dots=1+h+O(h^2)
$$
