---
title: abstract class
created: Monday 6th October 2025 19:26
last_modified: Monday 6th October 2025 19:26
aliases: []
tags:
  - computer-science/object-oriented-programming
course:
  - CSCB07
LEC:
  - "5"
---
# abstract class
- abstract class instance cannot be instantiated using the __new__ operator
- usually contain abstract methods that are implemented in concrete subclasses

```java
public class Point {
	double x;
	double y;
	
	public Point(double x, double y) {
		this.x = x;
		this.y = y;
	}
}

public class Shape {
	String color;
	
	public Shape(String color) {
		this.color = color;
	}
	
	public String getColor() {
		return color;
	}
	
	public void setColor(String color) {
		this.color = color;
	}

	public abstract void computerArea();
}

public class Circle extends Shape {
	//..., with method computeArea
}

public class Rectangle extends Shape {
	//..., with method computeArea
}

public class Driver {
	
	public static void main(String [] args) {
		Shape [] shapes = new Shape[2];
		shapes[0] = new Rectangle(5, 6, "red");
		shapes[1] = new Circle(new Point(0, 0), 4, "blue");
	}
	//...
	
	for(int i = 0; i < shapes.length; i++) {
		// If computeArea() is not declared in Shape, this lines will throw a syntax error, because the array shapes is compile type, not runtime type
		System.out.println(shapes[i].computeArea());
	}
}
```

If a method is abstract, then __ALL__ of the concrete (non abstract) subclasses must implement this method.

However, note that because of this, no object of type Shape can be instantiated from now on.