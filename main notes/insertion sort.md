---
title: insertion sort
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 05:33
tags:
  - computer-science/algorithm/sort
  - computer-science/recursion
course:
  - CSCA48
---
# insertion sort
Insertion sort sorts the array by repeatedly increasing the size a sorted array until it has the size of N.

- Set $i = 1$
- Insert entry $i$ to the array from $0$ to $i - 1$, in the exact location so that it is sorted
- $i = i +1$

```
void array_insertion_sort(int array[], int N) {
    int temp = 0;
    int index = 0;
	
    for (int i = 1; i < N; i++) {
		
        temp = array[i];
        index = i - 1;
		
        while (index >= 0 && temp < array[index]) {
            array[index + 1] = array[index];
            index--;
        }
		
        array[index + 1] = temp;
    }
}
```

## time complexity
worst case (sorted backward): $1+2+\dots+N\to O(N^2)$
average case: $O(N^2)$
best case (sorted forward): $O(N)$
