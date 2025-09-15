---
title: binary search algorithm
created: Before 28th July, 2025
last_modified: Monday 7th July 2025 21:26
tags:
  - computer-science/algorithm/search
course:
  - CSCA48
---
Assuming given array is sorted, then,
Binary search algorithm is done by:
1. Go to the entry at the middle of the current array (index $\lfloor N/2 \rfloor$)
2. Compare current entry with the query term, if they match, return the index of this term
3. if current array has only one entry, then return -1
4. if query term < middle entry, then change current array to first half ($0$ to $\lfloor N/2 \rfloor-1$, and go back to step 1. Otherwise, change current array to latter half ($\lfloor N/2 \rfloor+1$ to $N-1$), go back to step 1)

best case: $O(1)$
average case: $O\left( \frac{N}{2} \right)$
worst case: $O(\log_{2}N)$
