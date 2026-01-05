---
title: Java array
created: Monday 15th September 2025 20:13
last_modified: Monday 15th September 2025 20:13
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC: 2
---
Arrays in Java are __non primative__

# array sample code
```
public class Driver{
	public static void main(String [] args) {
		int [] A = new int[3];
		
		A[0] = 10;
		A[1] = 20;
		A[2] = 30;
		
		for (int i = 0; i < A.length; i++){
			system.out.println(A[i]);
		}
	}
}
```

The output will be
```
10
20
30
```

(Note that on the line `int [] A = new int[3];`, the array is initiated with default values 0)

Also we can initiate with `double[] myList = {1.9, 3.4}`
Or `int [][] A = new int[2][3]`