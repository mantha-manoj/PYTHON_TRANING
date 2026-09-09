# 🐍 Python 45 Days Challenge — Day 23

## 📌 Topic: Sets and Set Operations

### 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Understand what a Set is in Python
- Create Sets
- Add and remove elements
- Understand unique values in Sets
- Perform Union
- Perform Intersection
- Perform Difference
- Perform Symmetric Difference
- Use Set operators such as `|`, `&`, `-`, and `^`
- Solve practical problems using Sets

---

# 1. What is a Set?

A **Set** is a collection of **unique and unordered elements** in Python.

```python
skills = {"Python", "Java", "SQL", "Python"}

print(skills)
```

Output will contain `Python` only once because Sets do not allow duplicate values.

### Important Properties of Sets

- Sets contain **unique elements**
- Sets are **unordered**
- Sets are **mutable**
- Sets do not support indexing
- Sets can contain different data types
- Sets are useful for mathematical set operations

---

# 2. Creating a Set

## Using Curly Braces

```python
skills = {"Python", "Java", "SQL"}

print(skills)
```

## Using `set()`

```python
skills = set(["Python", "Java", "SQL"])

print(skills)
```

## Creating an Empty Set

Be careful:

```python
x = {}
```

This creates an **empty dictionary**, not a Set.

Correct way:

```python
x = set()
```

---

# 3. Duplicate Values

Sets automatically remove duplicate values.

```python
skills = {"Python", "Java", "Python", "SQL", "Java"}

print(skills)
```

Possible output:

```text
{'Python', 'Java', 'SQL'}
```

---

# 4. Adding Elements

## `add()`

Adds one element to a Set.

```python
skills = {"Python", "Java"}

skills.add("SQL")

print(skills)
```

## `update()`

Adds multiple elements.

```python
skills = {"Python", "Java"}

skills.update(["SQL", "HTML", "CSS"])

print(skills)
```

---

# 5. Removing Elements

## `remove()`

```python
skills = {"Python", "Java", "SQL"}

skills.remove("Java")

print(skills)
```

If the element does not exist, `remove()` raises an error.

## `discard()`

```python
skills = {"Python", "Java", "SQL"}

skills.discard("Java")

print(skills)
```

If the element does not exist, `discard()` does not raise an error.

## `pop()`

```python
skills = {"Python", "Java", "SQL"}

skills.pop()

print(skills)
```

`pop()` removes an arbitrary element because Sets are unordered.

## `clear()`

Removes all elements.

```python
skills = {"Python", "Java", "SQL"}

skills.clear()

print(skills)
```

---

# 6. Set Operations

Consider two Sets:

```python
student1 = {"Python", "Java", "SQL"}
student2 = {"Python", "SQL", "HTML"}
```

We can perform four important operations:

1. Union
2. Intersection
3. Difference
4. Symmetric Difference

---

# 7. Union

## Meaning

**Union returns all unique elements from both Sets.**

### Using `union()`

```python
student1 = {"Python", "Java", "SQL"}
student2 = {"Python", "SQL", "HTML"}

print(student1.union(student2))
```

Output:

```text
{'Python', 'Java', 'SQL', 'HTML'}
```

### Using `|` Operator

```python
print(student1 | student2)
```

### Easy Memory Trick

> **UNION = ALL unique elements**

---

# 8. Intersection

## Meaning

**Intersection returns elements that are common to both Sets.**

### Using `intersection()`

```python
student1 = {"Python", "Java", "SQL"}
student2 = {"Python", "SQL", "HTML"}

print(student1.intersection(student2))
```

Output:

```text
{'Python', 'SQL'}
```

### Using `&` Operator

```python
print(student1 & student2)
```

### Easy Memory Trick

> **INTERSECTION = COMMON elements**

---

# 9. Difference

## Meaning

Difference returns elements that are present in the **first Set but not in the second Set**.

```python
student1 = {"Python", "Java", "SQL"}
student2 = {"Python", "SQL", "HTML"}

print(student1.difference(student2))
```

Output:

```text
{'Java'}
```

### Using `-` Operator

```python
print(student1 - student2)
```

### Reverse Difference

```python
print(student2 - student1)
```

Output:

```text
{'HTML'}
```

### Important

`A - B` and `B - A` are different.

> **Difference depends on the order of the Sets.**

---

# 10. Symmetric Difference

## Meaning

Symmetric Difference returns elements that are in **either Set but not in both**.

```python
student1 = {"Python", "Java", "SQL"}
student2 = {"Python", "SQL", "HTML"}

print(student1.symmetric_difference(student2))
```

Output:

```text
{'Java', 'HTML'}
```

### Using `^` Operator

```python
print(student1 ^ student2)
```

### Easy Memory Trick

> **SYMMETRIC DIFFERENCE = Elements unique to either Set**

---

# 11. Set Operations Cheat Sheet

| Operation | Method | Operator | Meaning |
|---|---|---|---|
| Union | `union()` | `\|` | All unique elements |
| Intersection | `intersection()` | `&` | Common elements |
| Difference | `difference()` | `-` | Elements in first Set only |
| Symmetric Difference | `symmetric_difference()` | `^` | Elements unique to either Set |

### Quick Memory Trick

```text
U → Union → All
I → Intersection → Common
D → Difference → First only
S → Symmetric Difference → Unique to either
```

---

# 12. Main Program — Student Skills

## Problem Statement

Create two Sets containing student skills and display:

- Union
- Intersection
- Difference
- Symmetric Difference

## Solution

