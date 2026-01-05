---
title: unit testing
created: Monday 6th October 2025 20:46
last_modified: Monday 6th October 2025 20:46
aliases: []
tags:
  - computer-science/software-development/testing
course:
  - CSCB07
LEC:
  - "5"
---
# unit testing
Test a single unit in isolation
Unit testing process:
- write one or more tests to verify the behavior of the unit, where these tests are called __unit tests__, and each unit test is written by specifying an input and the expected output/state.

Automation is key:
- Automation means the act of running and checking the code is done without programmers' writing
- (eg the task of running and checking the output should be done automatically)
(unit tests are __useless__ without automation)

Note that the __number of test cases__ is not an indication of how good the test case is.
Thus, when planning test cases, you wanna have a list of criterias that must be satisfied (eg test all methods in the class at least)

Note that even if all the criterias are satisfied and all the test cases passed, this still does __NOT__ guarantee the correctness