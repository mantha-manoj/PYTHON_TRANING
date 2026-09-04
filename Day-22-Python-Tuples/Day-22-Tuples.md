# Day 22 — Tuples in Python

## 📚 Topic
**Tuples: Creation, Indexing, Slicing, Immutability, Unpacking, `count()` and `index()`**

---

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Understand what a tuple is.
- Create tuples in Python.
- Access tuple elements using indexing.
- Use positive and negative indexing.
- Perform tuple slicing.
- Understand tuple immutability.
- Unpack tuple values into variables.
- Use `count()` and `index()`.
- Loop through a tuple.
- Understand the difference between lists and tuples.

---

# 1. What is a Tuple?

A **tuple** is an ordered collection of elements in Python.

Tuples are:

- Ordered
- Indexed
- Immutable
- Allow duplicate values
- Can contain different data types

Tuples are normally created using parentheses `()`.

```python
subjects = ("Python", "Java", "SQL", "HTML", "CSS")

print(subjects)
print(type(subjects))
```

Output:

```text
('Python', 'Java', 'SQL', 'HTML', 'CSS')
<class 'tuple'>
```

### Simple Definition

> A tuple is an ordered and immutable collection of elements.

---

# 2. List vs Tuple

| List | Tuple |
|---|---|
| Uses `[]` | Uses `()` |
| Mutable | Immutable |
| Elements can be changed | Elements cannot be changed |
| More methods available | Fewer methods available |
| Suitable for changing data | Suitable for fixed data |

### List Example

```python
marks = [80, 90, 75]

marks[0] = 95

print(marks)
```

Output:

```text
[95, 90, 75]
```

### Tuple Example

```python
marks = (80, 90, 75)

marks[0] = 95
```

This gives a `TypeError` because tuples are immutable.

---

# 3. Creating Tuples

## Empty Tuple

```python
t = ()

print(type(t))
```

## Tuple of Numbers

```python
numbers = (10, 20, 30, 40)
```

## Tuple of Strings

```python
languages = ("Python", "Java", "C++")
```

## Mixed Tuple

A tuple can contain different data types.

```python
data = ("Pavan", 22, 85.5, True)

print(data)
```

---

# 4. Single Element Tuple

This is an important concept.

```python
x = (10)

print(type(x))
```

Output:

```text
<class 'int'>
```

Why?

Because `(10)` is simply the number `10` surrounded by parentheses.

To create a single-element tuple, use a comma:

```python
x = (10,)

print(type(x))
```

Output:

```text
<class 'tuple'>
```

### Remember

```python
(10)     # int
(10,)    # tuple
```

The comma creates the tuple.

---

# 5. Tuple Indexing

Tuple indexing works just like list indexing.

```python
subjects = ("Python", "Java", "SQL", "HTML", "CSS")
```

Indexes:

```text
Python → 0
Java   → 1
SQL    → 2
HTML   → 3
CSS    → 4
```

### Access Elements

```python
print(subjects[0])
print(subjects[2])
print(subjects[4])
```

Output:

```text
Python
SQL
CSS
```

---

# 6. Negative Indexing

Negative indexes start from the end.

```text
CSS    → -1
HTML   → -2
SQL    → -3
Java   → -4
Python → -5
```

Example:

```python
subjects = ("Python", "Java", "SQL", "HTML", "CSS")

print(subjects[-1])
print(subjects[-2])
```

Output:

```text
CSS
HTML
```

---

# 7. Tuple Slicing

Slicing is used to extract a portion of a tuple.

Syntax:

```python
tuple[start:stop]
```

Example:

```python
subjects = ("Python", "Java", "SQL", "HTML", "CSS")

print(subjects[0:3])
```

Output:

```text
('Python', 'Java', 'SQL')
```

### Last Three Elements

```python
print(subjects[2:])
```

Output:

```text
('SQL', 'HTML', 'CSS')
```

### Reverse a Tuple

```python
print(subjects[::-1])
```

Output:

```text
('CSS', 'HTML', 'SQL', 'Java', 'Python')
```

