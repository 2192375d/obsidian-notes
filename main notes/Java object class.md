---
title: object class
created: Monday 6th October 2025 19:21
last_modified: Monday 6th October 2025 19:21
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC: 4
---
# object class
Every classes in Java are inherited by __Object__ class, it has the following mehtods that are usually overridden:
- equals
- hashCode
- toString

## equals
Header: `boolean equals(Object obj)`

returns true iff this object have the __same memory allocation__ as the target object

(original source code from JDK 21)
```java
public boolean equals(Object obj) {
	return (this == obj);
}
```

The (overridden) methods must follow:
- reflexive: for any non-null reference value `x`, `x.equals(x)` should always return true.
- symmetry: for any non-null reference value `x`, `y`, `x.equals(y)==y.equals(x)`
- transitive: for any non-null reference value `x`, `y` and `z`, if `x.equals(y)` returns true and `y.equals(z)` returns true, then `x.equals(z)` should return true
- consistent: for any non-null reference value `x`, `y`, `x.equals(y)` should always return the same value if no modifications are made on `x` and `y`
- for any non-null reference value `x`, `x.equals(null)` should return false

## hashCode
Header: `int hashCode`

returns the hash of the object, which is usually (by default) the memory address

If equals is overridden, hashCode must also be overridden, where if `x.equals(y)` returns true, `x.hashCode() == y.hashCode()` must also be true

For unequal objects, a good hashCode method tends to produce unequal hash codes (eg __hashcodes are unique__)

## toString
Header: `String toString()`

if instance is not null, `toString` method is automatically invoked when an object is passed to `println` or string concatenation operator
Otherwise it prints "null"

returns a string with the classname and the hashCode in hexadecimal
```java
public String toString() {
	return getClass().getName() + "@" + Integer.toHexString(hashCode());
}
```

toString is usually overridden to return a more descriptive string representation of the object