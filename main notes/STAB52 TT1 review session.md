---
title: STAB52 TT1 review session
created: Before 28th July, 2025
last_modified: Wednesday 11th June 2025 15:34
tags:
  - probability
  - exam-review
course:
  - STAB52
---
# good resources
- The textbook (obviously)

## stuffs to remember that is not on the formula sheet
- Let $A, B$ be events, then$$P(A\cap B^C)=P(A)-P(A\cap B)$$$$P(A\Delta B)=P((A\cap B^c)\cup(B\cap A^c))=P(A)+P(B)-2P(A\cap B)$$

|                                         | care about order | don't care about order |
| --------------------------------------- | ---------------- | ---------------------- |
| don't put back a duplicate after taking | $Perm(n,k)$      | $\binom{n}{k}$         |
| put back a duplicate after taking       | $n^k$            | $\binom{n+k-1}{k}$     |

__independent__
Let $A, B$ be events, if $A\perp B$, then 
1. $P(A\cap B)=P(A)P(B)$
2. $P(A|B)=P(A),P(B|A)=P(B)$
__complement independence__
Let $A,B$ be events, if $A\perp B$, then$$A\perp B^c$$
__mutual independence__
Let $A_1,...,A_n$ be events, if $A_1,...,A_n$ are mutually independent, then $\forall A_{k_1},...,A_{k_m}\subset\{A_1,...,A_n\}$, $$P(A_{k_1}\cap\dots\cap A_{k_m})=P(A_{k_1})\dots P(A_{k_m})$$
__conditioning on mutual independence__
Let $A_1,...,A_n$ be mutually independent events
Suppose $A_{j_1},\dots,A_{k_l},A_{j_1},\dots,A_{j_l}\in\{A_1,\dots,A_n\}$ S.T. $\{A_{j_1},\dots,A_{k_l}\},\{A_{j_1},\dots,A_{j_l}\}$ are disjoint
Suppose $1\leq i\leq n$, then
1. $$P(A_i|A_{k_1},\dots A_{k_m})=\frac{P(A_i\cap A_{k_1}\cap\dots\cap A_{k_m})}{P( A_{k_1}\cap\dots\cap A_{k_m})},$$ 
2. $$P(A_{j_1}\cap\dots\cap A_{j_k}|(A_{k_1},\dots,A_{k_m}))=P(A_{j_1}\cap\dots\cap A_{j_l})$$
__conditional independence__
Just remember 
1. if $(A\perp B|C)$, then $(A\perp B^c|C$), however (IMPORTANT!!!), $P(A\cap B|C)\neq P(A\cap B|C^c)$
2. if $A,B,C$ are mutually independent, then $(A\perp B|C)$

## Questions to go through
#### (Q5 2020)
![[Pasted image 20250611135814.png]]

Give them 7 minutes to think about it
<u>Points to talk about</u>
- The probability laws apply "inside" conditional statements
	$P(A\cap B^c|C)=P(A|C)-P(A\cap B|C)$
- You can't take the complement of the event you are conditioning on
	$P(A|B)\neq P(A|B^c)$

