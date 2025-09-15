---
title: limitations of C
created: Before 28th July, 2025
last_modified: Saturday 26th July 2025 19:30
tags:
  - computer-science/software-development
course:
  - CSCA48
---
One limition on C is that it doesn't encapsulate the data.
For example, user can access every info about your struct without telling you, and do everything they want with it, like modifying the value.

This creates concern regarding modules making structs no longer been self-contained and can potentially cause bugs or misuse by malicious users.

The solution to this problem (which is a feature not in C) is __OOP (object oriented programming)__
