---
title: orthonormal bases
created: Friday 21st November 2025 00:36
last_modified: Friday 21st November 2025 00:36
aliases:
  - Gram Schmidt Procedure
  - Rietz representation theorem
tags:
  - math/linear-algebra/inner-product/norm
---
# orthonormal (definition)
A set $S$ of vectors is called __orthonormal__ if $S$ satisfies
$$
\langle e_{j},e_{k}\rangle=\begin{cases}
1 ,j=k\\
0,j\neq k
\end{cases}
$$
where $S=\{ e_{1},\dots,e_{m} \}$, $0\leq j,k\leq m$

## norm of an orthonormal linear combination
Let $e_{1},\dots,e_{m}$ be an orthonormal list of vectors in $V$, then
$$
||a_{1}e_{1}+\dots+a_{m}e_{m}||^2=|a_{1}|^2+\dots+|a_{m}|^2
$$
(literally by Pythagorian Theorem applied $m-1$ times)

# orthonormal bases (definition)
An __orthonormal basis__ of $V$ is an orthonormal list of vectors in $V$ that is also a basis of $V$

(Note that every orthonormal list of vectors in $V$ with cardinality = $dim(V)$ is an orthonormal basis of $V$)

## vector written as linear combination of orthonormal basis
Let $e_{1},\dots,e_{n}$ be an orthonormal basis of $V$ and $v\in V$, then
$$
\begin{align}
v=\langle v,e_{1}\rangle e_{1}+\dots+\langle v,e_{n}\rangle e_{n}  \\
||v||^2=|\langle v,e_{1}\rangle|^2+\dots+|\langle v,e_{n}\rangle|^2  
\end{align}
$$

### proof
Since $e_{1},\dots,e_{n}$ is a basis of $V$, then
$$
v=a_{1}e_{1}+\dots+a_{n}e_{n}
$$
for some $a_{1},\dots,a_{n}\in\mathbb{F}$
Take inner product with $e_{j}$ on both side, we get $\langle v,e_{j}\rangle=a_{j}$, as wanted
(the second part is trivial)

## Gram-Schmidt Procedure (GSP)
Let $v_{1},\dots,v_{m}$ be a linearly independent list of vectors in $V$, $\displaystyle e_{1}=\frac{v_{1}}{||v_{1}||}$
For $j=2,\dots,m$, define $e_{j}$ inductively by
$$
e_{j}= \frac{v_{j}-\langle v_{j},e_{1}\rangle e_{1}-\dots-\langle v_{j},e_{j-1}\rangle e_{j-1}}{||v_{j}-\langle v_{j},e_{1}\rangle e_{1}-\dots-\langle v_{j},e_{j-1}\rangle e_{j-1}||}
$$
Then $e_{1},\dots e_{m}$ is an orthonormal list of vectors in $V$ S.T.
$$
\operatorname{span}(v_{1},\dots,v_{j})=\operatorname{span}(e_{1},\dots,e_{j})
$$
for $j=1,\dots,m$


## existence of orthonormal basis
Every fininte-dimensional inner product space has an orthonormal basis

(easily proven by Gram-Schmidt Procedure)


## orthonormal list extends to orthonormal basis
title

### proof
Every orthonormal list is linearly indepdent, thus it can be extended to a basis, apply Gram-Schmidt process on that basis you will get a orthonormal basis with the first few components from the original orthonormal list


## upper triangular matrix with respect to orthonormal basis
Let $T\in\mathcal{L}(V)$, if $T$ has an upper triangular matrix with respect to some basis of $V$, then $T$ has an upper-triangular matrix with respect to some orthonormal basis of $V$

(Another result of GSP)

## Schur's theorem
Let $V$ be a finite dimensional _complex_ vector space and $T\in\mathcal{L}(V)$
Then $T$ has an upper-triangular matrix with respect to some orthonormal basis of $V$


## Riesz representation theorem
Let $V$ be a finite dimensional vector space, $\varphi$ be a linear functional on $V$, then there is a unique vector $u\in V$ S.T.
$$
\varphi(v)=\langle v,u\rangle
$$
for every $v\in V$