---
title: design pattern
created: Monday 17th November 2025 19:20
last_modified: Monday 17th November 2025 19:20
aliases:
  - factory method
  - singleton
tags:
  - software-development/design-pattern
course:
  - CSCB07
LEC:
  - "9"
---

# creational design pattern
A creational pattern that addresses problems with object creation. 

One example is singleton design pattern

## singleton
Singleton design pattern deals situations when a class is designed to have one instance only

```java
final class Manager {
	priavte static Manager manager;
	
	private Manager() {}
	
	public static Manager getInstance() {
		if (manager == null) {
			 manager = new Manager();
		}
		return manager;
	}
}
```

## factory method
Define an interface for creating an object

```java
class Circle extends Shape {}
class Triangle extends Shape {}

abstract class GraphicsApplication {
	List<Shape> shapes;
	
	public void addShape() {
		Shape s = null;
		
		if(this isInstanceof Circle) {
			s = new Circle();
		}
		if(this isInstanceof Triangle) {
			s = new Triangle();
		}
		
		shapes.add(s);
	}
}
```

This violates DIP and OCP so it's not optimal
Instead we can do this:
```java
class Circle extends Shape {}
class Triangle extends Shape {}

abstract class GraphicsApplication {
	List<Shape> shapes;
	public abstract Shape factoryMethod();
	
	public void addShape() {
		Shape s = factoryMethod();
		shapes.add(s);
	}
}

class TrianglesApplication extends GraphicsApplication {
	public Shape factoryMethod() {
		return new Triangle();
	}
}

class CirclesApplication extends GraphicsApplication {
	public Shape factoryMethod() {
		return new Circle();
	}
}
```