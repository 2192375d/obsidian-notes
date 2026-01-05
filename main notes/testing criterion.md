---
title: testing criterion
created: Monday 20th October 2025 19:15
last_modified: Monday 20th October 2025 19:15
aliases: []
tags:
  - computer-science/software-development/testing
course:
  - CSCB07
LEC:
  - "6"
---
# testing criterion
Testing criterion is a set of rules that impose test requirements on a test set

Because the number of tests is not a good indication of how well the code is tested, so we need a testing criterion

Having a test criterion allows us to quantify the quality of testing

## statement coverage
Statement coverage is an indication of how many percent of statements are ran.

## limitations of statement coverage
In some cases, it might be impossible to achieve full coverage, due to:
- dead code
- complex criteria
Note that in some cases, full caverage might not necessarily mean that all bugs will be detected.

Consider this code
```java
public class Example {
	public static int min(int a, int b) {
		int min = b; //fault, should be min = a;
		if (b < a) {
			min = b;
		}
		return min;
	}
}
```
If we test it with `a = 2, b = 1`, 

then, `min = b` and  `b < a`, resulting in `min = b`, and it does pass (note that it has a 100% statement coverage), though it does not show what is wrong

## branch coverage
To deal with this issue, we want to have a branch for `b < a` and `b >= a` (eg going through all if statements)
