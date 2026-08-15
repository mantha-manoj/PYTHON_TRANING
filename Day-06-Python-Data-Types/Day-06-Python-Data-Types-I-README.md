# 🐍 Python – Day 6: Data Types – I

> **Course:** Python Full Course – 45 Working Days  
> **Day:** 6  
> **Topic:** Data Types – I  
> **Date:** 13-Aug-2026

---

## 📌 Learning Objectives

By the end of Day 6, students should be able to:

- Understand what a data type is.
- Identify the basic built-in data types in Python.
- Understand `int`, `float`, `complex`, `str`, and `bool`.
- Create variables with different data types.
- Check the data type of a value using `type()`.
- Understand the difference between values and their data types.
- Write simple programs using different data types.

---

# 1. What is a Data Type?

A **data type** tells Python what kind of value a variable contains.

For example:

```python
age = 22
name = "Pavan"
salary = 45000.50
is_student = True
```

Here:

- `22` → Integer
- `"Pavan"` → String
- `45000.50` → Float
- `True` → Boolean

Python automatically identifies the data type when we assign a value to a variable.

---

# 2. Why Do We Need Data Types?

Data types help Python understand:

- What kind of data is stored.
- What operations can be performed.
- How the value should be handled internally.

Example:

```python
a = 10
b = 20

print(a + b)
```

Output:

```text
30
```

But:

```python
a = "10"
b = "20"

print(a + b)
```

Output:

```text
1020
```

The first example performs **numeric addition**.

The second example performs **string concatenation**.

So, the data type affects how Python behaves.

---

# 3. Python's Basic Data Types

In today's class, we focus on:

| Data Type | Example | Meaning |
|---|---|---|
| `int` | `10` | Whole numbers |
| `float` | `10.5` | Decimal numbers |
| `complex` | `2 + 3j` | Complex numbers |
| `str` | `"Python"` | Text |
| `bool` | `True` / `False` | Logical values |

---

# 4. Integer (`int`)

An integer represents **whole numbers without decimal points**.

Examples:

```python
age = 22
marks = 95
temperature = -5
count = 0
```

Check the type:

```python
age = 22

print(age)
print(type(age))
```

Output:

```text
22
<class 'int'>
```

### Integer examples

```python
a = 100
b = -50
c = 0

print(type(a))
print(type(b))
print(type(c))
```

All three are integers.

### Integer operations

```python
a = 10
b = 3

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a // b)
print(a % b)
print(a ** b)
```

---

# 5. Float (`float`)

A float represents a **number containing a decimal point**.

Examples:

```python
price = 99.99
percentage = 85.5
height = 175.5
temperature = -2.5
```

Example:

```python
price = 99.99

print(price)
print(type(price))
```

Output:

```text
99.99
<class 'float'>
```

### Integer vs Float

```python
a = 10
b = 10.0

print(type(a))
print(type(b))
```

Output:

```text
<class 'int'>
<class 'float'>
```

Even though both represent the number 10, their data types are different.

---

# 6. Complex (`complex`)

A complex number contains:

- A **real part**
- An **imaginary part**

Python uses `j` to represent the imaginary part.

Example:

```python
z = 2 + 3j

print(z)
print(type(z))
```

Output:

```text
(2+3j)
<class 'complex'>
```

### More examples

```python
a = 5 + 2j
b = 10 - 4j

print(a)
print(b)
```

### Access real and imaginary parts

```python
z = 5 + 3j

print(z.real)
print(z.imag)
```

Output:

```text
5.0
3.0
```

### Important

In Python:

```python
3j
```

means an imaginary number.

Do not confuse `j` with a normal variable unless it is being used as part of a complex number.

---

# 7. String (`str`)

A string represents **text or a sequence of characters**.

Strings can be written using:

- Single quotes `' '`
- Double quotes `" "`
- Triple quotes `` or `""" """`

Examples:

```python
name = "Pavan"
course = 'Python'
city = "Bangalore"
```

Check the type:

```python
name = "Pavan"

print(name)
print(type(name))
```

Output:

```text
Pavan
<class 'str'>
```

### String can contain numbers

```python
a = "100"

print(a)
print(type(a))
```

The value looks like a number, but its type is `str`.

Therefore:

```python
a = "10"
b = "20"

print(a + b)
```

Output:

```text
1020
```

This is **concatenation**, not arithmetic addition.

---

# 8. Boolean (`bool`)

Boolean represents one of two logical values:

```python
True
False
```

Example:

```python
is_student = True
is_logged_in = False

print(is_student)
print(type(is_student))
```

Output:

```text
True
<class 'bool'>
```

### Boolean values are commonly used in conditions

```python
age = 22

print(age >= 18)
```

Output:

```text
True
```

Another example:

```python
marks = 35

print(marks >= 40)
```

Output:

```text
False
```

---

# 9. The `type()` Function

The `type()` function is used to identify the data type of a value.

Syntax:

```python
type(value)
```

Example:

```python
x = 100

print(type(x))
```

Output:

```text
<class 'int'>
```

More examples:

```python
a = 10
b = 10.5
c = 2 + 3j
d = "Python"
e = True

print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(type(e))
```

Output:

```text
<class 'int'>
<class 'float'>
<class 'complex'>
<class 'str'>
<class 'bool'>
```

---

# 10. Variables with Different Data Types

A variable can store different types of values.

```python
name = "Pavan"
age = 22
percentage = 85.5
complex_number = 2 + 3j
is_student = True

print(name, type(name))
print(age, type(age))
print(percentage, type(percentage))
print(complex_number, type(complex_number))
print(is_student, type(is_student))
```

