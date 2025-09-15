---
title: deterministic finite state automata
created: Wednesday 3rd September 2025 10:37
last_modified: Wednesday 3rd September 2025 10:37
aliases:
  - transition function
tags:
  - computer-science/computation-logic/automata
course:
  - CSCB36
LEC: []
---
# DFSA (deterministic finite state automata)
A __DFSA__ $M$ is a quintuple $M=(Q,\Sigma,\delta,s,F)$ where
- $Q$ is a finite set of __states__
- $\Sigma$ is a finite alphabet
- $\delta:Q\times \Sigma\to Q$ is a __transition function__, note $\delta(q,a)=q'$ means that there is an edge labeled $a$ from state $q$ to state $q'$
- $s\in Q$ is the __start state__ or __initial state__
- $F\subset Q$ is the set of __accepting states__

