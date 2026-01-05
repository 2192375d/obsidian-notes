---
title: pushdown automata (PDA)
created: Wednesday 5th November 2025 15:13
last_modified: Wednesday 5th November 2025 15:13
aliases: []
tags:
  - computer-science/computation-logic/automata
course:
  - CSCB36
LEC:
  - "7"
---
# PDA
Informally, a PDA is an NFSA with a stack. (eg NFSA with a memory)

Formally, A PDA is a 6-tuple $M=(Q,\Sigma,\Gamma,\delta,s,F)$ where
- $Q$: finite set of states
- $\Sigma$: input alphabet
- $\Gamma$: stack alphabet
- $\delta$: transition function, $\delta:Q\times (\Sigma \cup \{ \epsilon \} )\times(\Gamma\cup \{ \epsilon \})\to \mathcal{P}(Q\times(\Gamma\cup \{ \epsilon \}))$
- $s$: initial state, $s\in Q$
- $F$ set of accepting states, $S\subset Q$

Here is a sample transition:
![[pushdown automata (PDA) 2025-11-05 15.21.20.excalidraw|100%]]

For the $X$ and $Y$ as above,
- if $X=\epsilon,Y\in\Gamma$ then this means push $Y$ on stack
- if $X\in\Gamma,Y=\epsilon$ then this means pop $Y$ from stack (only when $X$ is at the top of stack)
- if $X,Y\in\Gamma$ then this means replace $X$ by $Y$ at the top of stack (only when $X$ is at top of stack)
- if $X=Y=\epsilon$ then this means no stack operation

## string accepted by PDA
A PDA $M$ accepts a string $x$ means there is a way for $M$
- initially with an empty stack (eg stack is empty during initial state)
- read all of $x$
- end in an accepting state
- end with empty stack

(Note that some textbook define a PDA $M$ to accept a string if $M$ ends with an empty stack, while some defines $M$ to end at the correct state)

