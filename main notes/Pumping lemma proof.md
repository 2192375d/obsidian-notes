---
title: Pumping lemma proof
created: Friday 17th October 2025 14:50
last_modified: Friday 17th October 2025 14:50
aliases: []
tags:
  - computer-science/computation-logic
  - theorem
course:
  - CSCB36
LEC:
  - "7"
---
# Pumping lemma proof sketch
Suppose $L$ is regular
Let $M=(Q,\Sigma,\delta,s,F)$ be a DFSA S.T. $\mathcal{L}(M)=L$ (BY BIG RESULT!!!!- - - -)
Let $n=|Q|$, in other words, number of states in $M$
Let $x\in L$ where $|x|\geq M$

Consider $x=a_{1}a_{2}\dots a_{n}a_{n+1}\dots a_{|x|}\in L$
Consider $q_{i}=\delta^*(s,x[:i])$ (The state you get to after reading $i$ symbols), for $0\leq i\leq|x|$
Since the string is in $L$, we get $q_{|x|}\in F$

Note that when we get to $q_{n}$, the corresponding character is $a_{n}$, thus, we have $n+1$ states with $n$ characters, by Pigeon Hole Principle, at least one state is revisited.


Consider $u=a_{1}\dots a_{i}$, $v=a_{i}a_{i+1}$