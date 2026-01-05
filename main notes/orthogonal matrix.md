---
title: orthogonal matrix
created: Friday 21st November 2025 01:33
last_modified: Friday 21st November 2025 01:33
aliases:
  - orthogonal linear transformation
tags:
  - math/linear-algebra/inner-product/norm
---

# orthogonal matrix (definition)
Let $A \in \mathcal{M}(\mathbb{R}^n)$, then $A$ is __orthogonal__ if
$$
A^TA=I
$$

## orthogonal matrix property
Let $A\in\mathcal{M}(\mathbb{R}^n)$, then the followings are equivalent
- The rows of $A$ form an orthonormal basis of $\mathbb{R}^n$
- The columns of $A$ form an orthonormal basis of $\mathbb{R}^n$
- $A$ is orthogonal

Also,
Suppose $A,B$ are orthogonal matrices in $\mathcal{M}(\mathbb{R}^n)$, then
- $A^T$ is orthogonal
- $\det(A)=\pm 1$
- $AB$ is orthogonal

## multiplication by orthogonal matrix
Let $A\in\mathcal{M}(\mathbb{R}^n)$ be an orthogonal matrix, and $x,y\in\mathbb{F}^n$, then
- $(Ax)(Ay)^T=y^Tx$
- $||Ax||=||x||$
- The angle between $x$ and $y$ is the angle between $Ax$ and $Ay$, for any nonzero vectors $x,y$

## symmetric matrix properties
Let $M$ be a real symmetric matrix, then eigenspaces of $A$ are orthogonal with each other

## orthogonal diagonalization
Let $A$ be a real symmetric matrix, then $A$ is diagonalizable, and it's diagonalization $C^{-1}AC=D$ can be achieved suing a real orthogonal matrix $C$

Also,
Consider $CAC^{-1}=D$
Let $C$ be an orthogonal matrix, $D$ be a diagonal matrix, then we can get $A$ from above as a symmetric matrix, called an __orthogonal diagonalization__

# orthogonal linear transformation
Let $V$ be an inner product space, $T\in\mathcal{L}(V)$
Then $T$ is __orthogonal__ if
$$
\langle T(v),T(w)\rangle=\langle v,w\rangle
$$
for any $v,w\in V$

## orthogonal linear transformation property
Let $T$ be orthogonal, then
- $||T(x)||=||x||$
- The angle between $x$ and $y$ is the angle between $T(x)$ and $T(y)$, for any nonzero vectors $x,y$