# 🐍 Day 3 — Python Basics: Syntax

> **Goal:** Understand the basic syntax of Python and write your first interactive Python programs.

---

## 📚 Today's Learning Objectives

By the end of Day 3, you should be able to:

- Understand basic Python syntax
- Use the `print()` function
- Take input from users using `input()`
- Understand basic variables used with input
- Create formatted output using f-strings
- Write single-line comments
- Understand multi-line comments/documentation strings
- Write a small interactive Python program

---

# 1. What is Python Syntax?

**Syntax** means the rules that define how we should write a Python program.

Just like English has grammar rules, Python has syntax rules.

### Example

```python
print("Hello Python")
```

This is valid Python syntax.

### Incorrect Example

```python
print("Hello Python"
```

The closing `)` is missing, so Python will produce an error.

---

# 2. Important Python Syntax Rules

## 2.1 Python is Case-Sensitive

Python treats uppercase and lowercase letters differently.

```python
name = "Pavan"
Name = "Rahul"
```

`name` and `Name` are two different identifiers.

---

## 2.2 Parentheses Must Match

Correct:

```python
print("Hello")
```

Incorrect:

```python
print("Hello"
```

---

## 2.3 Strings Need Quotes

Text is generally written inside quotes.

```python
print("Hello")
```

You can use:

```python
print('Hello')
```

Both are valid.

---

## 2.4 Python Uses Indentation

Python uses indentation to define blocks of code.

Example:

```python
if True:
    print("Hello")
```

The spaces before `print()` are important.

The commonly recommended indentation is **4 spaces**.

> We will study indentation in more detail when we learn conditional statements and loops.

---

## 2.5 Semicolons Are Usually Not Required

Python normally uses a new line to separate statements.

```python
name = "Pavan"
age = 23
print(name)
print(age)
```

You don't need to write:

```python
name = "Pavan";
age = 23;
```

---

# 3. The `print()` Function

The `print()` function is used to display information on the screen.

### Example

```python
print("Hello Python")
```

Output:

```text
Hello Python
```

---

## Printing Numbers

```python
print(10)
print(25)
print(100)
```

Output:

```text
10
25
100
```

---

## Printing Calculations

```python
print(10 + 20)
```

Output:

```text
30
```

Another example:

```python
print(50 + 25)
print(100 - 20)
```

Output:

```text
75
80
```

---

## Printing Multiple Values

```python
name = "Pavan"
age = 23

print("Name:", name)
print("Age:", age)
```

Output:

```text
Name: Pavan
Age: 23
```

---

# 🧪 Practice 1 — Using `print()`

Create a Python program that displays:

```text
My name is <your name>
I am learning Python
My city is <your city>
I am learning Python Full Stack
```

### Challenge

Also print the result of:

```text
100 + 50
```

Try writing the program yourself before looking for help.

---

# 4. Taking Input from the User

Programs become more useful when they can interact with users.

Python provides the `input()` function for this purpose.

### Example

```python
name = input("Enter your name: ")

print(name)
```

When the program runs:

```text
Enter your name: Pavan
Pavan
```

---

## How `input()` Works

Consider:

```python
name = input("Enter your name: ")
```

There are three important parts:

### `input()`

Takes information from the user.

### `"Enter your name: "`

Message displayed to the user.

### `name`

Stores the value entered by the user.

> We will study variables in depth in the next lessons.

---

# 5. Taking Multiple Inputs

You can take multiple values from the user.

```python
name = input("Enter your name: ")
college = input("Enter your college: ")
course = input("Enter your course: ")

print(name)
print(college)
print(course)
```

Example:

```text
Enter your name: Pavan
Enter your college: ABC College
Enter your course: Python Full Stack

Pavan
ABC College
Python Full Stack
```

---

# 🧪 Practice 2 — Student Information

Create a program that asks the user for:

- Name
- College
- Course

Then display the entered information.

### Expected Output

```text
Enter your name: Pavan
Enter your college: ABC College
Enter your course: Python Full Stack

Name: Pavan
College: ABC College
Course: Python Full Stack
```

### ⭐ Challenge

Add:

- City
- Graduation year

---

# 6. Formatted Output Using f-Strings

Suppose we have:

```python
name = "Pavan"
course = "Python Full Stack"
```

We can write:

```python
print(f"Welcome {name}!")
print(f"You are learning {course}.")
```

Output:

```text
Welcome Pavan!
You are learning Python Full Stack.
```

---

## What is an f-string?

