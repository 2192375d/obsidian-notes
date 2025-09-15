---
title: gradiant has direction of fastest increase
created: Monday 11th August 2025 13:39
last_modified: Monday 11th August 2025 13:39
aliases: 
tags:
  - calculus/derivative
  - calculus/multivariable
  - theorem
course:
  - MATB41
---
# Theorem: $\nabla f$ is the direction of fastest increase
Suppose that $f: \mathbb{R}^n \to \mathbb{R}$ is differentiable at $\mathbf{x}_0$ and $\nabla f(\mathbf{x}_0) \neq 0$.

The maximum value of the directional derivative of $f$ at $\mathbf{x}_0$ is $\lVert \nabla f(\mathbf{x}_0) \rVert$ and it occurs in the direction of the unit vector
$$\mathbf{n} = \frac{\nabla f(\mathbf{x}_0)}{\lVert \nabla f(\mathbf{x}_0) \rVert}.$$
The minimum value of the directional derivative of $f$ at $\mathbf{x}_0$ is $-\lVert\nabla f(\mathbf{x}_0)\rVert$ and it occurs in the direction of the unit vector $-\mathbf{n}$.