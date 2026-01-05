---
title: RIPR model
created: Monday 20th October 2025 19:42
last_modified: Monday 20th October 2025 19:42
aliases: []
tags:
  - computer-science/software-development/testing
course:
  - CSCB07
LEC:
  - "6"
---
# RIPR model
Four conditions are needed for a failure to be observed
- reachability: a test must reach the location in the program that contains the fault
- infection: after the faulty location is executed, the state of the program must be incorrect
- propagation: the infected state must propagate through the rest of the executation and cause some output or final state of the program to be incorrect
- revealability: the tester must observe part of the incorrect portion of the final program state

Note that propagation->infection, infection->reachability

## reachability does not imply infection
Consider this code (again)
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

If we input with `a = b`, say `a = b = 2`
Then when we reach line 3, we do reach the line with error, but it does not infest the state