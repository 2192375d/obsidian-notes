---
title: program correctness proof example (termination)
created: Saturday 27th September 2025 14:07
last_modified: Saturday 27th September 2025 14:07
aliases: []
tags:
  - computer-science/computation-logic/program-correctness
course:
  - CSCB36
LEC:
  - "4"
---
# program correctness proof example (termination)
Consider the following code and specification:
- precondtiion: $x,y\in\mathbb{N}$
- postcondition: True

```
while x != 0 or y != 0 do
	if x != 0 then
		x = x - 1
	else
		x = 16
		y = y - 1
	end if
end while
```

# step 1: define LI
a) $0\leq x\leq \max(x_{0},16)$
b) $0\leq y\leq y_{0}$

# step 2: prove LI holds
(stuffs)

# step 3: prove partial correctness
(too obviously true, __you can skip it!__)

# step 4: expression for $e$
~~Let e=x+y~~
~~Let e=x+16y (put more weights on y maybe?)~~
Let $e=x+17y$ (put ay weight more than 16 to guarentee decreasing)

# step 5: prove $e$ is decreasing and $e$ 
(stuffs)



