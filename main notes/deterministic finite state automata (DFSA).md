---
title: deterministic finite state automata
created: Wednesday 3rd September 2025 10:37
last_modified: Wednesday 3rd September 2025 10:37
aliases:
tags:
  - computer-science/computation-logic/automata
course:
  - CSCB36
LEC:
  - "6"
---
# deterministic finite state automata (DFSA)
A __DFSA__ $M$ is a quintuple (5 tuple) $M=(Q,\Sigma,\delta,s,F)$ where
- $Q$ is a finite set of __states__
- $\Sigma$ is the __input alphabet__
- $\delta:Q\times \Sigma\to Q$ is a __transition function__, note $\delta(q,a)=q'$ means that there is an edge labeled $a$ from state $q$ to state $q'$
- $s\in Q$ is the __start state__ or __initial state__ ($s\in Q$)
- $F\subset Q$ is the set of __accepting states__ ($F \subset Q$)

A DFSA accepts an input symbol $x\in\Sigma$ iff $\delta(s,x)\in F$
A DFSA accepts an input string $x\in\Sigma^*$ iff $\delta^*(s,x)\in F$

## DFSA diagram
(to be continued)