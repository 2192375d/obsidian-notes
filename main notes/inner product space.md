---
title: inner product space
created: Saturday 11th October 2025 22:29
last_modified: Saturday 11th October 2025 22:29
aliases:
  - angle between vectors
tags:
  - math/linear-algebra/inner-product
course:
  - MATB24
LEC:
  - "6"
---
(angle between vectors is at the end)

# inner product space
Inner product space is a vector space that satisfies:
Let $u,v,w\in V$, $c\in\mathbb{F}$
- positivity: $\langle u, u\rangle\geq 0$
- definiteness: $\langle u,u\rangle = 0$ iff $u=0$
- additivity in first slot: $\langle u+v, w \rangle=\langle u, v \rangle+\langle u, w \rangle$
- homogeneity in first slot: $\langle cu, v\rangle=c\langle u, v \rangle$
- conjugate symmetry: $\overline{\langle u,v\rangle}=\langle v,u\rangle$

## example
An inner product space on $\mathbb{R}^n$ has the inner product defined as the dot product
An inner product space on $\mathcal{P}_{n}([0,1])$ has the inner product defined as 
$$
\displaystyle \langle p(x),q(x)\rangle=\int_{0}^1p(x)q(x)dx
$$
An inner product space on $\mathbb{C}^n$ has the inner product defined as
$$
\langle v,w\rangle= \sum_{i=1}^n \overline{v_{i}}w_{i}
$$

## inner product properties (theorem)
Let $V$ be an inner product space over $\mathbb{F}$, then
- For each fixed $u\in V$, the function that takes $v$ to $\langle v,u\rangle$ is a linear map from $V$ to $\mathbb{F}$
- $\langle 0,u\rangle=0$ for every $u\in V$
- $\langle u,0\rangle=0$ for every $u\in V$
- $\langle u,v+w\rangle=\langle u,v\rangle+\langle u,w\rangle$ for all $u,v,w\in V$
- $\langle u,\lambda v\rangle= \bar{\lambda}\langle u,v\rangle$ for all $\lambda\in\mathbb{F}$ and $u,v\in V$

### proof
- Let $u \in V$, then define $T(v)=\langle v,u\rangle$, by additivity and homogeneity in the first slot, $T$ is linear
- Define $T$ as above, then by $T(0)=0$, this follows
- Define $T$ as above, then by $T(0)=0$ and conjugate symmetry property, this follows
- Let $u,v,w \in V$, then
$$
\begin{align}
\langle u,v+w\rangle&= \overline{\langle v+w,u\rangle} \\
&= \overline{\langle v,u\rangle+\langle w,u\rangle} \\
&= \overline{\langle v,u\rangle}+\overline{\langle w,u\rangle} \\
&= \langle u,v\rangle+\langle u,w\rangle
\end{align}
$$
- (similarly the last one can be easily proven)

# angle between vectors
Let $V$ be an inner product space and let $\mathbf{v},\mathbf{w}\in V$, then the angle $\theta$ between $\mathbf{v}$ and $\mathbf{w}$ is defined to be 
$$
\cos\theta=   \frac{\langle\mathbf{v},\mathbf{w}\rangle}{||\mathbf{v}||||\mathbf{w}|| }
$$
