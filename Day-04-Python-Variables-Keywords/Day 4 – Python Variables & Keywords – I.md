# 🐍 Python – Day 4: Variables & Keywords – I

## 🎯 Learning Objectives

By the end of this session, you should be able to:

- Understand what a variable is.
- Create and use variables in Python.
- Store different types of values in variables.
- Follow Python variable naming rules.
- Understand dynamic typing.
- Update/reassign variable values.
- Perform multiple assignments.
- Swap two variables.
- Use variables with the `print()` function.

---

## 1. What is a Variable?

A **variable** is a name used to refer to a value in a Python program.

Think of a variable like a labeled box that holds a value.

```python
name = "Pavan"
age = 23
marks = 85
```

Here:

- `name` → variable
- `age` → variable
- `marks` → variable
- `"Pavan"` → value
- `23` → value
- `85` → value

### Assignment Operator `=`

The `=` operator is used to **assign a value to a variable**.

```python
age = 23
```

This means:

> Assign the value `23` to the variable `age`.

It does **not** mean mathematical equality.

---

## 2. Creating Variables

Python does not require us to declare a variable before using it.

```python
name = "Rahul"
age = 21
percentage = 87.5
is_passed = True
```

We can then print the values:

```python
print(name)
print(age)
print(percentage)
print(is_passed)
```

Output:

```text
Rahul
21
87.5
True
```

---

## 3. Variables Can Store Different Types of Values

A variable can refer to different kinds of values.

```python
name = "Pavan"
age = 23
percentage = 85.5
is_student = True
```

Examples:

| Variable | Value |
|---|---|
| `name` | `"Pavan"` |
| `age` | `23` |
| `percentage` | `85.5` |
| `is_student` | `True` |

We will learn data types in detail in upcoming sessions.

---

# 4. Variable Naming Rules

Python has rules for naming variables.

## Rule 1: Letters are allowed

```python
name = "Pavan"
student = "Rahul"
```

---

## Rule 2: Numbers can be used, but not at the beginning

✅ Valid:

```python
student1 = "Pavan"
student2 = "Rahul"
```

❌ Invalid:

```python
1student = "Pavan"
```

A variable name cannot start with a number.

---

## Rule 3: Underscore `_` is allowed

```python
student_name = "Pavan"
student_age = 23
total_marks = 450
```

---

## Rule 4: Spaces are not allowed

❌ Incorrect:

```python
student name = "Pavan"
```

✅ Correct:

```python
student_name = "Pavan"
```

---

## Rule 5: Special characters are not allowed in normal variable names

❌ Incorrect:

```python
student-name = "Pavan"
student@name = "Pavan"
```

✅ Correct:

```python
student_name = "Pavan"
```

---

## Rule 6: Variable names are case-sensitive

Python treats uppercase and lowercase letters differently.

```python
name = "Pavan"
Name = "Rahul"
NAME = "Kiran"
```

These are three different variables.

```python
print(name)
print(Name)
print(NAME)
```

Output:

```text
Pavan
Rahul
Kiran
```

---

# 5. Recommended Naming Style

Python commonly uses **snake_case** for variable names.

Example:

```python
student_name = "Pavan"
student_age = 23
student_marks = 85
college_name = "ABC College"
```

Prefer meaningful names:

```python
student_name = "Pavan"
```

Instead of:

```python
x = "Pavan"
```

Meaningful variable names make programs easier to understand.

---

# 6. Dynamic Typing in Python

Python is a **dynamically typed language**.

We do not have to explicitly specify the data type when creating a variable.

```python
x = 10
```

Later, the same variable can refer to another type of value:

```python
x = "Python"
```

And later:

```python
x = 25.5
```

Python determines the type based on the value assigned.

### Example

```python
x = 10
print(type(x))

x = "Python"
print(type(x))

x = 10.5
print(type(x))
```

Output:

```text
<class 'int'>
<class 'str'>
<class 'float'>
```

The `type()` function tells us the type of the value.

---

# 7. Updating / Reassigning Variables

A variable's value can be changed.

```python
age = 20

print(age)

age = 21

print(age)
```

Output:

```text
20
21
```

The second assignment changes the value associated with `age`.

### Another Example

```python
marks = 70

print("Before:", marks)

marks = 85

print("After:", marks)
```

Output:

```text
Before: 70
After: 85
```

---

# 8. Multiple Assignment

Python allows us to assign multiple values to multiple variables in one statement.

Instead of:

```python
name = "Pavan"
age = 23
marks = 85
```

We can write:

```python
name, age, marks = "Pavan", 23, 85
```

Now:

