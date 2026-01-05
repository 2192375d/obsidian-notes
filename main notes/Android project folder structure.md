---
title: Android project folder structure
created: Monday 3rd November 2025 19:26
last_modified: Monday 3rd November 2025 19:26
aliases: []
tags:
  - computer-science/software-development/android
course:
  - CSCB07
LEC:
  - "7"
---

# Android project folder structure
An Android project contains the following files:
- manifest file: It defines the structure and metadata of an application, its components, and its requirements. Stored in the root of its project hierarchy as an XML file
- Java files: 
- resource files: Resources are maintained in sub-directories of the app/res directory (e.g. res/layout). A resources can be accessed in the code using its resource ID (eg `R.layout.activity_main`)
- Gradle scripts: used to automate the build process

## sample directory structure
app
-> manifests
-> java
-> -> 
-> -> 
-> res
-> -> drawable
-> -> layout
-> -> -> `activity_main.xml`
-> -> mipmap
-> -> -> `colors.xml`, `string.xml`, themes
-> Gradle Scripts