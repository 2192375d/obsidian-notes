---
title: directional derivative
created: Monday 11th August 2025 13:37
last_modified: Monday 11th August 2025 13:37
aliases: 
tags:
  - calculus/derivative
  - calculus/multivariable
course:
  - MATB41
---


# Directional derivatives
Suppose that $f: \mathbb{R}^n \to \mathbb{R}$. The **directional derivative** of $f$ at $\mathbb{x}$ along the **unit vector** $\mathbb{v}$ is given by
$$\mathbf{D}_\mathbf{v} f(\mathbf{x}) = \frac{\mathrm{d}}{\mathrm{d}t}f(\mathbf{x} + t\mathbf{v}) \Bigg\rvert_{t=0} = \lim_{t \to 0} \frac{f(\mathbf{x} + t\mathbf{v}) - f(\mathbf{x})}{t}.$$
Note that $\mathbf{D}_{\mathbf{v}}f(\mathbf{x})=\nabla f(\mathbf{x})\cdot\mathbf{v}$