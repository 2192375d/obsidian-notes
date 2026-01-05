---
title: linear system estimating accuracy
created: Thursday 28th August 2025 10:11
last_modified: Thursday 28th August 2025 10:11
aliases: []
tags:
  - computer-science/approximation
  - math/linear-algebra/matrix
course: CSCC37
---

# estimating accuracy
To find the relative accuracy of a linear system $Ax=b$, where the solution achieved is $\hat{x}$
we make use of condition to bound the relative error of solution $\hat{x}$, with $A \hat{x}=\hat{b}$
$$
\frac{||\hat{x}-x||}{||x||}\leq cond(A)\frac{||\hat{b}-b||}{||b||}
$$

A similar result holds if $Ax=b$ and $(A+E)\hat{x}=b$
$$
\frac{||\hat{x}-x||}{||x||}\leq cond(A)\frac{||E||}{||A||}
$$


## proof (?)
Note that $A\hat{x}=b-r$ and $Ax=b$, 
Thus, $A(x-\hat{x})=r\iff(x-\hat{x})=A^{-1}r$
We get, $||x-\hat{x}||=||A^{-1}r||\leq ||A^{-1}||\ ||r||$ (\*)

Also note that $b=Ax \iff||b||=||Ax|| \iff ||b||\leq ||A||\ ||x||$ (\*\*)
Combining (\*) and (\*\*), we get 
$$
\begin{align}
&||x-\hat{x}||\leq ||A^{-1}|| \ ||r|| \\
\iff& \frac{||x-\hat{x}||}{||A|| \ ||x||}\leq \frac{||A^{-1}|| \ ||r||}{||b||} \\
\iff& \frac{||x-\hat{x}||}{||x||}\leq||A||\ ||A^{-1}|| \frac{||r||}{||b||} = cond(A) \frac{||r||}{||b||}
\end{align}
$$
