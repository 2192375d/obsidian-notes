---
title: bubble sort
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 01:49
tags:
  - computer-science/algorithm/sort
course:
  - CSCA48
---
# bubble sort
Consider an array with $N$ entires, then bubble sort is done by
```
void bubbleSort(int array[N], int N){
	int t = 0;
	_Bool swapped = 1;
	
	for(int i = 0; i < N - 1 && swapped == 1; i++){
		swapped = 0;
		
		for(int j = 0; j < N - 1 - i; j++){
			
			// Swap between j and j + 1 if one of them is greater
			if(array[j] > array[j + 1]){
				t = array[j];
				array[j] = array[j + 1];
				array[j + 1] = t;
				
				swapped = 1;
			}
		}
	}
}
```

## time complexity
this algorithm has a 
- worst case (sorted backward): $N(N-1)2 = 2(N^2-N)\to O(N^2)$
- average case: $O(N^2)$
- best case (sorted forward): $O(N)$
