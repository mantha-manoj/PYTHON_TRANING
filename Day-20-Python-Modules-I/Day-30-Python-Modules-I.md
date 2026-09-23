# 🐍 Python 45 Days – Day 30

## 📚 Topic: Modules – I

**Duration:** 1 Hour 30 Minutes

---

## 🎯 Learning Objectives

By the end of this class, students will be able to:

- Understand Python modules
- Create custom modules
- Import modules
- Import specific functions
- Use module aliases
- Organize Python programs into multiple files
- Build a calculator using a custom module

---

# 1. What is a Module?

A **module** is a Python file containing reusable code.

A module can contain:

- Functions
- Variables
- Classes
- Statements

Python files have the `.py` extension.

Example:

```text
calculator.py
```

---

# 2. Why Do We Use Modules?

Modules help us to:

- Reuse code
- Organize large programs
- Avoid code duplication
- Make programs easier to maintain
- Divide a large project into smaller files

---

# 3. Creating a Custom Module

Create a file named:

```text
calculator.py
```

Add the following:

```python
def add(a, b):
    return a + b


def subtract(a, b):
    return a - b


def multiply(a, b):
    return a * b
```

This file is now a Python module.

---

# 4. Importing a Module

Create another file:

```text
main.py
```

Write:

```python
import calculator

print(calculator.add(10, 20))
print(calculator.subtract(20, 10))
print(calculator.multiply(5, 4))
```

### Output

```text
30
10
20
```

### Important Syntax

```python
module_name.function_name()
```

Example:

```python
calculator.add()
```

---

# 5. `from ... import`

Instead of importing the complete module, we can import a particular function.

```python
from calculator import add

print(add(10, 20))
```

### Multiple Functions

```python
from calculator import add, subtract, multiply

print(add(10, 20))
print(subtract(20, 5))
print(multiply(4, 5))
```

---

# 6. Importing Everything

We can use:

```python
from calculator import *
```

Then:

```python
print(add(10, 20))
print(subtract(20, 10))
```

> It is generally clearer to explicitly import the functions that you need.

---

# 7. Module Alias

An alias gives a module a shorter name.

```python
import calculator as calc

print(calc.add(10, 20))
print(calc.multiply(5, 5))
```

Here:

```text
calculator → calc
```

So instead of:

```python
calculator.add()
```

we can write:

```python
calc.add()
```

---

# 8. Built-in Modules

Python also provides many built-in modules.

### Example – `math`

```python
import math

print(math.sqrt(25))
print(math.pow(2, 3))
```

Output:

```text
5.0
8.0
```

### Example – `random`

```python
import random

number = random.randint(1, 10)

print(number)
```

This generates a random integer between 1 and 10.

---

# 🧑‍💻 Day 30 Mini Project

## Calculator Using a Custom Module

### Project Structure

```text
Day30/
│
├── calculator.py
└── main.py
```

---

## `calculator.py`

```python
def add(a, b):
    return a + b


def subtract(a, b):
    return a - b


def multiply(a, b):
    return a * b


def divide(a, b):
    if b == 0:
        return "Cannot divide by zero"
    return a / b
```

---

## `main.py`

```python
import calculator

a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

print("Addition:", calculator.add(a, b))
print("Subtraction:", calculator.subtract(a, b))
print("Multiplication:", calculator.multiply(a, b))
print("Division:", calculator.divide(a, b))
```

### Example Output

```text
Enter first number: 20
Enter second number: 5

Addition: 25.0
Subtraction: 15.0
Multiplication: 100.0
Division: 4.0
```

---

# 📝 Practice Questions

### Question 1
Create a module called `student.py` containing:

```python
student_name
student_age
student_marks
```

Import it into another file and display the values.

### Question 2
Create a module called `calculator.py` with:

- Addition
- Subtraction
- Multiplication
- Division

Import and use the functions from `main.py`.

### Question 3
Create a module called `numbers.py` containing functions to:

- Check even/odd
- Find square
- Find cube

### Question 4
Use `math` to calculate:

- Square root
- Power
- Factorial

---

# 🔗 Day 30 Assignment

## Student Result Module

Create:

```text
student_project/
│
├── marks.py
└── main.py
```

### `marks.py`

Create these functions:

```python
def total(marks):
    pass


def average(marks):
    pass


def highest(marks):
    pass


def lowest(marks):
    pass


def passed_students(marks):
    pass
```

### `main.py`

Import the module:

```python
import marks
```

Display:

```text
Total
Average
Highest
Lowest
Passed Marks
Sorted Marks
```

Try to use concepts from previous classes such as:

- Lambda
- `map()`
- `filter()`
- `sorted()`
- `max()`
- `min()`

---

# 🧠 Quick Revision

| Concept | Purpose |
|---|---|
| Module | Reusable Python file |
| `import` | Import a module |
| `from ... import` | Import specific functions |
| `as` | Create an alias |
| `module.function()` | Access a function from a module |
| `math` | Mathematical operations |
| `random` | Generate random values |

---

# 🏠 Homework

### Task 1 – Calculator Module
Create a calculator module with at least 5 operations.

### Task 2 – Student Module
Create a module that calculates:

- Total
- Average
- Highest
- Lowest
- Pass/Fail

### Task 3 – Number Module
Create a module with functions for:

- Even/Odd
- Square
- Cube
- Prime checking

---

## 📌 Key Takeaways

```python
import calculator
```

```python
calculator.add(10, 20)
```

```python
from calculator import add
```

```python
import calculator as calc
```

Modules make Python projects **organized, reusable, and easier to maintain**.

---

## ✅ Topics Completed

- Python Modules
- Custom Modules
- `import`
- `from ... import`
- Module Aliases
- Built-in Modules
- `math`
- `random`
- Custom Calculator Module
- Module-based Project
