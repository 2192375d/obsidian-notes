---
title: condition of error
created: Friday 22nd August 2025 23:25
last_modified: Friday 22nd August 2025 23:25
aliases:
  - relative error approximation
  - absolute error approximation
tags:
  - computer-science/approximation/error
course: CSCC37
---
# conditioning
The condition number of $f$ at $x$ is
$$
\text{cond}=\frac{|\text{relative change in solution}|}{|\text{relative change in input data}|}=\frac{|(f(\hat{x})-f(x))/f(x)|}{|(\hat{x}-x)/x|}
$$
This value indicates how much solution changes upon changing the input

## approximating condition
Note that for $\hat{x}$ close to $x$, eg $\hat{x}=x+h$ for some small $h$, we get
$$
\text{aboslute error}=f(x+h)-f(x)\approx hf'(x)
$$
and
$$
\text{relative error}=\frac{f(x+h)-f(x)}{f(x)}\approx h \frac{f'(x)}{f(x)}
$$
Thus,
$$
\text{cond}=\left| \frac{hf'(x)/f(x)}{h /x}\right|=\left|x \frac{f'(x)}{f(x)}\right|
$$
The condition number is denoted as $\displaystyle K_{f(x)}=\left|\frac{xf'(x)}{f(x)}\right|$

from this, we can get for $f(x)=e^x$, the absolute error is around $he^x$, the relative error is around $h$ and the cond is around $|x|$ (the greater the $x$, the quicker the change)