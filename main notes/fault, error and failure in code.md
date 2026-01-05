---
title: fault, error and failure in code
created: Monday 20th October 2025 19:32
last_modified: Monday 20th October 2025 19:32
aliases: []
tags:
  - computer-science/software-development/testing
course:
  - CSCB07
LEC:
  - "6"
---
# fault/error/failure
- Software fault: a static defect in the software (eg assigning a wrong value)
- Software error: an incorrect internal state that is the manifestation of some fault
- Software failure: external, incorrect behavior with respect to the requirements or another description of the expected behaviour

Note that __state of program__ (mentioned above) is a snapshot of all the variables with their values, and if the values are not what are expected, this is a software error

When we say a program has a bug, we mean one of the three above is happening

```java
public static int numZero (int []arr) {
	int count = 0;
	for (int i = 1; i < arr.length; i++) {
		if (arr[i] == 0) {
			count++;
		}
	}
}
```

On line 3, we have a software fault due to the wrong value

Consider testing this with `arr = [2, 7, 0]`, then expected: `1`, actual: `1` and
- error: `i` is `1`, not `0`, in the first iteration
- failure: none

Consider testing again with `arr = [0, 2, 7]`, then expected: `1`, actual: `0` and
- error: `i` is `1`, not `0`, in the first iteration, error propagates to the variable count
- failure: count is `0` at return statement
