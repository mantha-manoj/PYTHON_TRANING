# 🐍 Python 45 Days – Day 29

## 📚 Topic: Lambda & Built-in Functions

**Duration:** 1 Hour 30 Minutes

---

## 🎯 Learning Objectives

By the end of this class, students will be able to:

- Understand Lambda functions
- Create anonymous functions
- Use `map()`
- Use `filter()`
- Use `sorted()`
- Use `max()` and `min()`
- Combine Lambda with built-in functions

---

## 1. Lambda Function

A **lambda function** is a small anonymous function used for simple operations.

### Syntax

```python
lambda arguments: expression
```

### Example

```python
square = lambda x: x * x

print(square(5))
```

### Output

```text
25
```

---

## 2. Normal Function vs Lambda

### Normal Function

```python
def add(a, b):
    return a + b

print(add(10, 20))
```

### Lambda Function

```python
add = lambda a, b: a + b

print(add(10, 20))
```

Both produce:

```text
30
```

---

## 3. Lambda Examples

### Cube

```python
cube = lambda x: x ** 3

print(cube(4))
```

### Check Even Number

```python
even = lambda x: x % 2 == 0

print(even(10))
```

### Find Maximum

```python
maximum = lambda a, b: a if a > b else b

print(maximum(10, 20))
```

> Lambda functions are mainly useful for short and simple operations.

---

# 4. `map()`

`map()` applies a function to every element in an iterable.

### Syntax

```python
map(function, iterable)
```

### Example

```python
numbers = [1, 2, 3, 4, 5]

result = map(lambda x: x * x, numbers)

print(list(result))
```

### Output

```text
[1, 4, 9, 16, 25]
```

### Example – Double Numbers

```python
numbers = [10, 20, 30, 40]

result = map(lambda x: x * 2, numbers)

print(list(result))
```

Output:

```text
[20, 40, 60, 80]
```

---

# 5. `filter()`

`filter()` selects elements that satisfy a condition.

### Syntax

```python
filter(function, iterable)
```

### Example – Even Numbers

```python
numbers = [1, 2, 3, 4, 5, 6]

result = filter(lambda x: x % 2 == 0, numbers)

print(list(result))
```

Output:

```text
[2, 4, 6]
```

### Example – Passed Marks

```python
marks = [35, 78, 42, 90, 25, 65]

passed = filter(lambda x: x >= 40, marks)

print(list(passed))
```

Output:

```text
[78, 42, 90, 65]
```

---

# 6. `sorted()`

`sorted()` returns the elements in sorted order.

### Ascending

```python
numbers = [50, 10, 40, 20, 30]

print(sorted(numbers))
```

Output:

```text
[10, 20, 30, 40, 50]
```

### Descending

```python
print(sorted(numbers, reverse=True))
```

Output:

```text
[50, 40, 30, 20, 10]
```

### Sorting Using Lambda

```python
students = [
    ("Pavan", 85),
    ("Rahul", 72),
    ("Arun", 92)
]

result = sorted(students, key=lambda x: x[1])

print(result)
```

---

# 7. `max()` and `min()`

### Example

```python
numbers = [10, 50, 20, 80, 30]

print("Maximum:", max(numbers))
print("Minimum:", min(numbers))
```

Output:

```text
Maximum: 80
Minimum: 10
```

### Student Marks

```python
marks = [78, 92, 65, 88, 95]

print("Highest:", max(marks))
print("Lowest:", min(marks))
```

---

# 🧑‍💻 Day 29 Practical Program

## Student Marks Analyzer

```python
marks = [45, 78, 32, 90, 67, 25, 88]

# Add 5 grace marks
updated = list(map(lambda x: x + 5, marks))

# Find passed marks
passed = list(filter(lambda x: x >= 40, updated))

# Sort marks
sorted_marks = sorted(updated, reverse=True)

print("Original Marks:", marks)
print("Updated Marks:", updated)
print("Passed Marks:", passed)
print("Highest:", max(updated))
print("Lowest:", min(updated))
print("Sorted Marks:", sorted_marks)
```

---

# 📝 Practice Questions

1. Square every number using `map()`.
2. Find even numbers using `filter()`.
3. Find odd numbers using `filter()`.
4. Find numbers greater than 50.
5. Sort a list in ascending order.
6. Sort a list in descending order.
7. Find maximum and minimum values.
8. Sort students according to marks using Lambda.
9. Add 10 to every number using `map()`.
10. Find students who scored 40 or above using `filter()`.

---

# 🏠 Homework

Create a **Number Analyzer** program that:

- Accepts a list of numbers
- Doubles every number
- Finds even numbers
- Finds numbers greater than 50
- Sorts the numbers
- Displays maximum and minimum

---

# 📌 Quick Revision

| Concept | Purpose |
|---|---|
| Lambda | Small anonymous function |
| `map()` | Transform every element |
| `filter()` | Select elements based on condition |
| `sorted()` | Sort values |
| `max()` | Find largest value |
| `min()` | Find smallest value |

---

## ✅ Topics Completed

- Lambda Functions
- `map()`
- `filter()`
- `sorted()`
- `max()`
- `min()`
- Lambda with built-in functions
