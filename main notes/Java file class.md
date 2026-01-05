---
title: Java file class
created: Monday 15th September 2025 20:50
last_modified: Monday 15th September 2025 20:50
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC: 2
---
# The file class
Contains methods for obtaining the properties of a file/directory and ofr renaming and deleting a file/directory.

Files could be specified using absolute or relative names
(Constructing a file instance does not create a file ont he machine)

methods include:
- `boolean createNewFile()`
- `boolean delete()`
- `boolean exists()`
- `boolean isDirectory()`
- `File [] listFiles()`

## file I/O example
There are multiple ways to read/write in files
- reading using the __BufferedReader__ class: `BufferedReader input = new BufferedReader(new FilesReader("myfile.txt"));`
- reading using the __Scanner__ class: `Scanner input = new Scanner(new Files("myfile.txt"));`
- writing using the __PrintStream__ class: `PrintStream output = new PrintStream("myfile.txt");`
- writing using the __FileWriter__ class: `FileWriter output = new FileWriter("myfile.txt", false); //use true for appending` 

## sample code
The following code prints a file
```
BufferedReader input = new BufferedReader(new FileReader("filepath"));
String line = input.readLine();
while(line != null){
	line = System.out.println(line);
	line = input.readLine();
}
```
The following code writes in a file
```
PrintStream p = new PrintStream("filepath"):
p.println("L1");
p.println("L2");
p.println("L3");
```