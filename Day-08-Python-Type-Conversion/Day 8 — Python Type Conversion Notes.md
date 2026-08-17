# 🐍 Day 8 — Type Conversion

**Date:** 17-Aug-2026  
**Day:** 8 of 45  
**Topic:** Type Conversion

---

## 📌 Today's Objective

Learn how to convert values from one Python data type to another using built-in conversion functions.

Today's practice focuses on:

- Taking input as a string
- Converting a string to `int`
- Converting a string to `float`
- Converting numbers to `str`
- Understanding `int()`, `float()`, and `str()`
- Checking data types using `type()`

---

## 1. What is Type Conversion?

**Type conversion** is the process of changing a value from one data type to another.

For example:

```python
age = "22"

print(type(age))
```

Output:

```text
<class 'str'>
```

We can convert it to an integer:

```python
age = int(age)

print(type(age))
```

Output:

```text
<class 'int'>
```

So:

```text
"22"  →  22
str      int
```

---

# 2. Why Do We Need Type Conversion?

The `input()` function always returns data as a **string**.

Example:

```python
age = input("Enter your age: ")

print(age)
print(type(age))
```

If the user enters:

```text
22
```

The output will be:

```text
22
<class 'str'>
```

Even though `22` looks like a number, Python receives it as a string.

Therefore, if we want to perform mathematical operations, we need to convert it.

```python
age = int(input("Enter your age: "))
```

Now `age` is an integer.

---

# 3. Common Type Conversion Functions

| Function | Purpose | Example | Result |
|---|---|---|---|
| `int()` | Converts to integer | `int("25")` | `25` |
| `float()` | Converts to float | `float("25.5")` | `25.5` |
| `str()` | Converts to string | `str(25)` | `"25"` |
| `bool()` | Converts to Boolean | `bool(1)` | `True` |

Today's main focus:

```python
int()
float()
str()
```

---

# 4. `int()` — Convert to Integer

The `int()` function converts a compatible value into an integer.

### Example

```python
age = "22"

age = int(age)

print(age)
print(type(age))
```

Output:

```text
22
<class 'int'>
```

### More examples

```python
print(int("10"))
print(int("100"))
print(int(25.8))
```

Output:

```text
10
100
25
```

### Important

When converting a float to an integer, the decimal part is removed.

```python
number = 25.8

print(int(number))
```

Output:

```text
25
```

It does **not** round the number.

---

# 5. `float()` — Convert to Floating-Point Number

The `float()` function converts a compatible value into a floating-point number.

### Example

```python
marks = "85.5"

marks = float(marks)

print(marks)
print(type(marks))
```

Output:

```text
85.5
<class 'float'>
```

### More examples

```python
print(float("10"))
print(float("25.5"))
print(float(20))
```

Output:

```text
10.0
25.5
20.0
```

---

# 6. `str()` — Convert to String

The `str()` function converts a value into a string.

### Example

```python
age = 22

age = str(age)

print(age)
print(type(age))
```

Output:

```text
22
<class 'str'>
```

### Another example

```python
marks = 85.5

marks = str(marks)

print(marks)
print(type(marks))
```

Output:

```text
85.5
<class 'str'>
```

---

# 7. Main Day-8 Program

## Student Age and Marks

### Requirement

- Take age as input
- Convert age to `int`
- Take marks as input
- Convert marks to `float`
- Display the values and their types

```python
age = input("Enter your age: ")
marks = input("Enter your marks: ")

age = int(age)
marks = float(marks)

print("Age:", age)
print("Age type:", type(age))

print("Marks:", marks)
print("Marks type:", type(marks))
```

### Sample Input

```text
Enter your age: 22
Enter your marks: 85.5
```

### Output

```text
Age: 22
Age type: <class 'int'>
Marks: 85.5
Marks type: <class 'float'>
```

---

# 8. Shorter Version

Instead of converting after taking input:

```python
age = input("Enter your age: ")
age = int(age)
```

We can directly convert the input:

```python
age = int(input("Enter your age: "))
```

Similarly:

```python
marks = float(input("Enter your marks: "))
```

### Complete Program

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
marks = float(input("Enter your marks: "))

print("Name:", name)
print("Age:", age)
print("Marks:", marks)
```

---

# 9. Type Conversion Examples

## String → Integer

```python
number = "100"

number = int(number)

print(number)
print(type(number))
```

---

## String → Float

```python
number = "100.50"

number = float(number)

print(number)
print(type(number))
```

---

## Integer → String

```python
number = 100

number = str(number)

print(number)
print(type(number))
```

---

## Float → Integer

```python
number = 100.75

number = int(number)

print(number)
```

Output:

```text
100
```

---

## Integer → Float

```python
number = 100

number = float(number)

print(number)
```

Output:

```text
100.0
```

---

# 10. Type Conversion vs Type Casting

These terms are often used interchangeably in Python.

### Type Conversion

Changing one data type into another.

```python
x = "10"

x = int(x)
```

### Type Casting

Explicitly converting a value using functions such as:

```python
int()
float()
str()
bool()
```

For practical Python programming, you will commonly see both terms used for the same concept.

---

# 11. Implicit vs Explicit Conversion

## Implicit Conversion

Python automatically converts the type when appropriate.

Example:

```python
x = 10
y = 2.5

result = x + y

