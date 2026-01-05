---
title: pushdown automada example
created: Wednesday 5th November 2025 16:26
last_modified: Wednesday 5th November 2025 16:26
aliases: []
tags:
  - computer-science/computation-logic/automata
course:
  - CSCB36
LEC:
  - "7"
---

## PDA example
$\Sigma=\{ 0,1 \}$, $L=\{ x\in\Sigma^*:\#_{0}(x)=\#_{1}(x) \}$
Find a PDA that accepts $L$
![[pushdown automata (PDA) 2025-11-05 15.37.49.excalidraw|100%]]
(Note that this is a __deterministic PDA__, also called __DPDA__)
By deterministic, this means there is no "choice" for which transition to go for

Note that PDA in general (that is, nondeterministic PDA), is at the same level as DPDA on big results

An (N)PDA $M$ that accepts $L$ this can be
![[pushdown automata (PDA) 2025-11-05 15.51.20.excalidraw]]

Consider proving $\mathcal{L}(M)=L$ via showing $\mathcal{L}(M)\subset L$  and $L\subset\mathcal{L}(M)$
(to be continued...)

## another PDA example
Consider an DPDA and an (N)PDA $\{ x\in\Sigma^*:\#_{00}(x)=\#_{11}(x) \}$

For DPDA:
![[pushdown automata (PDA) 2025-11-05 16.00.41.excalidraw|100%]]

For (N)PDA:
![[pushdown automata (PDA) 2025-11-05 16.20.56.excalidraw|100%]]

## another another PDA example
Consider $L=\{ x\in\Sigma^*:2\#_{00}(x)=\#_{11}(x) \}$
DPDA:
![[pushdown automada example 2025-11-05 16.27.53.excalidraw|100%]]

NPDA:
![[pushdown automada example 2025-11-05 16.42.37.excalidraw|100%]]

