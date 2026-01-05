---
title: language accepted by a machine
created: Wednesday 8th October 2025 15:43
last_modified: Wednesday 8th October 2025 15:43
aliases: []
tags:
  - computer-science/computation-logic/automata
course:
  - CSCB36
LEC:
  - "6"
---
# language accepted by a machine
The language accepted by a machine $M$ is
$$
\mathcal{L}(M)=\{ x\in\Sigma^*:  M\text{ accepts }x\}
$$

(Note that this works for both DFSA and NFSA)
## how to describe the language accepted
$\mathcal{L}(M)$ can be described by just giving what are accepted or not accepted

Consider the example below
(image to be inserted)

In this example, $\{\displaystyle\mathcal{L}(M)=x\in\Sigma^*: \text{x has odd number of 1 iff x ends with 1}\}$

This can be proven using a state invariant

Consider $\delta^*(q_{0},x)$,
$$
\delta^*(q_{0},x)=\begin{cases}
q_{0},& \text{$x$ has even number of $1$s and $x$ doesn't end with $1$} \\
q_{1},& \text{$x$ has odd number of $1$ and $x$ ends with $1$}\\
q_{2},& \text{$x$ has odd number of $1$ and $x$ ends with $0$}\\
q_{3},& \text{$x$ has even number of $1$ and $x$ ends with $1$}
\end{cases}
$$
(just don't prove this cause it's stupid)