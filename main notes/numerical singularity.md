---
title: numerical singularity
created: Monday 20th October 2025 14:35
last_modified: Monday 20th October 2025 14:35
aliases: []
tags: []
course:
  - CSCC37
LEC:
  - "6"
---
# numerical singularity (exact singularity)
During nuemrical facotrization in a FPS, usually we cannot expect exact zeros, but "near singular"
If all elements below the diagonal in column k (and $\hat{a}_{kk}$) at the kth stage of magnitude needs to satisfy
$$
< \epsilon_{mach} \max_{1\leq j < k}|u_{jj}|
$$

(as the threshold)