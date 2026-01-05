---
title: Java inheritence
created: Monday 22nd September 2025 19:48
last_modified: Monday 22nd September 2025 19:48
aliases: []
tags:
  - computer-science/object-oriented-programming
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "3"
---
# Java inheritence
Consider code
```
public class Person {
	
	String name;
	String address;
	
	Public Person(){}
	
	Public Person(String name, String address) {
		this.name = name;
		this.address = address;
	}
	
	public void func foo() {
		System.out.println("foo in Person");
	}
}

public class Employee extends Person{
	
	double salary;
	
	public Employee(String name, String address, double salary){
		super(name, address); //calls the Person(name, address);
		this.salary = salary;
	}
	
	public double getSalary() {
		return salary;
	}
	
	public void setSalary(double salary) {
		this.salary = salary;
	}
}
```

## Important stuffs to watch out
If we don't call `super(String, String, double)` or `super()` as the __first statement__, instead in later statements, in the `Employee(String, String, double)` method, the function will automatically throw an error

```
public Employee(String name, String address, double salary){
	this.salary = salary;
	super(name, salary) //error
}
```

If you don't call `super(...)` at all, it's gonna call `super()` right before first line is ran. If `super()` is not present (in this context method `Person()` does not exist), this will throw an error.
