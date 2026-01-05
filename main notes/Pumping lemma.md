---
title: Pumping lemma
created: Friday 17th October 2025 14:20
last_modified: Friday 17th October 2025 14:20
aliases: []
tags:
  - computer-science/computation-logic
  - theorem
course:
  - CSCB36
LEC:
  - "7"
---
# Pumping lemma
(Used to prove a language is not regular through contradiction)

If $L$ is a regular language, then there is an integer $n>0$ with the property that:
For any string $x\in L$ where $|x|\geq n$, there are strings $u,v,w$ S.T.
- $x=uvw$
- $v\neq\epsilon$
- $|uv|\leq n$
- $uv^kw\in L$ for all $k\in\mathbb{N}$

## apply Pumping lemma
To prove that a language $L$ is not regular, we use proof by contradiction:
1. Suppose $L$ is regular
2. Since $L$ is regular, by Pumping Lemma and assert the existence of a number $n>0$ that satisfies the 4 properties
3. Find a string $x$ S.T. $x\in L$ and $|x|\geq n$ 
(Note that step 3 is the trickiest part, a wrong choice could make step 4 impossible)
4. By Pumping lemma, there are strings $u,v,w$ S.T. all four properties hold. Pick a particular number $k\in\mathbb{N}$ and argue that $uv^kw\not\in L$, thus yielding our desired contradiction
