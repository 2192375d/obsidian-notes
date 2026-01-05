---
title: interface
created: Monday 6th October 2025 19:43
last_modified: Monday 6th October 2025 19:43
aliases: []
tags:
  - computer-science/software-development
course:
  - CSCB07
LEC:
  - "5"
---
# interface
An interface can be used to define common behaviour for classes
- In an interface class, all methods are __abstract__

```java
public interface Edible{
	public abstract String howToEat();
}
```

Consider when you have classes Apple and Chicken, note that inheritance vise, they are not associated to each other. However, they are both edible, thus we can use the interface above to generalize both of them.

Note that the abstract keyword can be discarded, the result is the same, eg
```java
public interface Edible{
	public String howToEat();
}
```
this code above gives the exact same result

Note that a concrete class cannot inherit an interface