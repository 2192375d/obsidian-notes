---
title: merge sort
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 05:32
tags:
  - computer-science/algorithm/sort
  - computer-science/recursion
course:
  - CSCA48
---
# merge sort
Merge sort is one of the algorithms that implement the __conquer and divide__ method

Consider sorting $\{ 5,1,8,3,4,2,7,6 \}$
- First split the array in halfs: $\{ 5,1,8,3 \},\{ 4,2,7,6 \}$
- Then sort individual arrays: $\{ 1,3,5,8 \},\{ 2,4,6,7 \}$
- Compare the first index in both arrays, take the smallest and put it in the new array:
we have $\{ 1 \}$, with individual arrays $\{ 3,5,8 \}\{ 2,4,6,7 \}$, as $1<2$
we have $\{ 1,3 \}$, with individual arrays $\{ 3,5,8 \}\{ 4,6,7 \}$, as $2<3$ 
we have $\{ 1,2,3 \}$, with individual arrays $\{ 5,8 \}\{ 4,6,7 \}$, as $3<4$
...
And so on, until both arrays are empty.

This is one way of doing this, however, merge sort is usually done by repeating the first step until we split everything to a bunch of arrays of size $1$

Note that the worst case scenario complexity is $O(N\log_{2} N)$

Here is a general pseudocode for merge sort
```
mergesort(input_array)
	if length of input_array <= 1, return input_array
	
	split array into 2 sub-arrays: lower_half and upper_half
	sorted_low = mergesort(lower_half)
	sorted_high = mergesort(upper_half)
	
	merge in sorted order the two sub-arrays sorted_low and sorted_high, and return it
```
Here is a general explanation for why sorting complexity is $O(N\log_{2}N)$:
- It takes $\log_{2}(N)$ splits to reduce the input array to sub-arrays of size 1
- Merging each split takes $N$ steps

()
## time efficiency
[[merge sort time complexity]]
all cases: $O(N\log N)$