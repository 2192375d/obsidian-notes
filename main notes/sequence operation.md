---
title: sequence operation
created: Sunday 3rd August 2025 12:44
last_modified: Sunday 3rd August 2025 12:44
aliases: 
tags:
  - math/set-theory/sequence
course:
  - CSCB36
---
## sequence concatenation
Let $\sigma:I\to A$, $\sigma':I'\to A$ be sequences over set $A$, and supposed $\sigma$ is finite
if $\sigma'$ is infinite, let $J=\mathbb{N}$, otherwise, let $J$ be the initial segment $\{ 0,1,\dots,|I|,\dots|I|+|I'|-1 \}$.
Then, the __concatenation__ of $\sigma$ and $\sigma'$ is a sequence $\sigma\circ\sigma':J\to A$, where
$$
\begin{align}
&\forall i\in I,\ \sigma\circ\sigma'(i)=\sigma(i), \\
&\forall i\in I',\ \sigma\circ\sigma'(|I|+i)=\sigma'(i)
\end{align}
$$

## sequence reversal
Let $\sigma:I\to A$, then the reversal of $\sigma$ is a sequence $\sigma^R:I\to A$ S.T. 
$$
\forall i\in I, \ \sigma^R(i)=\sigma(|I|-1-i)
$$
## sequence equivalence
By definition of function equivalence and definition of sequence, two sequences $\sigma:I\to A$ and $\sigma':I\to A$ are __equal__ if and only if
$$
\forall k\in I, \ \sigma(k)=\sigma'(k)
$$
(Note that two sequences of different length cannot be equal, since the corresponding functions cannot possibly be equal)

By definition of concatentation, it is easy to verify that, for any sequence $\sigma$,
$$
\epsilon\circ\sigma=\sigma
$$
and if $\sigma$ is finite, then
$$
\sigma\circ\epsilon=\sigma
$$
