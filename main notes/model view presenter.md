---
title: model view presenter
created: Monday 3rd November 2025 19:55
last_modified: Monday 3rd November 2025 19:55
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "7"
---
# model-view-presenter
An architectural design pattern that results in code that is easier to test
It consists of three components
- model (data): update model-change events for __presenter__
- view (UI): Handles any interactions with the user (including display ofc), provides __presenter__ user events
- presenter (business logic): updates UI for __view__, update __model__
