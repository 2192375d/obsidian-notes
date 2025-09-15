---
title: recursion stack
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 05:53
tags:
  - computer-science/recursion
course:
  - CSCA48
---
In terms of memory model, recursion is very tricky, as it calls itself a LOT of times. The idea of calling itself means everytime we call the function, space has to be reserved for the function's parameters, variables, and return value.
This is something we never cared about in non-recursive code, as space reserved will be immediately released after the return statement.
For recursion though, those space will hang around until the last call is reached.

_example_
Consider the following pseudocode that calculates sum of an array
```
sum(array, n)
	if(n == 0) return array[0]
	else return array[n] + sum(array, n - 1)
```

Let's say we call the function with array $[10,5,3,2,1,8]$,

Then, the first call will be
Sum([10,5,3,2,1,8],5)
Next it will be
Sum([10,5,3,2,1,8],4)

To keeptrack of the two calls to Sum(), the program keeps track of it using a stack
![[Pasted image 20250715054459.png]]
This repeats until it reaches the top of stack with
Sum([10,5,3,2,1,8],0)
![[Pasted image 20250715054610.png]]
As this happens, Sum() finds the base case and returns array[0].
![[Pasted image 20250715054659.png]]
The process proceeds until terminating
![[Pasted image 20250715054722.png]]

At the end of the process, all active function calls are completed thus the stack is empty again.
If a recursion requires a lot of space, you can run into trouble by running out of them, called __stack overflow__

# so, what is a stack?
- Memories for a function in a program is stored in a stack
- The stack can only add/remove entries on the top of stack (e.g. you can't do anythig with the bottom of the stack without removing all entries)
- The part of the stack reserved for each function call is a stack frame
- The code can run out of stack space with recursive functions, if this happens, the program will terminate (crash or segfault or other weirdo stuffs)
- Using the stack, every recursive function calls get its own reserved space for variables, parameters, and return type.