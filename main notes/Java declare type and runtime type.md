---
title: Java declare type and runtime type
created: Monday 22nd September 2025 20:29
last_modified: Monday 22nd September 2025 20:29
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "3"
---
Consider code
(Note Employee extends Person)
```
public class Driver {
	
	public static void main(String [] args) {
		
		Person p = new Employee("abc", "xyz", 1000);
	}
}
```
declare type: `Person`
runtime type: `Employee`

The declare type can be the same as the same of it's runtime type or any super class of the runtime type

Here is how it looks like in memory:
stack:
- p of type Person, pointing to Employee object in heap
heap:
- Employee, with fields "abc", "xyz", 1000

super()

# Java declare type and runtime type
The declare type affects how code deals with the compiling part
The runtime type decides how the code is running

For example, you cannot attempt to call a function from the Employee class
`float x = p.getSalary() //error`
(getSalary is a method from Employee not in Person)
but if the method already exists in Person and Employee, it's gonna print from the Employee function.
```
public class Person {
	
	// constructors
	
	public void foo() {
		System.out.println("foo in Person")
	}
}

public class Employee extends Person {
	
	// constructors
	
	public void foo(){
		System.out.println("foo in Employee")
	}
}

public class Driver {
	public static void main(String [] Args) {
		Person p = new Employee
		p.foo();
	}
}
```

The output will be `foo in Employee`

## typecasting using this
```
Person p = new Employee("abc", "xyz", 1000);
Employee e = (Employee) p;
```

This will create a new Employee pointing to the employee that p is pointing to in the heap

```
System.out.println(e.getSalary())
```

this will print `1000`

## calling a method from it's own class

Consider
```java
public class Person {
	
	Person(){}
	
	public void bar() {
		print("bar from Person");
	}
	
	public void foo() {
		bar();
	}
}

public class Employee extends Person {
	
	Employee(){}
	
	public void bar() {
		print("bar from Employee");
	}

}

public class Driver {
	public static void main(String [] args) {
		Person p = new Employee;
		p.foo();
	}
}
```

The output is, __surprisingly__, `bar from Employee`, this means everytime when you make a method call inside a method, you are rewriting __instance_name.method_name()__ in the main function, on this example, `bar()` call in `foo` is equivalent to `p.bar()`