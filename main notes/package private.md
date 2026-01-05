---
title: package private
created: Monday 22nd September 2025 19:55
last_modified: Monday 22nd September 2025 19:55
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "3"
---
If a field's visibility is not metioned (no public/private ahead), then it is __package private__. Which means it is available for any files in the same ~~directory~~ package.

eg
```
class Point{
	int x;
	int y;
}
```

Then, for any files in the same directory as Point.java, any instances' x and y fields are available to them