---

# 11. Python is Dynamically Typed

Python is a **dynamically typed language**.

This means we do not have to explicitly declare the data type of a variable.

Example:

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

The same variable name can refer to values of different types at different times.

---

# 12. Checking Multiple Values

We can use `type()` to inspect multiple variables.

```python
name = "Rahul"
age = 21
salary = 45000.75
is_employee = True
number = 3 + 4j

print("Name:", name, "| Type:", type(name))
print("Age:", age, "| Type:", type(age))
print("Salary:", salary, "| Type:", type(salary))
print("Employee:", is_employee, "| Type:", type(is_employee))
print("Number:", number, "| Type:", type(number))
```

---

# 13. Real-World Example

Imagine a student management system:

```python
student_name = "Rahul"
student_age = 21
student_percentage = 82.5
student_result = True
```

Here:

- `student_name` → `str`
- `student_age` → `int`
- `student_percentage` → `float`
- `student_result` → `bool`

This is how real applications store different kinds of information.

---

# 14. Important Difference: `"10"` vs `10`

This is one of the most important concepts for beginners.

```python
a = 10
b = "10"

print(type(a))
print(type(b))
```

Output:

```text
<class 'int'>
<class 'str'>
```

Now:

```python
print(a + 5)
```

Output:

```text
15
```

But:

```python
print(b + "5")
```

Output:

```text
105
```

Because:

- `10 + 5` → arithmetic addition
- `"10" + "5"` → string concatenation

---

# 15. Common Beginner Mistakes

## Mistake 1: Confusing number and string

Wrong assumption:

```python
age = "22"
```

This is a string, not an integer.

Check it:

```python
print(type(age))
```

---

## Mistake 2: Using lowercase boolean values

Incorrect:

```python
is_student = true
```

Correct:

```python
is_student = True
```

Python is case-sensitive.

---

## Mistake 3: Forgetting quotes for strings

Incorrect:

```python
name = Pavan
```

Correct:

```python
name = "Pavan"
```

---

## Mistake 4: Expecting `10 + "20"` to work

```python
print(10 + "20")
```

This causes a `TypeError` because Python cannot directly add an integer and a string.

---

# 16. Day-6 Practice Program

### Problem Statement

Create variables for:

- Integer
- Float
- Complex number
- String
- Boolean

Then print:

1. The value
2. The data type of each variable

### Solution

```python
number = 100
price = 99.99
complex_number = 3 + 4j
name = "Python"
is_active = True

print("Integer:", number)
print("Type:", type(number))

print("Float:", price)
print("Type:", type(price))

print("Complex:", complex_number)
print("Type:", type(complex_number))

print("String:", name)
print("Type:", type(name))

print("Boolean:", is_active)
print("Type:", type(is_active))
```

---

# 17. Student Practice Questions

## Practice 1

Create variables for:

```text
Name
Age
Height
Percentage
Is Student
```

Print the value and data type of each.

---

## Practice 2

Create the following variables:

```python
a = 25
b = 25.5
c = 5 + 6j
d = "25"
e = False
```

Print the type of every variable.

---

## Practice 3

Predict the output before running:

```python
a = 10
b = "20"

print(type(a))
print(type(b))
```

---

## Practice 4

Predict the output:

```python
x = 10
x = "Python"
x = 10.5

print(x)
print(type(x))
```

---

# 18. Interview Questions

### Q1. What is a data type?

A data type defines the kind of value stored in a variable.

### Q2. What are the basic data types covered today?

`int`, `float`, `complex`, `str`, and `bool`.

### Q3. How do you check the type of a variable?

Using the `type()` function.

```python
type(variable)
```

### Q4. What is the difference between `10` and `"10"`?

`10` is an integer, while `"10"` is a string.

### Q5. What is a Boolean?

A Boolean represents either `True` or `False`.

### Q6. How do you represent a complex number in Python?

Using `j` for the imaginary part.

```python
2 + 3j
```

### Q7. Is Python statically typed or dynamically typed?

Python is dynamically typed.

---

# 19. Quick Revision

```text
int      → Whole numbers
float    → Decimal numbers
complex  → Real + imaginary numbers
str      → Text
bool     → True / False
type()   → Checks the data type
```

Example:

```python
a = 10
b = 10.5
c = 2 + 3j
d = "Python"
e = True

print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(type(e))
```

---

# 🎯 Day-6 Assignment

Create a Python program called:

```text
day6_datatypes.py
```

The program should:

1. Create one variable of each type:
   - `int`
   - `float`
   - `complex`
   - `str`
   - `bool`
2. Print every value.
3. Print the data type using `type()`.
4. Add comments explaining each variable.
5. Run the program successfully.
6. Push the program to GitHub.

### Expected GitHub structure

```text
Python-45-Days/
│
├── Day-01/
├── Day-02/
├── Day-03/
├── Day-04/
├── Day-05/
│
└── Day-06/
    ├── README.md
    └── day6_datatypes.py
```

---

# ✅ Day-6 Checklist

- [ ] Understand what data types are
- [ ] Understand `int`
- [ ] Understand `float`
- [ ] Understand `complex`
- [ ] Understand `str`
- [ ] Understand `bool`
- [ ] Understand `type()`
- [ ] Understand dynamic typing
- [ ] Complete the practice programs
- [ ] Complete the Day-6 assignment
- [ ] Push Day-6 work to GitHub

---

## 🚀 Key Takeaway

> **A data type tells Python what kind of value a variable contains and helps Python determine how that value should be handled.**

Mastering data types is essential because almost every Python program works with different kinds of data.
