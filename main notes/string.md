---
title: string
created: Sunday 3rd August 2025 12:52
last_modified: Sunday 3rd August 2025 12:52
aliases:
  - alphabet
tags:
  - math/set-theory/sequence
  - computer-science/string
course:
  - CSCB36
---
# alphabet
An __alphabet__ is a nonempty set $\Sigma$, where the elements of the alphabet are __symbols__.

# string
A __string__ over alphabet $\Sigma$ is a finite sequence over $\Sigma$
By convention, when we want to write the sequence (string) $(0,1,0,0)$, instead we write $0100$ as a string.
The empty sequence as a string is still denoted as $\epsilon$. 
The set of all strings over alphabet $\Sigma$ is denoted $\Sigma^*$ (Note that although each string is a finite sequence, individual strings have an arbitrary length thus $\Sigma^*$ is an infinite set)

## substring
The corresponding term to contiguous subsequence (note it's not sequence!)
For any $\sigma,\tau\in \Sigma^*$, $\sigma$ is a substring of $\tau$ if and only if
$$
\exists \sigma',\sigma''\in \Sigma^* \text{ S.T. }\tau=\sigma'\sigma \sigma''
$$