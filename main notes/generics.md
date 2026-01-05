---
title: generics
created: Monday 6th October 2025 19:59
last_modified: Monday 6th October 2025 19:59
aliases: []
tags:
  - computer-science/software-development/generics
course:
  - CSCB07
LEC:
  - "5"
---
# generics

Consider this code
```java
public class Pair {
	Object a;
	Object b;
}
```

This can be problematic because `a` and `b` might not be of the same type

This will solve the problem
```java
public class Pair<E> {
	E a;
	E b;
}
```

If you want to restrict `E` to a particular class, use extend
```java
public class Pair<E extends Person> {
	E a;
	E b;
}
```
Then `a` and `b` must be of class Person
