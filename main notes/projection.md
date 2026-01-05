---
title: projection
created: Wednesday 19th November 2025 16:28
last_modified: Wednesday 19th November 2025 16:28
aliases: []
tags:
  - math/linear-algebra/inner-product
---
# projection (on one vector)
Let $V$ be an inner product space and $W=span(a)$ be a subspace of $V$, then projection of $b$ on $\operatorname{span}(a)$ is
$$
\mathbf{p}=\operatorname{proj}_{\mathbf{a}}\mathbf{b}=||\mathbf{b}||\cos\theta \frac{ \mathbf{a}}{||\mathbf{a}||}
$$
where in $\mathbb{R}^n$,
$$
\mathbf{p}=||\mathbf{b}||\cos \theta \frac{\mathbf{a}}{||\mathbf{a}||}=\frac{||\mathbf{b}||||\mathbf{a}||\cos\theta}{||\mathbf{a}||||\mathbf{a}||}\mathbf{a}=\frac{\mathbf{b}\cdot \mathbf{a}}{\mathbf{a}\cdot \mathbf{a}}\mathbf{a}
$$
and in finite dimensional inner product space $V$:
$$
\operatorname{proj}_{\mathbf{a}}(\mathbf{b})= \frac{\left\langle  \mathbf{b},\mathbf{a} \right\rangle}{\langle \mathbf{a},\mathbf{a}\rangle}\mathbf{a}
$$

## projection (on a subspace)
Let $V$ be an inner product space and $W=span(v_{1},\dots,v_{m})$ be a subspace of $V$, were $(v_{1},\dots,v_{n})$ is an orthogonal basis of $W$, then projection of $b$ on $W$ is
$$
proj_{W}(b)=\sum_{i=1}^m \frac{b \cdot v_{i}}{v_{i}\cdot v_{i}}v_{i}
$$
The idea behind is that you project the $b$ on each vector in the basis, and take the sum of it.

# orthogonal projection
Let $V$ be a vector space, $U$ be subspace of $V$
Then the __orthogonal projection__ of $V$ onto $U$ is the operator $P_{U}\in\mathcal{L}(V)$ defined as

For every $v\in V$, if we write $v=u+w$, where $u \in U$ and $v \in U^{\perp}$, then
$$
P_{U}(v)=u
$$

## orthogonal project properties
Let $U$ be a finite-dimensional subspace of $V$ and $v\in V$, then
- $P_{U}\in\mathcal{L}(V)$
- $range(P_{U})=U$
- $null(P_{U})=U^T$
- $v-P_{U}(v)\in U^{\perp}$
- $P_{U}^2=P_{U}$
- $||P_{U}(v)||\leq ||v||$
- for every orthonormal basis $e_{1},\dots,e_{m}$ of $U$,
$$
P_{U}(v)=\langle v,e_{1}\rangle e_{1}+\dots+\langle v,e_{m}\rangle e_{m}
$$


