---
title: design a good API
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 00:48
tags:
  - computer-science/software-development
course:
  - CSCA48
---
API handles how __other programs interact with our module__. 
The API contains all specifications we need to make use of, or interact with, including software module, code library, subsystem, and even working components of an operating system or a remote server.

some common APIs:
- Google Maps
- TensorFlow
- Amazon AWS
- Unity
# Why do we need a good API?
Consider writing a function:
```
intList *findPath(int Adj[N][N], int start, int goal)  
{  
/*  
	This function returns a linked-list of nodes  
	that form a path from 'start' to 'goal' in  
	the input graph described by the adjacency  
	matrix Adj. 'start' and 'goal' are the indexes  
	of the nodes we want to find a path between.  
	If there is no path, the function returns NULL.  
	Assumes: Adj is size (N*N) where N is the number  
				of nodes in the graph. Adj(i,j) is 1  
				if there is a node from i to j, and 0  
				otherwise.  
				i,j are node indexes in [0,N-1]  
	intList consists of nodes that contain:  
				int nodeIndex;  
				pathList *next;  
	*/  
	
	...  
}
```
The user doesn't need to know how the function works, he/she only need to read the function declaration and the comments to tell what the function takes and returns.

Note that when a bug is found, changing one API means other all other associated APIs need to be updated.
Thus, when making an API, __minimize the likelihood of changing it in the future__.

# use case
Once API is stable and in use, things will be problematic if we didn't think of a __use case__ that turns out to be important to many potential users out there.

- use case: The specific situation in which the module/software component will be used for.
- dependency: The relation between software modules where the dependent module requries a library or module it depends on to be available and have correct version in order to compile and run

Anything added to the code via "include" statements introduces a dependency in your code. (e.g. not including it will stop the program from running)

(More in CSCC01, CSCD01)

# how to design a good API?
According to Google experts, a good API should be
- Easy to learn/use
- Difficult to use incorrectly
- Easy to maintain
- Easy to extend
- Suitable for the target customers.

They proposed the following principles
- The API should do one thing, and do it well-the functionalities should be easy to explain and make sense of. If it can't be explained in simple terms, it's bad bad.
- The API should be as small as possible. It should satisfy the need it's serving, but do not try to add every single possible thing you can think of it. The reason behind is that it's easy to add, but once it's there, it's hard to remove it.
- The API should be possible for you to completely chance the way function is implemented, without changing the API. In other words, it should be implementation independent
- Maximize information hiding, only make available to the user the functionality/data that user needs. (e.g. in C, it's really hard, but doable by avoiding to make global variables)
- Use correct naming, correct documentation.
- Make good performance.
- User of the API should not be surprised by the behaviour of the API
- API should report errors as soon as they occur.
- If API makes uses of strings, provide functions to parse strings into any components the user may need to handle seperately. This prevents annoyance and keeps the user from having to write parsers for the API's output.

Below is good general principles for good programming
- Use the most appropriate return value for each function
- be consistent with ordering of parameter
- avoid long parameter lists



