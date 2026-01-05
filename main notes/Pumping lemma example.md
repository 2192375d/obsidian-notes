---
title: Pumping lemma example
created: Friday 17th October 2025 14:31
last_modified: Friday 17th October 2025 14:31
aliases: []
tags:
  - computer-science/computation-logic
course:
  - CSCB36
LEC:
  - "7"
---
# example of using PL to prove a language is not regular (palindrome)
Consider $\Sigma=\{ 0,1 \},L=\{ x\in\Sigma ^*:x^R=x \}$
WTP $L$ is not regular

By way of contradiction, suppose $L$ is regular
Let $n$ be as in P.L.
Choose $x=0^n 10^n$

(Note that $x\in L$ by defn of $L$ and $|x|=2n+1\geq n$)
By 1, 2, 3 from the lemma, $v=0^j$ for some $j$ where $0<j\leq n$
By 4, (pick $k = 2$, ie by puming $v$ 2 times), we get $uv^2w\in L$
However, $uv^2w=uvvw=0^{i+j}10^n\not\in L$, which is a contradiction

# another example
Let $L=\{ (10)^p 1^q:p,q\in\mathbb{N},p\geq q \}$
WTP $L$ is not regular

## step 1
By way of contradiction, suppose $L$...