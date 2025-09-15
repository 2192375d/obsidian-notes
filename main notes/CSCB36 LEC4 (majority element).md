<h3> <u>majority element</u> </h3>
Given a list A and an element x, x is a majority element if
<p style="text-align:center;">x occurs in A more than len(A)/2 times</p>
<h5> example </h5>
Suppose we want to prove the following:
<i>precondition:</i> A is a list (possibly empty)
<i>postcondition:</i> Return majority element of A if it exists, return NONE otherwise

Here is a simple program as solution:
```
e = NONE
for i in range(len(A)):
	count = 0
	for j in range(len(A)):
		if A[j] == A[i]
			count += 1
	if count > len(A)/2:
		e = A[i]
return e
```

This algorithm has a run-time of $O(n^2)$, here is a $O(n)$ algorithm
```
# part 1
m = 0
e = NONE

for i in range(len(A)):
	if m == 0::
		m = 1
		e = A[i]
	elif A[i] == e:
		m += 1
	else:
		m -= 1

# part 2
count = 0
for j in range(len(A)):
	if A[j] == e:
		count += 1
if count > len(A)/2:
	return e
else:
	return None
```

__How to prove this second algorithm is correct?__
For part 1: 
<i>precondition</i>: A is a list.
<i>postcondition</i>: if A has a majority element, then it is e.

To prove this, consider the following LI:
1. $0\leq i\leq len(A)$
2. $m\geq 0$
3. if $m=0$, then $A[0:i]$ has no majority element
4. if m > 0, then $A[0:i]$ contains at lease $m$ copies of $e$ and $A[0:i]$ with $m$ copies of $e$ removed has no majority element