---

# 8. Tuple Immutability

**Immutable** means the tuple cannot be changed after it is created.

Example:

```python
subjects = ("Python", "Java", "SQL")

subjects[0] = "C++"
```

This results in:

```text
TypeError
```

We cannot directly modify tuple elements.

The following operations are not supported on tuples:

```python
subjects.append("HTML")
subjects.remove("Java")
subjects[0] = "C++"
```

These are list operations and cannot be directly performed on tuples.

---

# 9. Deleting a Tuple

We cannot delete individual tuple elements.

However, we can delete the entire tuple.

```python
subjects = ("Python", "Java", "SQL")

del subjects
```

After this:

```python
print(subjects)
```

will result in a `NameError` because the tuple variable has been deleted.

---

# 10. Tuple Unpacking

**Tuple unpacking** means assigning tuple values to separate variables.

Example:

```python
student = ("Pavan", 22, "Python")

name, age, course = student

print(name)
print(age)
print(course)
```

Output:

```text
Pavan
22
Python
```

The number of variables should normally match the number of values.

---

# 11. Star Unpacking

Python also supports extended unpacking using `*`.

```python
subjects = ("Python", "Java", "SQL", "HTML", "CSS")

first, second, third, *remaining = subjects

print(first)
print(second)
print(third)
print(remaining)
```

Output:

```text
Python
Java
SQL
['HTML', 'CSS']
```

The `*remaining` variable collects the remaining values into a list.

---

# 12. `count()` Method

The `count()` method returns the number of times a value occurs in a tuple.

Syntax:

```python
tuple.count(value)
```

Example:

```python
subjects = ("Python", "Java", "Python", "SQL", "Python")

print(subjects.count("Python"))
```

Output:

```text
3
```

Another example:

```python
numbers = (10, 20, 10, 30, 10, 40)

print(numbers.count(10))
```

Output:

```text
3
```

---

# 13. `index()` Method

The `index()` method returns the index of the first occurrence of a value.

Syntax:

```python
tuple.index(value)
```

Example:

```python
subjects = ("Python", "Java", "SQL", "HTML")

print(subjects.index("SQL"))
```

Output:

```text
2
```

### With Duplicate Values

```python
subjects = ("Python", "Java", "Python", "SQL")

print(subjects.index("Python"))
```

Output:

```text
0
```

`index()` returns the position of the **first occurrence**.

---

# 14. Looping Through a Tuple

A tuple can be used with a `for` loop.

```python
subjects = ("Python", "Java", "SQL", "HTML", "CSS")

for subject in subjects:
    print(subject)
```

Output:

```text
Python
Java
SQL
HTML
CSS
```

---

# 15. Tuple with `enumerate()`

`enumerate()` gives both the index and value.

```python
subjects = ("Python", "Java", "SQL", "HTML", "CSS")

for index, subject in enumerate(subjects):
    print(index, subject)
```

Output:

```text
0 Python
1 Java
2 SQL
3 HTML
4 CSS
```

---

# 16. Main Day-22 Program

### Store 5 Subjects in a Tuple

```python
subjects = ("Python", "Java", "SQL", "HTML", "CSS")

print("Subjects:", subjects)

# Unpacking
first, second, third, fourth, fifth = subjects

print("First subject:", first)
print("Second subject:", second)
print("Third subject:", third)

# Count
print("Python count:", subjects.count("Python"))

# Index
print("SQL index:", subjects.index("SQL"))
```

---

# 17. Practice Program 1 — Student Details

Create a tuple:

```python
student = ("Pavan", 22, "Python", 85)
```

Unpack the tuple and print all values.

### Solution

```python
student = ("Pavan", 22, "Python", 85)

name, age, course, marks = student

print("Name:", name)
print("Age:", age)
print("Course:", course)
print("Marks:", marks)
```

---

# 18. Practice Program 2 — Number Tuple

Given:

```python
numbers = (10, 20, 30, 20, 40, 20, 50)
```

Find:

