# 🐍 Python 45 Days — Day 21

## Lists – II: Removing Duplicates & Filtering

**Duration:** 1 hour 30 minutes

---

## 🎯 Learning Objectives

By the end of this session, you should be able to:

- Identify duplicate values in a list.
- Remove duplicates using `set()`.
- Remove duplicates while preserving the original order.
- Use `for` loops with lists.
- Use `if` conditions to filter values.
- Extract even numbers from a list.
- Extract odd numbers from a list.
- Combine duplicate removal and filtering in a program.

---

## 1. 🔄 Quick List Revision

A Python list is an ordered, mutable collection.

```python
marks = [80, 75, 90, 60, 85]
```

### Add an item

```python
marks.append(95)
```

### Insert an item

```python
marks.insert(2, 88)
```

### Remove an item

```python
marks.remove(60)
```

### Find the largest value

```python
max(marks)
```

### Find the smallest value

```python
min(marks)
```

### Find the total

```python
sum(marks)
```

### Find the number of elements

```python
len(marks)
```

---

# 2. 🔁 What Are Duplicates?

A duplicate is a value that appears more than once in a collection.

```python
numbers = [10, 20, 10, 30, 20, 40, 10]

print(numbers)
```

Output:

```text
[10, 20, 10, 30, 20, 40, 10]
```

Here:

- `10` appears 3 times.
- `20` appears 2 times.
- `30` appears once.
- `40` appears once.

We want:

```text
[10, 20, 30, 40]
```

---

# 3. 🧹 Removing Duplicates Using `set()`

A `set` stores unique values.

```python
numbers = [10, 20, 10, 30, 20, 40, 10]

unique_numbers = set(numbers)

print(unique_numbers)
```

Example output:

```text
{10, 20, 30, 40}
```

If we need the result as a list:

```python
unique_numbers = list(set(numbers))

print(unique_numbers)
```

Output:

```text
[10, 20, 30, 40]
```

### ⚠️ Important

A set is **unordered**. Therefore, don't rely on `set()` when the original order must be preserved.

---

# 4. ⭐ Removing Duplicates While Preserving Order

We can use a loop and an empty list.

```python
numbers = [10, 20, 10, 30, 20, 40, 10]

unique_numbers = []

for number in numbers:
    if number not in unique_numbers:
        unique_numbers.append(number)

print(unique_numbers)
```

Output:

```text
[10, 20, 30, 40]
```

### How it works

Initially:

```python
unique_numbers = []
```

The loop checks each number.

| Number | Already present? | Action |
|---|---|---|
| 10 | No | Add |
| 20 | No | Add |
| 10 | Yes | Skip |
| 30 | No | Add |
| 20 | Yes | Skip |
| 40 | No | Add |
| 10 | Yes | Skip |

Final result:

```text
[10, 20, 30, 40]
```

### ⭐ Remember this pattern

```python
new_list = []

for item in old_list:
    if item not in new_list:
        new_list.append(item)
```

This removes duplicates while preserving the order of first occurrence.

---

# 5. 🔢 Filtering Even Numbers

An even number is divisible by 2.

We use the modulus operator `%`.

```python
number % 2 == 0
```

Example:

```python
10 % 2 == 0
```

Therefore, `10` is even.

### Example

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

even_numbers = []

for number in numbers:
    if number % 2 == 0:
        even_numbers.append(number)

print(even_numbers)
```

Output:

```text
[2, 4, 6, 8, 10]
```

---

# 6. 🔢 Filtering Odd Numbers

An odd number is not divisible by 2.

We can check:

```python
number % 2 != 0
```

Example:

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

odd_numbers = []

for number in numbers:
    if number % 2 != 0:
        odd_numbers.append(number)

print(odd_numbers)
```

Output:

```text
[1, 3, 5, 7, 9]
```

---

# 7. 🔥 Combining Duplicate Removal + Even Filtering

Consider:

```python
numbers = [10, 15, 20, 10, 25, 30, 20, 40, 35, 40]
```

First remove duplicates:

```text
[10, 15, 20, 25, 30, 40, 35]
```

Then find even numbers:

```text
[10, 20, 30, 40]
```

### Complete Program

```python
numbers = [10, 15, 20, 10, 25, 30, 20, 40, 35, 40]

# Remove duplicates
unique_numbers = []

for number in numbers:
    if number not in unique_numbers:
        unique_numbers.append(number)

# Get even numbers
even_numbers = []

for number in unique_numbers:
    if number % 2 == 0:
        even_numbers.append(number)

print("Original List:", numbers)
print("Unique List:", unique_numbers)
print("Even Numbers:", even_numbers)
```

