---
title: iterative refinement
created: Monday 3rd November 2025 16:40
last_modified: Monday 3rd November 2025 16:40
aliases: []
tags:
  - math/linear-algebra/matrix
  - computer-science/approximation
course:
  - CSCC37
LEC:
  - "7"
---
# iterative refinement algorithm
Compute $\hat{x}^{(0)}$ by solving $Ax=b$ in the FPS
For $k=0,1,2,\dots$ until solution is "good enough"

Compute $r^{(k)}=b - A\hat{x}^{(k)}$
Solve $$