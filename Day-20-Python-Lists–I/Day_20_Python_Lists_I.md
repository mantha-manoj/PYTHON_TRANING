# 🐍 Python 45 Days – Day 20
## Lists – I

**Duration:** 1 Hour 30 Minutes  
**Topic:** Python Lists – Creating, Accessing, Adding, Updating, Removing, and Basic List Functions

---

## 📌 Learning Objectives

By the end of this session, you will be able to:

- Understand what a Python list is
- Create lists using `[]`
- Access list elements using indexes
- Use positive and negative indexing
- Add elements using `append()` and `insert()`
- Update list elements
- Remove elements using `remove()` and `pop()`
- Use `len()`, `min()`, `max()`, and `sum()`
- Calculate the average of list values

---

## 1. What is a List?

A **list** is used to store multiple values in a single variable.

Instead of:

```python
mark1 = 80
mark2 = 75
mark3 = 90
mark4 = 85
```

We can use:

```python
marks = [80, 75, 90, 85]
```

### Important Properties of Lists

- Lists use square brackets: `[]`
- Lists can store multiple values
- Lists are ordered
- Lists are changeable (mutable)
- Lists allow duplicate values
- Lists can contain different data types

Example:

```python
student = ["Pavan", 21, 85.5, True]

print(student)
```

Output:

```text
['Pavan', 21, 85.5, True]
```

---

## 2. Accessing List Elements

Every element in a list has an **index**.

Indexes start from `0`.

```python
marks = [80, 75, 90, 85]
```

| Index | Value |
|------:|------:|
| 0 | 80 |
| 1 | 75 |
| 2 | 90 |
| 3 | 85 |

Example:

```python
print(marks[0])
print(marks[2])
```

Output:

```text
80
90
```

### Negative Indexing

Python also supports negative indexes.

```python
print(marks[-1])
print(marks[-2])
```

Output:

```text
85
90
```

- `-1` → last element
- `-2` → second-last element

---

## 3. Adding Elements

### `append()`

`append()` adds an element to the **end** of the list.

```python
marks = [80, 75, 90]

marks.append(85)

print(marks)
```

Output:

```text
[80, 75, 90, 85]
```

### `insert()`

`insert()` adds an element at a specific index.

Syntax:

```python
list.insert(index, value)
```

Example:

```python
marks = [80, 75, 90]

marks.insert(1, 88)

print(marks)
```

Output:

```text
[80, 88, 75, 90]
```

---

## 4. Updating List Elements

Lists are **mutable**, so their values can be changed.

Example:

```python
marks = [80, 75, 90]

marks[1] = 85

print(marks)
```

Output:

```text
[80, 85, 90]
```

Syntax:

```python
list[index] = new_value
```

---

## 5. Removing Elements

### `remove()`

`remove()` removes a specific value.

```python
marks = [80, 75, 90, 75]

marks.remove(75)

print(marks)
```

Output:

```text
[80, 90, 75]
```

> `remove()` removes the **first matching value**.

### `pop()`

`pop()` removes an element using its index.

```python
marks = [80, 75, 90]

marks.pop(1)

print(marks)
```

Output:

```text
[80, 90]
```

If no index is given, `pop()` removes the last element:

```python
marks.pop()
```

---

## 6. Useful List Functions

Consider:

```python
marks = [80, 75, 90, 85, 70]
```

### `len()`

Returns the number of elements.

```python
print(len(marks))
```

Output:

```text
5
```

### `min()`

Returns the smallest value.

```python
print(min(marks))
```

Output:

```text
70
```

### `max()`

Returns the largest value.

```python
print(max(marks))
```

Output:

```text
90
```

### `sum()`

Returns the total of numeric values.

```python
print(sum(marks))
```

Output:

```text
400
```

### Calculating Average

```python
average = sum(marks) / len(marks)

print(average)
```

Output:

```text
80.0
```

---

# 💻 7. Complete Example – Student Marks

```python
marks = [80, 75, 90, 85, 70]

print("Original Marks:", marks)

# Add a mark
marks.append(95)
print("After append:", marks)

# Insert a mark
marks.insert(2, 88)
print("After insert:", marks)

# Update a mark
marks[1] = 82
print("After update:", marks)

# Remove a mark
marks.remove(70)
print("After remove:", marks)

# Calculate results
print("Minimum:", min(marks))
print("Maximum:", max(marks))
print("Total:", sum(marks))
print("Number of subjects:", len(marks))

average = sum(marks) / len(marks)
print("Average:", average)
```

---

# 🧪 8. Student Practice

## Problem

Create a list containing marks of **5 subjects**.

Example:

```python
marks = [78, 85, 92, 67, 88]
```

Perform the following operations:

1. Print the original list.
2. Add one new mark using `append()`.
3. Insert a mark at index `2`.
4. Update the mark at index `1`.
5. Remove one mark.
6. Print the highest mark.
7. Print the lowest mark.
8. Print total marks.
9. Print the number of subjects.
10. Calculate the average.

### Concepts to Use

```python
append()
insert()
remove()
list[index] = value
min()
max()
sum()
len()
```

---

# 📝 9. Quick Revision

| Operation | Syntax | Purpose |
|---|---|---|
| Create | `marks = [80, 90]` | Create a list |
| Access | `marks[0]` | Get an element |
| Append | `marks.append(95)` | Add at the end |
| Insert | `marks.insert(1, 85)` | Add at a position |
| Update | `marks[0] = 100` | Change a value |
| Remove | `marks.remove(90)` | Remove a value |
| Pop | `marks.pop(1)` | Remove using index |
| Length | `len(marks)` | Count elements |
| Minimum | `min(marks)` | Smallest value |
| Maximum | `max(marks)` | Largest value |
| Sum | `sum(marks)` | Total |

---

# 🎯 Key Takeaways

- A list stores multiple values in one variable.
- List indexing starts from `0`.
- Lists are mutable, so their elements can be changed.
- `append()` adds an element at the end.
- `insert()` adds an element at a particular position.
- `remove()` removes a value.
- `pop()` removes an element using its index.
- `len()` gives the number of elements.
- `min()` gives the smallest value.
- `max()` gives the largest value.
- `sum()` gives the total of numeric values.
- Average can be calculated using:

```python
sum(list) / len(list)
```

---

## ⭐ Day 20 One-Line Summary

> **Python List = An ordered and changeable collection used to store multiple values.**