```python
print(name)
print(age)
print(marks)
```

Output:

```text
Pavan
23
85
```

The assignments happen as:

```text
name  → "Pavan"
age   → 23
marks → 85
```

---

# 9. Assigning the Same Value to Multiple Variables

Python also allows the same value to be assigned to multiple variables.

```python
a = b = c = 100
```

Now:

```python
print(a)
print(b)
print(c)
```

Output:

```text
100
100
100
```

---

# 10. Swapping Two Variables

Python provides a simple way to swap values.

Initially:

```python
a = 10
b = 20
```

We can swap them using:

```python
a, b = b, a
```

Now:

```python
print(a)
print(b)
```

Output:

```text
20
10
```

### Complete Program

```python
a = 10
b = 20

print("Before swapping:")
print("a =", a)
print("b =", b)

a, b = b, a

print("After swapping:")
print("a =", a)
print("b =", b)
```

---

# 11. Variables with `print()`

Variables can be displayed using `print()`.

```python
name = "Pavan"
age = 23

print(name)
print(age)
```

We can also add labels:

```python
print("Name:", name)
print("Age:", age)
```

Output:

```text
Name: Pavan
Age: 23
```

---

# 12. Practical Example – Student Details

```python
name = "Pavan"
age = 23
marks = 85

print("Student Name:", name)
print("Age:", age)
print("Marks:", marks)
```

Output:

```text
Student Name: Pavan
Age: 23
Marks: 85
```

### Using Multiple Assignment

The same program can be written as:

```python
name, age, marks = "Pavan", 23, 85

print("Student Name:", name)
print("Age:", age)
print("Marks:", marks)
```

---

# 13. Common Mistakes

### Mistake 1: Forgetting quotation marks

❌ Incorrect:

```python
name = Pavan
```

✅ Correct:

```python
name = "Pavan"
```

---

### Mistake 2: Starting with a number

❌ Incorrect:

```python
1name = "Pavan"
```

✅ Correct:

```python
name1 = "Pavan"
```

---

### Mistake 3: Using spaces

❌ Incorrect:

```python
student name = "Pavan"
```

✅ Correct:

```python
student_name = "Pavan"
```

---

### Mistake 4: Case sensitivity

```python
Name = "Pavan"

print(name)
```

`Name` and `name` are different variables.

---

# 🧪 Practice Programs

## Program 1 – Personal Details

Create variables for:

- Name
- Age
- City

Display all the values.

Example:

```python
name = "Pavan"
age = 23
city = "Bengaluru"

print("Name:", name)
print("Age:", age)
print("City:", city)
```

---

## Program 2 – Student Details

Create variables for:

- Student name
- Age
- College
- Branch
- Marks

Display all details.

---

## Program 3 – Multiple Assignment

Create three variables using a single statement:

```python
a, b, c = 10, 20, 30
```

Print their values.

---

## Program 4 – Same Value

Create three variables and assign the same value:

```python
x = y = z = 50
```

Print all three variables.

---

## Program 5 – Swap Values

Create:

```python
a = 100
b = 200
```

Swap their values without using a third variable.

Expected technique:

```python
a, b = b, a
```

---

# 🧠 Quick Revision

### What is a variable?

A name used to refer to a value.

### What is `=`?

The assignment operator.

### Can a variable name start with a number?

No.

### Can we use `_` in a variable name?

Yes.

### Are `name` and `Name` the same?

No. Python is case-sensitive.

### Can a variable's value be changed?

Yes.

```python
x = 10
x = 20
```

### What is multiple assignment?

Assigning multiple values to multiple variables in one statement.

```python
a, b, c = 10, 20, 30
```

### How do we assign the same value to multiple variables?

```python
a = b = c = 10
```

### How do we swap two variables in Python?

```python
a, b = b, a
```

---

# 🎯 Day 4 Key Takeaways

```text
Variable
    ↓
name = value

Example:
age = 23

Multiple Assignment:
a, b = 10, 20

Same Value:
a = b = c = 10

Swap:
a, b = b, a

Python Variables:
✔ Dynamically typed
✔ Case-sensitive
✔ Can be reassigned
✔ Support multiple assignment
✔ Follow naming rules
```

## 🚀 Practice Challenge

Create a Python program that stores and displays the following:

```text
===== STUDENT DETAILS =====

Name    : Your Name
Age     : Your Age
College : Your College
Branch  : Your Branch
CGPA    : Your CGPA
```

**Requirements:**

1. Store every value in a separate variable.
2. Use meaningful variable names.
3. Display the information using `print()`.
4. Try using multiple assignment wherever appropriate.