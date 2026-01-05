---
title: Java dynamic binding
created: Thursday 9th October 2025 14:40
last_modified: Thursday 9th October 2025 14:40
aliases: []
tags:
  - computer-science/object-oriented-programming
course:
  - CSCB07
LEC:
  - "6"
---
Consider this code
```java
Object x = new Point(1, 2);
System.out.println(x);
```

where `toString` is overridden in the Point class

The way how dynamic binding works is that, it will priotize ___to be continued
You know what I'm too lazy to write it but it's just the thing that goes for the first method defined from the inheritance hierarchy (starting from the current one and go to the most base class)