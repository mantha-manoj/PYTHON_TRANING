# Python 45 Days – Day 10 Notes

## Operators – II

**Duration:** 1 Hour 30 Minutes  
**Day:** 10

---

## 1. Learning Objectives

By the end of Day 10, you should understand:

- Comparison operators
- Logical operators
- Membership operators
- Identity operators
- Difference between `==` and `is`
- Practical use of operators
- Combining multiple conditions

---

# 2. Comparison Operators

Comparison operators are used to compare two values.

The result is always a Boolean value:

- `True`
- `False`

| Operator | Meaning | Example |
|---|---|---|
| `==` | Equal to | `10 == 10` |
| `!=` | Not equal to | `10 != 5` |
| `>` | Greater than | `10 > 5` |
| `<` | Less than | `5 < 10` |
| `>=` | Greater than or equal to | `10 >= 10` |
| `<=` | Less than or equal to | `5 <= 10` |

### Example

```python
a = 10
b = 20

print(a == b)
print(a != b)
print(a > b)
print(a < b)
print(a >= b)
print(a <= b)
```

Output:

```text
False
True
False
True
False
True
```

### Important

Comparison operators always produce a Boolean result.

```python
x = 10
y = 20

result = x < y

print(result)
print(type(result))
```

Output:

```text
True
<class 'bool'>
```

---

# 3. Logical Operators

Logical operators are used to combine multiple conditions.

Python provides:

```text
and
or
not
```

---

## `and`

`and` returns `True` only when both conditions are `True`.

```python
print(True and True)
print(True and False)
print(False and True)
print(False and False)
```

Output:

```text
True
False
False
False
```

### Example

```python
age = 25
salary = 50000

print(age >= 18 and salary >= 30000)
```

Output:

```text
True
```

Both conditions are true.

---

## `or`

`or` returns `True` when at least one condition is `True`.

```python
print(True or True)
print(True or False)
print(False or True)
print(False or False)
```

Output:

```text
True
True
True
False
```

### Example

```python
marks = 30
attendance = 80

print(marks >= 35 or attendance >= 75)
```

Output:

```text
True
```

The second condition is true.

---

## `not`

`not` reverses the Boolean result.

```python
print(not True)
print(not False)
```

Output:

```text
False
True
```

### Example

```python
age = 20

print(not age < 18)
```

Output:

```text
True
```

---

# 4. Logical Operators Truth Table

| A | B | A and B | A or B |
|---|---|---|---|
| True | True | True | True |
| True | False | False | True |
| False | True | False | True |
| False | False | False | False |

For `not`:

| A | not A |
|---|---|
| True | False |
| False | True |

---

# 5. Membership Operators

Membership operators check whether a value exists inside a collection.

Python provides:

```text
in
not in
```

## `in`

```python
languages = ["Python", "Java", "C"]

print("Python" in languages)
print("HTML" in languages)
```

Output:

```text
True
False
```

## `not in`

```python
languages = ["Python", "Java", "C"]

print("Python" not in languages)
print("HTML" not in languages)
```

Output:

```text
False
True
```

---

## Membership with Strings

```python
name = "Python Programming"

print("Python" in name)
print("Java" in name)
```

Output:

```text
True
False
```

Character checking also works:

```python
word = "Python"

print("P" in word)
print("z" in word)
```

Output:

```text
True
False
```

---

# 6. Identity Operators

Identity operators check whether two variables refer to the same object.

Python provides:

```text
is
is not
```

### Example

```python
a = [10, 20]
b = a

print(a is b)
```

Output:

```text
True
```

Both variables refer to the same list object.

---

# 7. `==` vs `is`

This is an important Python and interview concept.

### `==`

Checks whether two objects have the same **value**.

### `is`

Checks whether two variables refer to the same **object in memory**.

Example:

```python
a = [10, 20]
b = [10, 20]

print(a == b)
print(a is b)
```

Output:

