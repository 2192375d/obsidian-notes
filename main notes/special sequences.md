---
title: special sequences
created: Sunday 3rd August 2025 12:44
last_modified: Sunday 3rd August 2025 12:44
aliases:
  - subsequence
  - contiguous subsequence
  - prefix of sequence
  - suffix of sequence
tags:
  - math/set-theory/sequence
course:
  - CSCB36
---
## subsequence
Let $A$ be a set, $I,J$ be initial segments of $\mathbb{N}$ S.T. $|I|\leq|J|$ and $\sigma:I\to A, \ \tau:J\to A$ be sequences over $A$.
Then, $\sigma$ is a __subsequence__ of $\tau$ if there is an increasing function $f:I\to J$ S.T.
$$
\forall i\in I, \ \sigma(i)=\tau(f(i))
$$

If $\sigma$ is a __subsequence__ of $\tau$ and $\sigma\neq \tau$, then we say $\sigma$ is a __proper subsequence__ of $\tau$

## contiguous subsequence
the sequence $\sigma$ is a __contiguous subsequence__ of sequence $\tau$ if
$$
\exists j\in\mathbb{N}\text{ S.T. }\forall i\in I, \ \sigma(i)=\tau(i+j)
$$

## prefix
A sequence $\sigma$ is a __prefix__ of sequence $\tau$, if either ($\sigma$ is finite and $\exists \sigma'$ S.T. $\sigma\circ\sigma'=\tau$) or ($\sigma$ is infinite and $\sigma=\tau$)
if $\sigma$ is a prefix of $\tau$ and $\sigma\neq \tau$, then $\sigma$ is a __proper prefix__ of $\tau$

## suffix
(pretty much the same as prefix, but with $\sigma'\circ\sigma$ (order flipped))