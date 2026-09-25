# Day 34 -- Python File Handling Basics II

## Duration

**1 Hour 30 Minutes**

## Topic

Append Mode, `with open()`, and Line-by-Line Reading

## Learning Objectives

By the end of this session, students should be able to: - Use append
mode `a`. - Understand the difference between write and append. - Use
`with open()` for safer file handling. - Read files line-by-line. - Use
`readline()`. - Use `strip()` to remove unwanted newline characters.

## 1. Quick Revision -- 10 Minutes

Revise: - `open()` - `read()` - `write()` - `close()` - File modes `r`,
`w`, and `a`

## 2. Append Mode -- 20 Minutes

Append mode adds new content without deleting existing content.

``` python
file = open("notes.txt", "a")

file.write("File Handling\n")
file.write("Exception Handling\n")
file.write("Object Oriented Programming\n")

file.close()
```

### Important Comparison

  Mode   Meaning
  ------ ------------------------
  `r`    Read
  `w`    Write / overwrite
  `a`    Add content at the end

## 3. Using `with open()` -- 20 Minutes

Instead of manually closing the file:

``` python
file = open("notes.txt", "r")
content = file.read()
print(content)
file.close()
```

Use:

``` python
with open("notes.txt", "r") as file:
    content = file.read()
    print(content)
```

The file is automatically closed after the `with` block.

### General Syntax

``` python
with open("filename", "mode") as variable:
    # file operations
```

## 4. Reading Line-by-Line -- 20 Minutes

### Using a `for` Loop

``` python
with open("notes.txt", "r") as file:
    for line in file:
        print(line)
```

### Removing Extra Newline

``` python
with open("notes.txt", "r") as file:
    for line in file:
        print(line.strip())
```

### Using `readline()`

``` python
with open("notes.txt", "r") as file:
    print(file.readline())
    print(file.readline())
```

## 5. Practical Program -- 15 Minutes

### Add and Display Python Topics

``` python
with open("notes.txt", "a") as file:
    file.write("File Handling\n")
    file.write("Exception Handling\n")
    file.write("OOP\n")

with open("notes.txt", "r") as file:
    print("Python Topics:")

    for line in file:
        print(line.strip())
```

## 6. Student Practice -- 5 Minutes

Create a program that: 1. Creates `students.txt`. 2. Adds five student
names. 3. Appends three more names. 4. Reads the file line-by-line. 5.
Prints every student name.

Example:

``` python
with open("students.txt", "w") as file:
    file.write("Rahul\n")
    file.write("Priya\n")
    file.write("Arun\n")
    file.write("Sneha\n")
    file.write("Kiran\n")

with open("students.txt", "a") as file:
    file.write("Anil\n")
    file.write("Meena\n")
    file.write("Ravi\n")

with open("students.txt", "r") as file:
    for name in file:
        print(name.strip())
```

## End-of-Day-34 Challenge

Build a **Student Notes File Manager**:

1.  Add student
2.  Display students
3.  Add more students
4.  Exit

Use only the concepts learned in Day 33 and Day 34.

## Key Takeaways

-   `a` appends data without deleting existing content.
-   `with open()` automatically closes the file.
-   A `for` loop can read a file line-by-line.
-   `readline()` reads one line.
-   `strip()` can remove surrounding whitespace and newline characters.