```text
True
False
```

Why?

Both lists contain the same values, so:

```python
a == b
```

is `True`.

But they are separate list objects, so:

```python
a is b
```

is `False`.

---

## Another Example

```python
a = [10, 20]
b = a
c = [10, 20]

print(a == b)
print(a is b)

print(a == c)
print(a is c)
```

Output:

```text
True
True
True
False
```

### Remember

```text
==  → compares values
is  → compares object identity
```

---

# 8. `is not`

`is not` returns `True` when two variables do not refer to the same object.

```python
a = [1, 2]
b = [1, 2]

print(a is not b)
```

Output:

```text
True
```

---

# 9. Real-Life Example – Student Eligibility

Suppose a student must:

- Be at least 18 years old
- Have marks of at least 60

```python
age = 20
marks = 75

eligible = age >= 18 and marks >= 60

print(eligible)
```

Output:

```text
True
```

This demonstrates how comparison and logical operators work together.

---

# 10. Practical Program – Student Eligibility Checker

```python
age = int(input("Enter your age: "))
marks = float(input("Enter your marks: "))

age_valid = age >= 18
marks_valid = marks >= 60

print("Age condition:", age_valid)
print("Marks condition:", marks_valid)

print("Eligible:", age_valid and marks_valid)
```

### Sample Input

```text
Enter your age: 21
Enter your marks: 75
```

### Output

```text
Age condition: True
Marks condition: True
Eligible: True
```

---

# 11. Combined Operators Program

```python
a = 10
b = 20

# Comparison
print("a == b:", a == b)
print("a != b:", a != b)
print("a > b:", a > b)
print("a < b:", a < b)

# Logical
print("AND:", a < b and b > 15)
print("OR:", a > b or b > 15)
print("NOT:", not a > b)

# Membership
numbers = [10, 20, 30, 40]

print("20 in numbers:", 20 in numbers)
print("50 not in numbers:", 50 not in numbers)

# Identity
x = numbers
y = numbers

print("x is y:", x is y)
```

---

# 12. Day 10 Quick Reference

## Comparison

```text
==   Equal
!=   Not equal
>    Greater than
<    Less than
>=   Greater than or equal
<=   Less than or equal
```

## Logical

```text
and  Both conditions must be True
or   At least one condition must be True
not  Reverses the Boolean result
```

## Membership

```text
in      Exists in collection
not in  Does not exist in collection
```

## Identity

```text
is      Same object
is not  Different objects
```

---

# 13. Interview Questions

### Q1. What are comparison operators?

Comparison operators compare two values and return a Boolean result.

### Q2. What is the difference between `and` and `or`?

`and` requires both conditions to be true, while `or` requires at least one condition to be true.

### Q3. What does `not` do?

It reverses a Boolean result.

### Q4. What are membership operators?

`in` and `not in` are membership operators used to check whether a value exists in a collection.

### Q5. What are identity operators?

`is` and `is not` are identity operators used to check whether variables refer to the same object.

### Q6. Difference between `==` and `is`?

```text
==  → compares values
is  → compares object identity
```

---

# 14. Practice Task

Create a **Student Eligibility Checker**.

Take the following inputs:

```text
Name
Age
Marks
Course
```

Requirements:

1. Check whether age is greater than or equal to 18.
2. Check whether marks are greater than or equal to 60.
3. Check whether the course is Python or Java.
4. Combine the conditions.
5. Display whether the student is eligible.

Useful operators:

```python
age >= 18
marks >= 60
course in ["Python", "Java"]
```

Combine them using:

```python
and
```

---

# 15. Day 10 Summary

Today we learned four major categories of operators:

```text
1. Comparison
   == != > < >= <=

2. Logical
   and or not

3. Membership
   in not in

4. Identity
   is is not
```

### Most Important Concept

```text
== → Same value
is → Same object
```

These operators will be heavily used with **conditional statements**, which are the next important step in Python programming.
