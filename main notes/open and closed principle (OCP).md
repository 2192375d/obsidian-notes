---
title: open and closed principle
created: Monday 10th November 2025 19:34
last_modified: Monday 10th November 2025 19:34
aliases: []
tags:
  - computer-science/software-development/SOLID
course:
  - CSCB07
LEC:
  - "8"
---
# open/closed principle (OCP)
Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification

Consider this code:
```java
public class Date {
	int day;
	int month;
	int year;
	
	public Date(int day, int month, int year) {
		this.day = day;
		this.month = month;
		this.year = year;
	}
	
	@Override
	public String toString() {
		return day + "/" + month + "/" + year;
	}
}
```

This code violates OCP because when you wanna change what is printed, you must modify `toString()` method directly.

Instead, we can do
```java
interface Formatter {
	public String getFormat(int day, int month, int year);
}

class DMYFormatter implements Formatter {
	public String getFormat(int day, int month, int year) {
		return day + "/" + month + "/" + year;
	}
}

public class Date {
	int day;
	int month;
	int year;
	
	Formatter f;
	
	public Date(int day, int month, int year) {
		this.day = day;
		this.month = month;
		this.year = year;
	}
	
	public void setFormatter(Formatter f) {
		this.f = f;
	}
	
	@Override
	public String toString() {
		return f.getFormat(day, month, year);
	}
```

Where we have this in main:
```java
Date d = new Date(23, 8, 2006);
d.setFormatter(new DMYFormatter);
System.out.println(d);
```
Note that this follows OCP correctly for the `toString()` method