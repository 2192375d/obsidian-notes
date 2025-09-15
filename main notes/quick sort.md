---
title: quick sort
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 01:50
tags:
  - computer-science/algorithm/sort
course:
  - CSCA48
---
# quick sort
Quick sort performs divide and conquer towards the array.
It breaks down the "current" array to left and right size. All elements on the left size are smaller to the pivot of the array and right side greater than pivot (note pivot is randomly selected).
It recursively does that until the reaching base case (N <= 1), then it starts to reassemble them by grouping left side, pivot, right side in the order.

```
void array_quick_sort(int array[], int N) {
    if (N <= 1) {
        return;
    }
	
    int pivot_value = array[N / 2];
    int array_left[N - 1];
    int array_right[N - 1];
    int count_left = 0;
    int count_right = 0;
	
    for (int i = 0; i < N; i++) {
        if (i == N / 2) {
            continue;
        }
	
        if (array[i] <= pivot_value) {
            array_left[count_left] = array[i];
            count_left++;
        } else {
            array_right[count_right] = array[i];
            count_right++;
        }
    }
	
    array_quick_sort(array_left, count_left);
    array_quick_sort(array_right, count_right);
	
    for (int i = 0; i < count_left; i++) {
        array[i] = array_left[i];
    }
    array[count_left] = pivot_value;
    for (int i = 0; i < count_right; i++) {
        array[i + count_left + 1] = array_right[i];
    }
}
```

## time efficiency
(slightly faster than merge sort and heapsort for randomized data)
worst case: $O(N^2)$
average and best case: $O(N\log N)$