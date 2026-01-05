---
title: Mockito
created: Monday 3rd November 2025 19:54
last_modified: Monday 3rd November 2025 19:54
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "7"
---
# Mockito
A mocking framework for Java, features include
- create mocks
- subbing
- verifying behavior

## Mock object
A mock is a software component that is used to replace the "real" component during testing
A mock object could be used to
- represent components that have not yet been implemented
- speed up testing
- reduce the cost (eg some testing may require payment, instead using a mock version will reduce the cost)
- avoid unrecoverable actions

## verify
`verify()` method is used to check if a function call occured during runtime. Note that it doens't care about the logic or anything, it simply checks if a method is called

Here is a sample Mockito test
```java
@RunWith(MockitoJUnitRunner.class)
public class ExampleUnitTest {
	
	@Mock
	MainActivity view;
	
	@Mock
	Model model;
	
	@Test
	public void testPresenter() {
		when(view.getUsername()).thenReturn("abc");
		when(model.isFound("abc")).thenReturn(true);
		Presenter presenter = new Presenter(model, view);
		
		presenter.checkUsername();
		verify(view).displayMessage("user found"); //verifies if any message call displayMessage("user found") happened
	}
}
```

Mockito can also be used to check number of times a method is called using `verify`
```java
verify(view, times(2)).displayMessage("user found");
```

## ArgumentCaptor
An equivalent of the first test using `ArgumentCaptor` is
```java
@Test
public void testPresenter() {
	when(view.getUsername()).thenReturn("abc");
	when(model.isFound("abc")).thenReturn(true);
	Presenter presenter = new Presenter(model, view);
	
	presenter.checkUsername();
	ArgumentCaptor<String> captor = ArgumentCaptor.forClass(String.class);
	verify(view).displayMessage(captor.capture());
	assertEquals(captor.getValue(), "user found");
}
```
Note that `ArgumentCaptor` can 
- only capture arguments passed into mocked methods
- only be used in `verify()` or `when()`

## order
`order` method checks if the method calls are done in a certain order
```java
@Test
public void testPresenter() {
	when(view.getUsername()).thenReturn("abc");
	when(model.isFound("abc")).thenReturn(true);
	Presenter presenter = new Presenter(model, view);
	
	presenter.checkUsername();
	InOrder order = inOrder(model, view);
	//using anyString() just checks runs through the test with arbitrary strings
	//order.verify(view).isFound(anyString());
	order.verify(view).isFound("abc");
	order.verify(view).displayMessage("user found");
}
```