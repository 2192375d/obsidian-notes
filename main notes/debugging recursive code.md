---
title: debugging recursive code
created: Before 28th July, 2025
last_modified: Saturday 26th July 2025 18:53
tags:
  - computer-science/recursion
  - computer-science/debug
course:
  - CSCA48
---
# todos before debugging
- Review all base cases are covered in the implementation
- Review the recursive case (splitting) is reasonable, and implemented properly.

# tracing recursive code
The problem is that the same functiong ets called over and over, so you need additional info to figure out which of the many recursive calls is not doing the right thing.

How to do that?

Add a new parameter __depth__ in your recursive function, increase it everytime by 1. Why? The depth variable tells us at what level in the recursion process caused the bug.
With this, we can use a debugging tool (such as __gdb__) or __printf__ to deal with the problem.
![[Pasted image 20250726184951.png]]
(just practice lol)

# common problems with recursion
- __It never reaches base case__ (happens when depth is going too high): Double check the recursive case, make sure it's making the problem smaller, and make sure base cases are identified.
- __It runs out of stack space for recursive calls__ (happens when large problems which require very deep sequences of recursive calls): Use depth to enforce a maximum allowed recursion depth.
- __Incorrect return value__: Check if base case returns a reasonable result, and check the process of building a bigger solution from the smaller one.