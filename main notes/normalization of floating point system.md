---
title: normalization of floating point system
created: Sunday 24th August 2025 00:42
last_modified: Sunday 24th August 2025 00:42
aliases: []
tags:
  - computer-science/floating-point-system
course: CSCC37
---
# normalization
A floatingpoint system is said to be __normalized__ if the leading digit $d_{0}$ is always __nonzero__ unless the number is zero.
In other words, the mantisa $m$ of a nonzero floating-point number always satisfies
$$
1\leq m\leq \beta
$$

We usually normalize a floating point number system because:
- the representation of each number is unique
- no digits wasated on leading zeros (maximize precision)