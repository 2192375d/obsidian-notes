---
title: unimodal
created: Friday 26th September 2025 19:17
last_modified: Friday 26th September 2025 19:17
aliases: []
tags:
  - math
course:
  - CSCB36
LEC:
  - "4"
---
# unimodal
Let $L$ be a list of integers
Let `L[p:q]` be a nonempty slice (ie $0\leq p<q\leq len(L)$)
We say that `L[p:q]` is __unimodal__ if there exists a $m\in\mathbb{N}$ S.T.: 
1. $p\leq m<q$
2. `L[p:m+1]` is strictly increasing
3. `L[m:q]` is strictly decreasing

where $m$ is called __mode__ of $L[p:q]$

## notes regarding unimodal
Since $L$ is the same as `L[0:len(L)]`, we also say $L$ is unimodal if `L[0:len(L)]` is unimodal

- note 1: any increasing slice `L[p:q]` is unimodal with mode $q-1$
- note 2: `L[p:p+1]` (ie any slice of length one) is both increasing and decreasing, thus `L[p:p+1]` is unimodal with mode $p$
- note 3: any smaller and nonempty slice within a unimodal slice is also unimodal, though not necessarily with the same mode
- note 4: the maximum element of an unimodal slice occurs at its mode