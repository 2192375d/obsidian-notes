---
title: expected value properties
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:13
tags:
  - probability/expected-value
course:
  - STAB52
LEC: 8
---
# theorem
Expected values are linear:
Let $X,Y$ be RVs, then
$$
E(aX+bY)=aE(X)+bE(Y)
$$
Moreover, for independent RVs $X,Y$
$$
X\perp Y\to E[X\times Y]=E[X]\times E[Y]
$$
_example_
Two processes run serially (one after the other) on the same computer and take i.i.d. $Geometric*(0.5)$ times to complete.
Find the average time until both processes complete

_example_
$n$ people throw their keys in a box, and each one picks a random set of keys. Find the expected number of people who get back their own key.
