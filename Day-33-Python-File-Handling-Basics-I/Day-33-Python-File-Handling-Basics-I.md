# Day 33 -- Python File Handling Basics I

## Duration

**1 Hour 30 Minutes**

## Topic

File Handling -- Creating, Writing and Reading Files

## Learning Objectives

By the end of this session, students should be able to: - Understand
what file handling is and why it is used. - Open files using `open()`. -
Understand file modes: `r`, `w`, `a`, and `x`. - Write data using
`write()` and `writelines()`. - Read data using `read()`. - Close files
using `close()`.

## 1. Introduction to File Handling -- 10 Minutes

Explain: - What is a file? - Why files are required for permanent data
storage. - Difference between variables and files. - Text files and
binary files. - Basic workflow: Open → Read/Write → Close.

## 2. Opening a File -- 15 Minutes

``` python
file = open("notes.txt", "mode")
```

### Common Modes

  Mode   Purpose
  ------ -------------------
  `r`    Read
  `w`    Write
  `a`    Append
  `x`    Create a new file

Important: - `w` creates a file if it does not exist. - `w` overwrites
an existing file.

## 3. Writing to a File -- 20 Minutes

``` python
file = open("notes.txt", "w")

file.write("Variables\n")
file.write("Data Types\n")
file.write("Operators\n")
file.write("Loops\n")
file.write("Functions\n")

file.close()
```

### Using `writelines()`

``` python
topics = ["Variables\n", "Lists\n", "Tuples\n", "Sets\n", "Dictionaries\n"]

file = open("notes.txt", "w")
file.writelines(topics)
file.close()
```

## 4. Reading a File -- 20 Minutes

### Using `read()`

``` python
file = open("notes.txt", "r")

content = file.read()
print(content)

file.close()
```

### Reading a Limited Number of Characters

``` python
file = open("notes.txt", "r")
print(file.read(10))
file.close()
```

## 5. Practical Program -- 20 Minutes

### Python Notes Manager

``` python
file = open("notes.txt", "w")

file.write("Python Variables\n")
file.write("Python Data Types\n")
file.write("Python Operators\n")
file.write("Python Loops\n")
file.write("Python Functions\n")

file.close()

file = open("notes.txt", "r")
content = file.read()

print("Python Topics:")
print(content)

file.close()
```

## 6. Practice Questions -- 5 Minutes

1.  What is file handling?
2.  What is the difference between `r` and `w`?
3.  What happens when an existing file is opened in `w` mode?
4.  What does `read()` do?
5.  Why should a file be closed?

## Day 33 Task

Create `notes.txt`, write five Python topics into it, then read and
display the complete file.

## Key Takeaways

-   `open()` opens a file.
-   `write()` writes data.
-   `read()` reads data.
-   `close()` closes the file.
-   `w` overwrites existing content.
