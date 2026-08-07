# 🐍 Day 2 – Python Installation, IDE Setup & Input/Output

Welcome to **Day 2** of the **Python 45 Days Training Program**.

In today's session, you will learn how to install Python, set up Visual Studio Code, understand the Python execution process, create Python files, and work with input and output functions.

---

# 🎯 Learning Objectives

By the end of this session, you will be able to:

- Install Python on your computer.
- Install and configure Visual Studio Code.
- Verify the Python installation.
- Understand the Python Interpreter.
- Create and run Python programs.
- Use the `print()` function.
- Take user input using the `input()` function.
- Display formatted output.

---

# 📥 Installing Python

## Step 1

Visit the official Python website:

https://python.org/downloads

Download the latest stable version of Python for your operating system.

---

## Step 2

Run the installer.

Before clicking **Install Now**, make sure to enable:

✅ **Add Python to PATH**

Then click **Install Now**.

---

## Step 3

Verify Installation

Open **Command Prompt** or **Terminal**.

```bash
python --version
```

or

```bash
py --version
```

Example Output

```text
Python 3.13.x
```

---

# 💻 Installing Visual Studio Code

Download Visual Studio Code:

https://code.visualstudio.com

Install the following extension:

- Python (Microsoft)

This extension provides:

- Syntax Highlighting
- IntelliSense
- Debugging
- Auto Completion
- Code Formatting

---

# 📂 Creating Your First Python Project

Create a folder.

Example:

```text
PythonTraining
```

Open this folder in Visual Studio Code.

Create a new file.

```text
hello.py
```

---

# ▶ Running Python Programs

### Method 1

Using Terminal

```bash
python hello.py
```

---

### Method 2

```bash
py hello.py
```

---

### Method 3

Run using the ▶ Run button in Visual Studio Code.

---

# 🧠 Python Interpreter

Python is an **interpreted programming language**.

### Execution Process

```text
Python Code (.py)
        │
        ▼
Python Interpreter
        │
        ▼
Machine Code
        │
        ▼
Output
```

Unlike compiled languages, Python executes the code line by line.

---

# 🖨 Output Using `print()`

The `print()` function is used to display information on the screen.

Example

```python
print("Welcome to Python")
```

Output

```text
Welcome to Python
```

---

# ✍ Multiple Print Statements

```python
print("Python")
print("Java")
print("C++")
```

Output

```text
Python
Java
C++
```

---

# 🧾 Printing Multiple Values

```python
name = "Rahul"
age = 21

print(name, age)
```

Output

```text
Rahul 21
```

---

# 🎯 Taking Input

The `input()` function allows users to enter data.

Example

```python
name = input("Enter your name: ")

print(name)
```

Output

```text
Enter your name: Rahul
Rahul
```

---

# 📌 Input Always Returns a String

Example

```python
age = input("Enter your age: ")

print(type(age))
```

Output

```text
<class 'str'>
```

To perform calculations, convert the input into the required data type.

---

# 🔢 Example: Integer Input

```python
age = int(input("Enter your age: "))

print(age)
```

---

# ➕ Addition Program

```python
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

sum = num1 + num2

print("Sum =", sum)
```

Example Output

```text
Enter first number: 10
Enter second number: 20

Sum = 30
```

---

# ✖ Multiplication Program

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

print("Multiplication =", a * b)
```

---

# 📋 Mini Practice Programs

## Program 1

Display your name.

```python
print("My Name is Pavan")
```

---

## Program 2

Take user name as input.

```python
name = input("Enter your name: ")

print("Hello", name)
```

---

## Program 3

Take age as input.

```python
age = int(input("Enter your age: "))

print("Your age is", age)
```

---

## Program 4

Addition of two numbers.

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

print("Addition =", a + b)
```

---

## Program 5

Display student details.

```python
name = input("Enter Name: ")
college = input("Enter College: ")
city = input("Enter City: ")

print("Name :", name)
print("College :", college)
print("City :", city)
```

---

# 💡 Best Practices

- Use meaningful variable names.
- Save Python files using the `.py` extension.
- Keep your code properly indented.
- Write one statement per line.
- Practice every example by yourself.

---

# ❓ Interview Questions

1. What is Python Interpreter?
2. Difference between Compiler and Interpreter?
3. What is Visual Studio Code?
4. What is the purpose of the `print()` function?
5. What is the purpose of the `input()` function?
6. What type of value does `input()` return?
7. How do you convert a string into an integer?
8. What is the extension of Python files?
9. How do you check the installed Python version?
10. Why should we add Python to PATH?

---

# 🏠 Assignment

## Task 1

Create a program to display:

- Name
- Age
- College
- City

using the `input()` function.

---

## Task 2

Write programs to:

- Add two numbers.
- Subtract two numbers.
- Multiply two numbers.
- Divide two numbers.

using user input.

---

## Task 3

Create a program that takes the user's:

- Name
- Age
- Favorite Programming Language

and displays a welcome message.

---

# 📝 Summary

Today you learned:

- ✅ Python Installation
- ✅ Visual Studio Code Setup
- ✅ Python Interpreter
- ✅ Creating Python Files
- ✅ Running Python Programs
- ✅ `print()` Function
- ✅ `input()` Function
- ✅ Basic User Input Programs
- ✅ Arithmetic Operations

---

# 📚 Next Session

## Day 3 – Python Variables, Keywords & Data Types

Keep practicing today's programs before moving to the next session.

Happy Coding! 🚀🐍