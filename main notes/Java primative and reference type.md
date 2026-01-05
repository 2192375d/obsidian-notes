---
title: Java primative and reference type
created: Monday 15th September 2025 19:29
last_modified: Monday 15th September 2025 19:29
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC: 2
---
# primative and reference type
Every variable represents a memory location that holds a value.
For variable of a __primative__ type (`int i = 1`), the value is of the primitive type
For variable of an __reference__ (object) type (`Cricle c`), the value is a reference to where an object is located

___Actually a reference is just a pointer___

Java objects are __references__ (don't mess this up), thus, 
```
public class Driver{
	
	public statis void main(String [] args) {
		Point p1 = new Point(1, 2);
		Point p2 = p1;
		p1.x = 100;
		System.out.println(p2.x);
	}
}
```

The output is `100` instead of `1`