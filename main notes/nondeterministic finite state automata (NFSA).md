---
title: nondeterministic finite state automata
created: Wednesday 8th October 2025 16:24
last_modified: Wednesday 8th October 2025 16:24
aliases: []
tags:
  - computer-science/computation-logic/automata
course:
  - CSCB36
LEC:
  - "6"
---
# nondeterministic finite state automata (NFSA)
An NFSA is an DFSA with 2 added features
- multiple choices on reading a symbol, for example:
![[nondeterministic finite state automata (NFSA) 2025-10-08 16.27.03.excalidraw]]
- epsilon transition, for example:
![[nondeterministic finite state automata (NFSA) 2025-10-08 16.28.15.excalidraw]]
(spawntaneously go to another state...?)

## NFSA example
![[nondeterministic finite state automata (NFSA) 2025-10-08 16.30.22.excalidraw|70%]]

Here, input $01$ is considered as __accepted__ as there exists one case when the string is accepted

## strings accepted by NFSA
An NFSA $M$ accepts a string $x$ iff there is a way to start at the initial state, read the whole string $x$, and end in the accepting state

In the previous example, 
$$
\begin{align}
\mathcal{L}(M)&=\{ x\in\Sigma^*: \text{$x$ ends with $01$ and $111$ is not a substring of $x$ and $x$ starts with $0$} \}\\
&=\mathcal{L}((00^*1(1+\epsilon))^*0^*01)\\
&=\mathcal{L}((0 + 01 + 011)^*01)
\end{align}
$$