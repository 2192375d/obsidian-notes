---
title: Java generics and ArrayList
created: Monday 6th October 2025 20:05
last_modified: Monday 6th October 2025 20:05
aliases:
  - Java ArrayList
  - Java foreach loop
tags:
  - computer-science/software-development/java
  - computer-science/software-development/generics
course:
  - CSCB07
LEC:
  - "5"
---
# Java ArrayList
Array but you can change the size after instantiating
commonly used methods:
- `boolean add(E e)`
- `E get(int index)`
- `int size()`
- `boolean contains(Object o)`
- `int indexOf(Object o)`

# generics and ArrayList class (and foreach loop)
Generics can force the type of individuals in the ArrayList
```java
public class Driver {
	public static void main(String [] args) {
		ArrayList<Circle> circles = new ArrayList<Circle>();
		// circles.add(new Circle());
		
		// for(int i = 0; i < A.size(); i++){
		//   System.out.println(A.get(i).computerArea());
		// }
		
		//the code above in foreach loop
		for(Circle c:A){
			System.out.println(c.computeArea());
		}
	}
}
```
