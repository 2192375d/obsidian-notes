---
title: rule of Sarrus
created: Sunday 19th October 2025 23:16
last_modified: Sunday 19th October 2025 23:16
aliases: []
tags:
  - math/linear-algebra/matrix
course:
  - MATB24
LEC:
  - "1"
---
# Rule of Sarrus
Consider computing
$$
\det \left(\begin{bmatrix}
a&b&c \\
d&e&f \\
g&h&i
\end{bmatrix}\right)
$$
Another way (non recursive method) of doing this is by rewriting the matrix as
$$
\begin{bmatrix}
a&b&c&a&b \\
d&e&f&d&e \\
g&h&i&g&h
\end{bmatrix}
$$
Then, multiply the diagonals a->i,b->g, c->h and the other way c->g, a->h, b->i, we get the determinant value
$$
\det \left(\begin{bmatrix}
a&b&c \\
d&e&f \\
g&h&i
\end{bmatrix}\right)=(aei+bfg+cdh-ceg-afh-bdi)
$$
