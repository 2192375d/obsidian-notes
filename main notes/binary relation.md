---
title: binary relation
created: Before 29th July, 2025
last_modified: Tuesday 29th July 2025 01:08
tags:
  - math/set-theory/relation
course:
  - CSCB36
---
# binary relations from B36 tb (0.5)
binary relations can be described using __directed graphs__. Consider $A\times B$:
$$
\{ A\times B={(a,b):a\in A,b\in B} \}
$$
and binary relation $R$ between $A$ and $B$,
## Important types of binary relations
<u>reflecive relation</u>
$R$ is __reflexive__ if 
$$
\forall a\in A,(a,a)\in R
$$
<u>symmetric relation</u>
$R$ is __symmetric__ if 
$$
\forall a,b\in A,(a,b)\in R \to (b,a)\in R
$$

<u>antisymmetric relation</u>
R is __antisymmetric__ if
$$
\forall a,b\in A,a\neq b,(a,b)\in R\to(b,a)\not\in R
$$

Note that a set can be neither symmetric nor antisymmetric, for example 
$$
R=\{ (a,b): \text{ $a$ and $b$ are persons with the same parents and $a$ is male} \}
$$

<u>transitive relation</u>
$R$ is __transitive__ if 
$$
\forall a,b,c\in A,(a,b)\in R \text{{ and }}(b,c)\in R \to (a,c)\in R
$$

<u>equivalence relation</u>
$R$ is an __equivalence relation__ if it is relfexive, symmetric and transitive

_example_
$a\equiv_{m} b$ is a equivalence relation, for every integer $m$

<u>partial order</u>
$R$ is a __partial order__ if it is antisymmetric and transitive.

<u>total order</u>
$R$ is a __total order__ if it is a partial order and
$$
\forall a,b\in A, \text{ either } (a,b)\in R \text{ or }(b,a)\in R
$$
_example_
The following $R$ is a total order
$$R=\{ (a,b): \text{ $a$ and $b$ are persons and $a$'s SIN is smaller than $b$'s } \}$$





# equivalence class from CSCB36 tb (0.5)
Let $R$ be an equivalence relation and $a$ be an element of $A$, then the __equivalence class__ of $a$ under $R$ is defined as a set 
$$
R_{a}=\{ b:(a,b)\in R \}
$$
## equivalence class properties
- $\forall a\in A,R_{a}\neq \emptyset$
- if $R_{a} \neq R_{b}$, then $R_{a}\cup R_{b}=\emptyset$