print(result)
print(type(result))
```

Output:

```text
12.5
<class 'float'>
```

Python automatically converts the integer to a float for the operation.

---

## Explicit Conversion

The programmer manually performs the conversion.

```python
age = "22"

age = int(age)
```

Here we explicitly told Python to convert the string into an integer.

---

# 12. Important Error — `ValueError`

Not every string can be converted into a number.

This works:

```python
age = int("22")
```

But this does not:

```python
age = int("hello")
```

Python raises:

```text
ValueError
```

Similarly:

```python
marks = float("abc")
```

also raises a `ValueError`.

### Why?

Because `"hello"` and `"abc"` do not represent valid numeric values.

---

# 13. String Addition vs Number Addition

This is an important concept.

### String concatenation

```python
a = "10"
b = "20"

print(a + b)
```

Output:

```text
1020
```

Because both values are strings.

---

### Numeric addition

```python
a = int("10")
b = int("20")

print(a + b)
```

Output:

```text
30
```

### Remember

```text
"10" + "20" → "1020"
10 + 20     → 30
```

---

# 14. Taking Two Numbers from User

```python
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

sum = num1 + num2

print("Sum:", sum)
```

### Sample Output

```text
Enter first number: 10
Enter second number: 20
Sum: 30
```

---

# 15. Complete Student Program

```python
name = input("Enter student name: ")
age = int(input("Enter age: "))
marks = float(input("Enter marks: "))

print("\n--- Student Details ---")
print("Name:", name)
print("Age:", age)
print("Marks:", marks)

print("\n--- Data Types ---")
print("Name type:", type(name))
print("Age type:", type(age))
print("Marks type:", type(marks))
```

### Sample Output

```text
Enter student name: Pavan
Enter age: 22
Enter marks: 85.5

--- Student Details ---
Name: Pavan
Age: 22
Marks: 85.5

--- Data Types ---
Name type: <class 'str'>
Age type: <class 'int'>
Marks type: <class 'float'>
```

---

# 🧠 Key Points to Remember

1. `input()` always returns a string.
2. Use `int()` when an integer is required.
3. Use `float()` when a decimal number is required.
4. Use `str()` to convert a value into a string.
5. `type()` is used to check the data type.
6. Invalid numeric conversion can produce `ValueError`.
7. `int(25.8)` gives `25`; it does not round to `26`.
8. `"10" + "20"` gives `"1020"`.
9. `10 + 20` gives `30`.

---

# 💻 Day-8 Practice Programs

## Program 1 — Convert Age

Take age as a string and convert it to an integer.

```python
age = input("Enter your age: ")

age = int(age)

print("Age:", age)
print("Type:", type(age))
```

---

## Program 2 — Convert Marks

Take marks as input and convert them to float.

```python
marks = input("Enter your marks: ")

marks = float(marks)

print("Marks:", marks)
print("Type:", type(marks))
```

---

## Program 3 — Add Two Numbers

Take two numbers using `input()` and find their sum.

```python
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

print("Sum:", num1 + num2)
```

---

## Program 4 — Integer to String

```python
number = 100

number = str(number)

print(number)
print(type(number))
```

---

## Program 5 — Student Details

Take:

- Student name
- Age
- Marks

Convert age to `int` and marks to `float`.

```python
name = input("Enter name: ")
age = int(input("Enter age: "))
marks = float(input("Enter marks: "))

print("Name:", name)
print("Age:", age)
print("Marks:", marks)
```

---

# 🎯 Interview Questions

### 1. What does `input()` return?

`input()` always returns a value of type `str`.

---

### 2. How do you convert a string to an integer?

```python
int("25")
```

---

### 3. How do you convert a string to a float?

```python
float("25.5")
```

---

### 4. How do you convert an integer to a string?

```python
str(25)
```

---

### 5. What is the output of this?

```python
x = "10"
y = "20"

print(x + y)
```

Output:

```text
1020
```

Because both values are strings.

---

### 6. What is the output?

```python
x = int("10")
y = int("20")

print(x + y)
```

Output:

```text
30
```

---

### 7. What happens when we execute `int("abc")`?

Python raises a `ValueError` because `"abc"` cannot be converted into an integer.

---

# 📝 Day-8 Summary

Today's concept:

```text
                 TYPE CONVERSION
                       |
        +--------------+--------------+
        |              |              |
      int()          float()         str()
        |              |              |
    Integer          Float          String
```

The most important rule:

> **`input()` always returns a string. Convert the input when you need a numeric data type.**

---

# 🚀 Day-8 Checklist

- [ ] Understand type conversion
- [ ] Understand `int()`
- [ ] Understand `float()`
- [ ] Understand `str()`
- [ ] Understand why `input()` needs conversion
- [ ] Practice integer conversion
- [ ] Practice float conversion
- [ ] Practice string conversion
- [ ] Practice adding converted numbers
- [ ] Understand `ValueError`
- [ ] Complete all 5 practice programs

---

## 📚 Day-8 Quick Reference

```python
# String to integer
x = int("10")

# String to float
x = float("10.5")

# Integer to string
x = str(10)

# Float to string
x = str(10.5)

# Integer to float
x = float(10)

# Check type
print(type(x))

# User input as integer
age = int(input("Enter age: "))

# User input as float
marks = float(input("Enter marks: "))
```

**Day 8 completed — Type Conversion ✅**