---
title: structural design pattern
created: Monday 17th November 2025 20:20
last_modified: Monday 17th November 2025 20:19
aliases: []
tags:
  - software-development/design-pattern
course:
  - CSCB07
LEC:
  - "9"
---

# structural design pattern

## facade
Facade: Something that ties stuff (behind it)?
intent: hide complexities and provide a unified interface to a set of interfaces in a subsystem
![[Pasted image 20251117202325.png]]

Consider this code
```java
class Screen {
	public void down() {}
}

class Light {
	public void dim() {}
}

class Projector {
	public void on() {}
}
```
Instead of dealing with these 3 subclasses, we would love to deal with this:
```java
class Facade {
	Screen s;
	Light l;
	Porjector p;
	
	//stuffs...
}

public class FacadeExamle {
	Facade f;

	public void watchMovie() {
		f.watchMovie();
	}
}
```

The person who creates the subsystem is responsible to make the Facade
If one client wants it's own work from `Screen`, `Light`, `Projector`, we can create more than one Facade.

## adapter
intent: Let classes work together that couldn't otherwise because of incompatible interfaces

Consider this code
```java
class Client {
	public void foo(Target t) {
		System.out.println(t.add(2, 3));
	}
}

interface Target {
	public int add(int a, int b);
}

class Adaptee {
	public int sum(int a, int b) {
		return a + b;
	}
}
```

Consider client does:
```java
Client c = new Client();
c.foo(new Target());
```

This is wrong because `Target` is an interface

Consider client does:
```java
c.foo(new Adaptee());
```
This also won't work for obvious reason

Instead we can do
```java
class Client {
	public void foo(Target t) {
		System.out.println(t.add(2, 3));
	}
}

interface Target {
	public int add(int a, int b);
}

class Adaptee implements Target{
	public int add(int a, int b) {
		return a + b;
	}
}
```
Then, `c.foo(new Adaptee());` will work, but, since we changed the method name `sum` to `add`, this is not good. (Doesn't follow OCP)

Thus, we have to make `Target` a class instead of interface.
```java
class Client{
	public void foo(Target t) {
		System.out.println(t.add(2,3));
	}
}

interface Target{
	public int add(int a, int b);
}

class Adaptee{
	public int sum(int a, int b) {
		return a + b;
	}
}

class Adapter implements Target{
	Adaptee adaptee;
	
	public Adapter(Adaptee adaptee) {
		this.adaptee = adaptee;
	}
	
	public int add(int a, int b) {
		return adaptee.sum(a,b);
	}
}

public class AdapterExample{
	public static void main(String [] args) {
		Adapter adapter = new Adapter(new Adaptee());
		Client client = new Client();
		client.foo(adapter);
	}
}
```