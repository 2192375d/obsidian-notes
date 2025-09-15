---
title: tail recursion
created: Before 28th July, 2025
last_modified: Tuesday 22nd July 2025 17:28
tags:
  - computer-science/recursion
course:
  - CSCA48
---
Tail recursion occurs when a recursive function's recursive step's ;ast return statement has no operation, simply returning the function itself

Similar to a non recursive function, tail recursion only occupies one stack frame. Because the computer is able to recognized that this is a tail recursion, thus removes previous call immediately since it serves no purpose, instead, just returns the next function call.
![[Pasted image 20250715060222.png]]

Thus, compared to regular recursion, tail recursion has the advantage of:
- recursive call no longer taking large amount of spaces in the stack
- The result is available as soon as we reach the base case, instead of passing it over lots of times until we get back to the first call. Resulting in a time usage of almost the same as a for loop.

This topic will be expanded by CSCC24
