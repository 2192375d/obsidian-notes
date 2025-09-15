---
title: multivariable chain rule
created: Monday 11th August 2025 13:36
last_modified: Monday 11th August 2025 13:36
aliases: 
tags:
  - calculus/multivariable
  - calculus/derivative
course:
  - MATB41
---

# Chain rule
Let $U\subset\mathbb{R}$ and $V\subset\mathbb{R}^k$ be open sets. 
Let $g:U\subset\mathbb{R}^n\rightarrow\mathbb{R}^k$  and $f:V\subset\mathbb{R}^k\rightarrow\mathbb{R}^m$. 
Assume that $g(U)\subset V$ so that $f\circ g:U\subset\mathbb{R}^n\rightarrow\mathbb{R}^m$ is defined on all of $U$.
If $g$ is differentiable at $\mathbf{x}_0$ and $f$ is differentiable at $\mathbf{y}_0=g(\mathbf{x}_0)$, then $f\circ g$ is differentiable at $\mathbf{x}_0$ and 
$$
\mathbf D(f\circ g)(\mathbf{x}_0)=\mathbf Df(\mathbf{y}_0)\mathbf Dg(\mathbf{x}_0)
$$
## Chain rule and gradients
If $\mathbf{c}:\mathbb{R}\to\mathbb{R}^k$ is a path and $f:\mathbb{R}^k\to\mathbb{R}$ is a real valued function, then $$\mathbf{D}(f\circ c)= \mathbf{D}f(\mathbf{c}(t))\cdot\mathbf{Dc}(t) = \nabla f(\mathbf{c}(t)) \cdot \mathbf{c}'(t).$$
Note that the result above is a dot product
