# 🐍 Day 32 – Python Packages

## 📌 Overview
On Day 32, we learned about Python Packages. A package is a collection of Python modules organized inside a folder.

## 🎯 Learning Objectives
- Understand Python packages
- Understand module vs package
- Create a package
- Create modules inside a package
- Import modules and functions from a package

## 1. What is a Package?
A package is a directory containing Python modules.

```text
studentapp/
├── __init__.py
├── student.py
└── marks.py
```

Here:
- `studentapp` → Package
- `student.py` → Module
- `marks.py` → Module

## 2. Module vs Package

| Module | Package |
|---|---|
| Usually one `.py` file | Directory containing modules |
| Contains functions/classes/code | Organizes multiple modules |
| Example: `student.py` | Example: `studentapp` |

## 3. Creating a Package

```text
PythonProject/
├── main.py
└── studentapp/
    ├── __init__.py
    └── student.py
```

### `student.py`
```python
def greet():
    print("Hello! Welcome to Student App")
```

### `main.py`
```python
from studentapp.student import greet

greet()
```

Output:
```text
Hello! Welcome to Student App
```

## 4. Multiple Modules

### `student.py`
```python
def student_name():
    print("Student: Pavan")
```

### `marks.py`
```python
def display_marks():
    print("Marks: 85")
```

### `main.py`
```python
from studentapp.student import student_name
from studentapp.marks import display_marks

student_name()
display_marks()
```

## 5. Calculator Package Example

```text
calculator/
├── __init__.py
├── addition.py
└── subtraction.py
```

### `addition.py`
```python
def add(a, b):
    return a + b
```

### `subtraction.py`
```python
def subtract(a, b):
    return a - b
```

### `main.py`
```python
from calculator.addition import add
from calculator.subtraction import subtract

print("Addition:", add(10, 5))
print("Subtraction:", subtract(10, 5))
```

## 🧠 Real-World Understanding
Think of a college:
```text
College
├── CSE Department
├── ECE Department
├── Mechanical Department
└── Civil Department
```

Similarly:
```text
Package
├── Module 1
├── Module 2
├── Module 3
└── Module 4
```

## 📝 Practice Programs
1. Create a package called `calculator`.
2. Create an `addition.py` module.
3. Create an `add()` function.
4. Import the function into `main.py`.
5. Create a `school` package with `student.py` and `teacher.py`.
6. Create a `bank` package with `account.py` and `transaction.py`.

## 🔑 Key Takeaways
```text
Module
   ↓
Single Python file

Package
   ↓
Collection of Python modules

import
   ↓
Used to access reusable code
```

Important syntax:
```python
from package.module import function
```

## 🚀 Day 32 Summary
We learned how to create Python packages, organize modules inside packages, and import functions from those modules.

**Next:** Day 33 – Advanced Python Concepts
