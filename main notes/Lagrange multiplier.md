---
title: Lagrange Multiplier
created: Monday 11th August 2025 13:54
last_modified: Tuesday 29th July 2025 00:44
aliases: 
tags:
  - calculus/multivariable
  - calculus/optimization
  - theorem
course:
  - MATB41
---
Lagrange multiplier is used when we want to find the local extremas of a function $f\in C^1$ restricted to some level set
$$
L_{c}=\{ \mathbf{x}:g(\mathbf{x})=c \}
$$
, where $g\in C^1$

#### theorem
if $f|L_{c}$ has a local extrema at $\mathbf{x}_{0}\in L_{c}$, then
$$
\nabla f(\mathbf{x_{0}})=\lambda \nabla g(\mathbf{x_{0}})
$$
, for some real number $\lambda$, the number $\lambda$ is called a __langrange multiplier__
