---
title: Android project data storage options
created: Monday 3rd November 2025 19:29
last_modified: Monday 3rd November 2025 19:29
aliases: []
tags:
  - computer-science/software-development/android
course:
  - CSCB07
LEC:
  - "7"
---
# data storage options
- file system
- shared preferences
- databases (eg: SQLite, Firebase Realtime Database)

## Firebase realtime database
- cloud hosted
- employs data synchronization: In a Firebase realtime database, if you modify something inside, as soon as the change is made, the users will immediately be notified that a change is made.
- no SQL database, data is stored as JSON
- The Firebase SDK provides many classes and methods to store and sync data (eg: `DatabaseReference`, `DataSnapshot`, `ValueEventListener`)