```python
student1 = {"Python", "Java", "SQL"}
student2 = {"Python", "SQL", "HTML"}

print("Student 1:", student1)
print("Student 2:", student2)

print("Union:", student1.union(student2))

print("Intersection:", student1.intersection(student2))

print("Difference:", student1.difference(student2))

print("Symmetric Difference:",
      student1.symmetric_difference(student2))
```

---

# 13. Using Set Operators

The same program can be written using operators:

```python
student1 = {"Python", "Java", "SQL"}
student2 = {"Python", "SQL", "HTML"}

print("Union:", student1 | student2)

print("Intersection:", student1 & student2)

print("Difference:", student1 - student2)

print("Symmetric Difference:", student1 ^ student2)
```

---

# 14. Practical Example — Frontend and Backend Skills

```python
frontend = {"HTML", "CSS", "JavaScript", "React"}
backend = {"Java", "Python", "SQL", "React"}

print("All Technologies:", frontend | backend)

print("Common Technologies:", frontend & backend)

print("Frontend Only:", frontend - backend)

print("Unique Technologies:", frontend ^ backend)
```

### What this demonstrates

- `frontend | backend` → All technologies
- `frontend & backend` → Common technologies
- `frontend - backend` → Frontend-only technologies
- `frontend ^ backend` → Technologies unique to either group

---

# 15. Taking Set Input from User

We can use `split()` with `set()` to create a Set from user input.

```python
student1 = set(input("Enter skills for Student 1: ").split())
student2 = set(input("Enter skills for Student 2: ").split())

print("Union:", student1 | student2)
print("Intersection:", student1 & student2)
print("Difference:", student1 - student2)
print("Symmetric Difference:", student1 ^ student2)
```

### Example Input

```text
Enter skills for Student 1: Python Java SQL
Enter skills for Student 2: Python SQL HTML
```

### Result

```text
Union: {'Python', 'Java', 'SQL', 'HTML'}
Intersection: {'Python', 'SQL'}
Difference: {'Java'}
Symmetric Difference: {'Java', 'HTML'}
```

---

# 16. Important Set Methods

| Method | Purpose |
|---|---|
| `add()` | Add one element |
| `update()` | Add multiple elements |
| `remove()` | Remove an element; error if absent |
| `discard()` | Remove an element; no error if absent |
| `pop()` | Remove an arbitrary element |
| `clear()` | Remove all elements |
| `union()` | Combine Sets |
| `intersection()` | Find common elements |
| `difference()` | Find elements only in first Set |
| `symmetric_difference()` | Find elements unique to either Set |

---

# 17. Common Mistakes

## Mistake 1 — Thinking `{}` creates an empty Set

```python
x = {}
```

This creates a dictionary.

Correct:

```python
x = set()
```

## Mistake 2 — Trying to access Set elements using indexes

```python
skills = {"Python", "Java", "SQL"}

print(skills[0])
```

This causes an error because Sets are unordered and do not support indexing.

## Mistake 3 — Confusing `remove()` and `discard()`

```python
skills.remove("C++")
```

Can raise an error if `"C++"` is absent.

```python
skills.discard("C++")
```

Does not raise an error if `"C++"` is absent.

## Mistake 4 — Forgetting that Difference is directional

```python
A - B
```

is different from:

```python
B - A
```

---

# 18. Practice Questions

## Practice 1

Given:

```python
a = {"Python", "Java", "C++"}
b = {"Python", "SQL", "Java"}
```

Find:

1. Union
2. Intersection
3. `a - b`
4. `b - a`
5. Symmetric Difference

---

## Practice 2

Create:

```python
frontend = {"HTML", "CSS", "JavaScript", "React"}
backend = {"Java", "Python", "SQL", "React"}
```

Find:

1. All technologies
2. Technologies common to both
3. Frontend-only technologies
4. Backend-only technologies
5. Technologies unique to either group

---

## Practice 3

Write a Python program that:

1. Takes two Sets from the user
2. Finds their Union
3. Finds their Intersection
4. Finds their Difference
5. Finds their Symmetric Difference

---

# 19. Quick Revision

### What is a Set?

A collection of unique and unordered elements.

### Which function creates an empty Set?

```python
set()
```

### Which method adds one element?

```python
add()
```

### Which method adds multiple elements?

```python
update()
```

### Which operation finds all unique elements?

```python
union()
```

or

```python
A | B
```

### Which operation finds common elements?

```python
intersection()
```

or

```python
A & B
```

### Which operation finds elements only in A?

```python
A - B
```

### Which operation finds elements unique to either Set?

```python
A ^ B
```

---

# 🧠 Day 23 Final Cheat Sheet

```python
# Create Sets
a = {"Python", "Java", "SQL"}
b = {"Python", "SQL", "HTML"}

# Add
a.add("C++")

# Add multiple
a.update(["React", "CSS"])

# Remove
a.remove("Java")

# Safe remove
a.discard("Java")

# Union
a | b
a.union(b)

# Intersection
a & b
a.intersection(b)

# Difference
a - b
a.difference(b)

# Symmetric Difference
a ^ b
a.symmetric_difference(b)
```

---

## 🎯 Key Takeaway

Remember these four operators:

```text
A | B  → UNION                  → ALL
A & B  → INTERSECTION           → COMMON
A - B  → DIFFERENCE             → A ONLY
A ^ B  → SYMMETRIC DIFFERENCE   → UNIQUE TO EITHER
```

---

**Day 23 completed ✅**

Next: Continue with **Day 24** according to the 45-Day Python schedule.
