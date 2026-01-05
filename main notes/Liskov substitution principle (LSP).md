---
title: Liskov substitution priciple
created: Monday 10th November 2025 20:15
last_modified: Monday 10th November 2025 20:15
aliases: []
tags:
  - computer-science/software-development/SOLID
course:
  - CSCB07
LEC:
  - "8"
---
# Liskov substitution principle (LSP)
(To follow this one, you can NEVER have something like `Square extends Rectangle`)
Subtypes must be substituable for base types
Formally, LSP says:
- Let $\Phi(x)$ be a property provable about objects $x$ of type $T$. Then $\Phi(y)$ should be true for objects $y$ of type $S$ where $S$ is a subtype of $T$
In human words, LSP says
- If it looks like a duck, quacks like a duck, but needs batteries, then you probably have the wrong abstraction

Consider this code:
```java
class Rectangle{
	double width;
	double height;
	
	public Rectangle(double width, double height) {
		//...
	}
	
	public void setWidth(double newWidth) {
		width = newWidth;
	}
	//...
}

class Square extends Rectangle {
	public Square (double side) {
		super(side, side);
	}
}
```

This violates LSP

To address the issue, you can override `setWidth()` in Square
```java
class Square extends Rectangle {
	public Square //...
	
	@override 
	public void setWidth (double new Width) {
		width = newWidth;
		height = newWidth;
	}
}
```

Some issues:
- Square class doesn't need the height and width, which takes unnecessary space
- We have to override methods (for this case, `setHeight(), setWidth()`)

This also fails for
```java
void testRectangleArea(Rectangle r) {
	r.setWidth(5);
	r.setHeight(4);
	assertEquals(r.computeArea(), 20);
})
```
for the cases when we pass a `Square` as parameter

Thus, it's impossible to have a valid `Square extends Rectangle` that respects LSP