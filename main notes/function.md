---
title: function
created: Wednesday 30th July 2025 21:42
last_modified: Wednesday 30th July 2025 21:42
aliases: 
tags:
  - math/set-theory/function
course:
  - CSCB36
---
# function from B36 tb (0.6)
A relation  $f\subset A\times B$ is a __function__ if
$$
\forall a\in A,\exists! b\in B \text{ S.T. }(a,b)\in f
$$
Note that in this context, $f$ is also a set
Denoted as $f:A\to B$

## domain and range and map
For $f:A\to B$, we call $A$ as the __domain__ of the function, $B$ as the __range__ of he function.
If $(a,b)\in f$, then we say $A$ __maps to__ $b$ (under $f$), and we write $f(a)$ to denote $b$ (note that $f(a)$ is well-defined since $b\in B$ is unique)

## surjective and injective
$f:A\to B$ is an __onto__ (or __surjective__) function if
$$
\forall b\in B, \exists a\in A \text{ S.T. }f(a)=b
$$
$f:A\to B$ is an __into__ (or __injective__) function if
$$
\forall b\in B,\exists!a\in A \text{ S.T. }f(a)=b
$$
$f$ is __bijective__ if it is both injective and surjective.
Note that if $f:A\to B$ is a bijection, then $|A|=|B|$

## restriction
The __restriction__ of a function $f:A\to B$ to a subset $A'\in A$, is a function $f':A'\to B$ S.T.
$$
\forall a\in A',f'(a)=f(a)
$$
Denoted as $f|A'$
By definition of equality of relation, $f=f'\leftrightarrow \forall a\in A,f(a)=f'(a)$