Output:

```text
Original List: [10, 15, 20, 10, 25, 30, 20, 40, 35, 40]
Unique List: [10, 15, 20, 25, 30, 40, 35]
Even Numbers: [10, 20, 30, 40]
```

---

# 8. 🧩 User Input

We can allow the user to enter numbers.

```python
numbers = list(map(int, input("Enter numbers separated by space: ").split()))

print(numbers)
```

Example input:

```text
10 20 10 30 20 40
```

Output:

```text
[10, 20, 10, 30, 20, 40]
```

### Understanding the code

```python
input()
```

Takes input as a string.

```python
.split()
```

Splits the string into separate values.

```python
map(int, ...)
```

Converts each value to an integer.

```python
list(...)
```

Creates a list.

---

# 9. 💻 Complete User-Input Program

```python
numbers = list(map(int, input("Enter numbers separated by space: ").split()))

# Remove duplicates
unique_numbers = []

for number in numbers:
    if number not in unique_numbers:
        unique_numbers.append(number)

# Find even numbers
even_numbers = []

for number in unique_numbers:
    if number % 2 == 0:
        even_numbers.append(number)

# Find odd numbers
odd_numbers = []

for number in unique_numbers:
    if number % 2 != 0:
        odd_numbers.append(number)

print("Original List:", numbers)
print("Unique List:", unique_numbers)
print("Even Numbers:", even_numbers)
print("Odd Numbers:", odd_numbers)
print("Total Unique Numbers:", len(unique_numbers))
```

---

# 10. 🧪 Practice Exercises

## Exercise 1 — Easy

Given:

```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5, 6]
```

Remove duplicates.

Expected:

```text
[1, 2, 3, 4, 5, 6]
```

---

## Exercise 2 — Medium

Given:

```python
numbers = [11, 20, 33, 40, 55, 60, 20, 40]
```

Remove duplicates and find the even numbers.

Expected:

```text
Unique List: [11, 20, 33, 40, 55, 60]
Even Numbers: [20, 40, 60]
```

---

## Exercise 3 — Challenge ⭐

Take numbers from the user.

Your program should:

1. Read the numbers.
2. Remove duplicates.
3. Find even numbers.
4. Find odd numbers.
5. Count unique numbers.
6. Display all results.

Example:

```text
Enter numbers separated by space: 10 15 10 20 25 30 20
```

Expected:

```text
Original List: [10, 15, 10, 20, 25, 30, 20]
Unique List: [10, 15, 20, 25, 30]
Even Numbers: [10, 20, 30]
Odd Numbers: [15, 25]
Total Unique Numbers: 5
```

---

# 🧠 Quick Revision / Cheat Sheet

| Concept | Syntax |
|---|---|
| Create list | `numbers = [1, 2, 3]` |
| Add item | `numbers.append(4)` |
| Insert item | `numbers.insert(1, 5)` |
| Remove item | `numbers.remove(2)` |
| Check membership | `x in numbers` |
| Check non-membership | `x not in numbers` |
| Remove duplicates | `list(set(numbers))` |
| Preserve order | `if x not in new_list:` |
| Even | `x % 2 == 0` |
| Odd | `x % 2 != 0` |
| Add to list | `new_list.append(x)` |
| List length | `len(numbers)` |
| Total | `sum(numbers)` |
| Largest | `max(numbers)` |
| Smallest | `min(numbers)` |

---

# 🎯 Key Takeaways

### 1. `set()` removes duplicates

```python
unique = list(set(numbers))
```

### 2. Loop method preserves order

```python
unique = []

for x in numbers:
    if x not in unique:
        unique.append(x)
```

### 3. Even number

```python
x % 2 == 0
```

### 4. Odd number

```python
x % 2 != 0
```

### 5. Filtering with a loop

```python
result = []

for x in numbers:
    if condition:
        result.append(x)
```

---

## 📚 Day 21 Summary

Today we learned:

- Duplicate values
- `set()`
- Removing duplicates with a loop
- Preserving list order
- `for` loops with lists
- `if` conditions
- Even number filtering
- Odd number filtering
- User input with `map()`
- Combining multiple list operations

> **One-line takeaway:**  
> **Use loops and conditions to clean, filter, and transform lists.**

---

## 🚀 Next

**Day 22 — Lists – III**

Continue practicing more advanced list operations and problem-solving.