An **f-string** allows us to insert variables directly inside a string.

Syntax:

```python
f"Text {variable}"
```

Example:

```python
name = "Pavan"

print(f"Hello {name}")
```

Output:

```text
Hello Pavan
```

---

# 🧪 Practice 3 — Welcome Message

Create a program that takes:

- Student name
- Course name

Then display:

```text
================================
Welcome Pavan!
You are learning Python Full Stack.
Happy Learning!
================================
```

### Requirements

- Use `input()`
- Use variables
- Use an f-string
- Use `print()`

---

# 7. Comments in Python

A **comment** is a note written in the program for humans.

Python does not execute normal comments.

Comments help developers understand their code.

---

## Single-Line Comments

Use `#`.

```python
# This is a comment

print("Hello Python")
```

Python ignores:

```python
# This is a comment
```

and executes:

```python
print("Hello Python")
```

---

## Comments with Code

```python
# Get the student's name
name = input("Enter your name: ")

# Display the student's name
print(name)
```

---

# 8. Why Should We Use Comments?

Comments can help us:

- Explain code
- Make code easier to understand
- Document important logic
- Help other developers understand our program
- Make maintenance easier

### Example

```python
# Get the student's name
name = input("Enter your name: ")

# Get the student's course
course = input("Enter your course: ")

# Display the welcome message
print(f"Welcome {name}!")
print(f"You are learning {course}.")
```

---

# 9. Multi-Line Comments / Documentation Strings

Python does not have a dedicated multi-line comment syntax.

For multiple comment lines, you can use `#` on each line:

```python
# This program
# takes student information
# and displays a welcome message.
```

You may also see triple-quoted strings:

```python
"""
This program takes
student information
from the user.
"""
```

Triple-quoted strings are commonly used for **docstrings** when documenting functions, classes, and modules.

For normal comments, prefer:

```python
# Comment
```

---

# 🧪 Practice 4 — Add Comments

Create a program that:

1. Takes the student's name
2. Takes the student's course
3. Displays a welcome message
4. Contains meaningful comments

Example structure:

```python
# Get student name

# Get course name

# Display welcome message
```

---

# 🚀 Final Practical — Student Welcome System

Now combine everything you learned today.

## Requirements

Create a program that asks the user for:

- Student name
- College name
- Course name
- City

Then display a formatted student welcome message.

### Expected Output

```text
========================================
          STUDENT WELCOME
========================================

Name    : Pavan
College : ABC College
Course  : Python Full Stack
City    : Bangalore

Welcome to the course, Pavan!
Happy Learning!

========================================
```

### Requirements

Your program must use:

- `print()`
- `input()`
- Variables
- f-strings
- Comments

### ⭐ Important

**Try to build this program yourself before looking at a solution.**

The goal is not to copy code.

The goal is to understand how each concept works and combine them.

---

# 🧠 Day 3 Quick Revision

| Concept | Example |
|---|---|
| `print()` | `print("Hello")` |
| `input()` | `name = input("Enter name: ")` |
| Variable | `name = "Pavan"` |
| f-string | `f"Hello {name}"` |
| Comment | `# This is a comment` |
| Case-sensitive | `name` ≠ `Name` |
| Indentation | `    print("Hello")` |

---

# ❓ Interview / Viva Questions

### 1. What is Python syntax?

Syntax is the set of rules used to write valid Python programs.

### 2. What is `print()`?

`print()` is a built-in function used to display output.

### 3. What is `input()`?

`input()` is used to receive input from the user.

### 4. Is Python case-sensitive?

Yes.

```python
name
Name
```

are different.

### 5. How do you write a single-line comment?

```python
# This is a comment
```

### 6. What is an f-string?

An f-string allows variables to be inserted directly into strings.

```python
name = "Pavan"

print(f"Hello {name}")
```

### 7. Is indentation important in Python?

Yes. Python uses indentation to define blocks of code.

---

# 📝 Homework

Complete the following programs and push them to your GitHub repository.

### Task 1 — Personal Introduction

Take:

- Name
- Age
- City
- Course

Display a formatted introduction.

### Task 2 — College Welcome

Take:

- Student name
- College
- Branch

Display a welcome message.

### Task 3 — Student Profile ⭐

Take:

- Name
- College
- Course
- City

Display a formatted student profile and include meaningful comments.


## 🎯 Learning Rule

> **Don't just read the code. Type it, run it, break it, fix it, and understand it.**

**Day 3 → Python Basics: Syntax ✅**