1. Count of `20`
2. Index of `40`
3. First element
4. Last element
5. Reverse tuple

### Solution

```python
numbers = (10, 20, 30, 20, 40, 20, 50)

print("Count:", numbers.count(20))
print("Index:", numbers.index(40))
print("First:", numbers[0])
print("Last:", numbers[-1])
print("Reverse:", numbers[::-1])
```

---

# 19. Practice Program 3 — User Input

Take 5 subjects from the user and store them in a tuple.

Input:

```text
Python Java SQL HTML CSS
```

### Solution

```python
subjects = tuple(input("Enter 5 subjects: ").split())

print(subjects)

print("First subject:", subjects[0])
print("Last subject:", subjects[-1])
```

---

# 20. Search for a Subject

```python
subjects = tuple(input("Enter 5 subjects: ").split())

search = input("Enter subject to search: ")

if search in subjects:
    print("Subject found")
    print("Index:", subjects.index(search))
else:
    print("Subject not found")
```

This combines:

- Input
- `split()`
- Tuple
- `in` operator
- `if-else`
- `index()`

---

# 21. Important Tuple Operations

```python
t = (10, 20, 30, 20)
```

### Length

```python
print(len(t))
```

### Membership

```python
print(20 in t)
```

### Indexing

```python
print(t[0])
```

### Slicing

```python
print(t[1:3])
```

### Count

```python
print(t.count(20))
```

### Index

```python
print(t.index(30))
```

---

# 🧠 Important Points to Remember

1. Tuple is ordered.
2. Tuple is indexed.
3. Tuple is immutable.
4. Tuple allows duplicate values.
5. Tuple can contain different data types.
6. Parentheses `()` are normally used for tuples.
7. A single-element tuple requires a comma.
8. `count()` counts occurrences.
9. `index()` returns the first matching index.
10. Tuple unpacking assigns values to variables.

---

# 📝 Quick Quiz

### Q1. Which brackets are normally used for a tuple?

A. `{}`  
B. `[]`  
C. `()`  
D. `<>`

**Answer: C**

### Q2. Which is a single-element tuple?

```python
A. x = (10)
B. x = (10,)
C. x = [10]
```

**Answer: B**

### Q3. Are tuples mutable?

A. Yes  
B. No

**Answer: B**

### Q4. What is the output?

```python
x = (10, 20, 30)

print(x[1])
```

**Answer:**

```text
20
```

### Q5. What does `count()` do?

**Answer:** It counts how many times a specified value occurs.

### Q6. What does `index()` return?

**Answer:** The index of the first occurrence of a specified value.

### Q7. What is the output?

```python
x = ("A", "B", "C")

a, b, c = x

print(b)
```

**Answer:**

```text
B
```

---

# 🏠 Homework

## 1. Student Tuple

Create:

```python
student = ("Rahul", 21, "Python", 90)
```

Unpack and print all values.

## 2. Number Tuple

Create a tuple containing 10 numbers and find:

- Maximum
- Minimum
- Length
- Sum

## 3. Search

Create a tuple containing 5 programming languages.

Ask the user for a language and check whether it exists.

## 4. Count

Given:

```python
numbers = (1, 2, 3, 2, 4, 2, 5, 2)
```

Find the number of occurrences of `2`.

## 5. ⭐ Challenge

Take 5 student names from the user and store them in a tuple.

Then:

- Print all students
- Print the first student
- Print the last student
- Ask for a student name
- Find its index if present

---

# 🔑 Day-22 Cheat Sheet

```python
# Create
t = (10, 20, 30)

# Access
print(t[0])

# Negative indexing
print(t[-1])

# Slicing
print(t[1:])

# Reverse
print(t[::-1])

# Count
print(t.count(20))

# Index
print(t.index(30))

# Unpacking
a, b, c = t

# Loop
for value in t:
    print(value)

# Membership
print(20 in t)
```

## ⭐ Remember

```text
LIST  → Mutable
TUPLE → Immutable
```

**Day 22 complete! 🐍**
