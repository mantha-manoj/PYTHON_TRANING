# Day 24 — Python Dictionaries – I

> **Class Duration:** 1 Hour 30 Minutes  
> **Topic:** Dictionaries – Creating, Accessing, Adding, Updating and Deleting Data

---

## 🎯 Learning Objectives

By the end of this class, you should understand:

- What a dictionary is
- Dictionary syntax
- Key-value pairs
- Creating dictionaries
- Accessing dictionary values
- Adding new key-value pairs
- Updating existing values
- Removing items
- Common dictionary methods
- Basic dictionary programs

---

## 1. What is a Dictionary?

A **dictionary** is a Python data structure that stores data in **key-value pairs**.

### Real-world example

A student may have:

```text
Name     → Pavan
Roll No  → 101
Course   → Python
Marks    → 85
```

In Python:

```python
student = {
    "name": "Pavan",
    "roll_no": 101,
    "course": "Python",
    "marks": 85
}
```

### Simple Definition

> A dictionary is a collection of **key-value pairs**.

---

## 2. Dictionary Syntax

```python
dictionary_name = {
    "key1": value1,
    "key2": value2,
    "key3": value3
}
```

Example:

```python
student = {
    "name": "Rahul",
    "age": 21,
    "marks": 85
}
```

Here:

```text
"name"  → key
"Rahul" → value

"age"   → key
21      → value

"marks" → key
85      → value
```

---

## 3. Dictionary Can Store Different Data Types

A dictionary can store different types of values:

```python
student = {
    "name": "Rahul",
    "age": 21,
    "marks": 85.5,
    "passed": True
}
```

Values can also be lists, tuples, or other dictionaries:

```python
student = {
    "name": "Rahul",
    "marks": [80, 85, 90]
}
```

---

## 4. Accessing Dictionary Values

Dictionary values are normally accessed using their **keys**.

```python
student = {
    "name": "Rahul",
    "age": 21,
    "marks": 85
}

print(student["name"])
print(student["age"])
print(student["marks"])
```

### Output

```text
Rahul
21
85
```

### Important

With a dictionary, use the **key** to access the value.

❌ Wrong:

```python
print(student[0])
```

✅ Correct:

```python
print(student["name"])
```

---

## 5. `get()` Method

Another way to access a value is using `get()`.

```python
print(student.get("name"))
```

Output:

```text
Rahul
```

### `[]` vs `get()`

If the key does not exist:

```python
student["city"]
```

Python raises:

```text
KeyError
```

But:

```python
student.get("city")
```

returns:

```text
None
```

You can also provide a default value:

```python
print(student.get("city", "Not Available"))
```

Output:

```text
Not Available
```

---

## 6. Adding a New Item

If the key does not already exist, assignment adds a new key-value pair.

```python
student = {
    "name": "Rahul",
    "age": 21,
    "marks": 85
}

student["course"] = "Python"

print(student)
```

Output:

```text
{'name': 'Rahul', 'age': 21, 'marks': 85, 'course': 'Python'}
```

---

## 7. Updating a Value

If the key already exists, assignment updates its value.

```python
student = {
    "name": "Rahul",
    "marks": 85
}

student["marks"] = 95

print(student)
```

Output:

```text
{'name': 'Rahul', 'marks': 95}
```

### ⭐ Important Rule

```python
dictionary[key] = value
```

- Existing key → **Update**
- New key → **Add**

This is an important MCQ concept.

---

## 8. Deleting Items

### Using `del`

```python
student = {
    "name": "Rahul",
    "age": 21,
    "marks": 85
}

del student["age"]

print(student)
```

Output:

```text
{'name': 'Rahul', 'marks': 85}
```

---

## 9. `pop()` Method

`pop()` removes a specified key and returns its value.

```python
student = {
    "name": "Rahul",
    "age": 21,
    "marks": 85
}

removed = student.pop("age")

print(removed)
print(student)
```

Output:

```text
21
{'name': 'Rahul', 'marks': 85}
```

### Difference

```python
del student["age"]
```

removes the item.

```python
student.pop("age")
```

removes the item **and can return the removed value**.

---

## 10. `keys()` Method

`keys()` returns the dictionary's keys.

```python
student = {
    "name": "Rahul",
    "age": 21,
    "marks": 85
}

print(student.keys())
```

You can also iterate through the keys:

```python
for key in student.keys():
    print(key)
```

Output:

```text
name
age
marks
```

---

## 11. `values()` Method

`values()` returns the dictionary's values.

```python
for value in student.values():
    print(value)
```

Output:

```text
Rahul
21
85
```

---

## 12. `items()` Method

`items()` returns **key-value pairs**.

```python
for key, value in student.items():
    print(key, value)
```

Output:

```text
name Rahul
age 21
marks 85
```

### ⭐ Remember

```text
keys()    → Keys
values()  → Values
items()   → Keys + Values
```

---

## 13. `len()` with Dictionary

`len()` returns the number of key-value pairs.

```python
student = {
    "name": "Rahul",
    "age": 21,
    "marks": 85
}

print(len(student))
```

Output:

```text
3
```

There are 3 key-value pairs.

---

# 👨‍💻 Practical Program 1 — Student Dictionary

```python
student = {
    "name": "Pavan",
    "roll_no": 101,
    "course": "Python",
    "marks": 85
}

print(student)
```

### Add a new key

```python
student["city"] = "Bangalore"
```

### Update marks

```python
student["marks"] = 92
```

### Delete course

```python
del student["course"]
```

### Print final dictionary

```python
print(student)
```

---

# 👨‍💻 Practical Program 2 — Dictionary Using User Input

```python
name = input("Enter student name: ")
roll_no = int(input("Enter roll number: "))
course = input("Enter course: ")
marks = float(input("Enter marks: "))

student = {
    "name": name,
    "roll_no": roll_no,
    "course": course,
    "marks": marks
}

print(student)
```

Example:

```text
Enter student name: Pavan
Enter roll number: 101
Enter course: Python
Enter marks: 88
```

Output:

```text
{'name': 'Pavan', 'roll_no': 101, 'course': 'Python', 'marks': 88.0}
```

---

# 👨‍💻 Practical Program 3 — Display Student Information

```python
student = {
    "name": "Pavan",
    "roll_no": 101,
    "course": "Python",
    "marks": 88
}

print("Name:", student["name"])
print("Roll No:", student["roll_no"])
print("Course:", student["course"])
print("Marks:", student["marks"])
```

---

# 👨‍💻 Practical Program 4 — Add, Update and Delete

```python
student = {
    "name": "Pavan",
    "roll_no": 101,
    "course": "Python",
    "marks": 85
}

# Add
student["city"] = "Bangalore"

# Update
student["marks"] = 95

# Delete
del student["roll_no"]

print(student)
```

### Final Output

```python
{
    "name": "Pavan",
    "course": "Python",
    "marks": 95,
    "city": "Bangalore"
}
```

---

# 🧠 Quick MCQ Revision

### 1. Dictionary stores data in what form?

**Answer:** Key-value pairs

---

### 2. What symbols are commonly used to create a dictionary?

```python
{}
```

---

### 3. How do you access a value?

```python
student["name"]
```

---

### 4. What happens when you assign to an existing key?

```python
student["marks"] = 90
```

**Answer:** The existing value is updated.

---

### 5. What happens when you assign to a new key?

```python
student["city"] = "Bangalore"
```

**Answer:** A new key-value pair is added.

---

### 6. Which method returns keys?

```python
student.keys()
```

**Answer:** `keys()`

---

### 7. Which method returns values?

```python
student.values()
```

**Answer:** `values()`

---

### 8. Which method returns key-value pairs?

```python
student.items()
```

**Answer:** `items()`

---

### 9. What happens if a missing key is accessed using `[]`?

```python
student["xyz"]
```

**Answer:** `KeyError`

---

### 10. What does `get()` return for a missing key by default?

```python
student.get("xyz")
```

**Answer:** `None`

---

### 11. Which keyword deletes a dictionary item?

```python
del student["age"]
```

**Answer:** `del`

---

### 12. Which method removes a key and can return its value?

```python
student.pop("age")
```

**Answer:** `pop()`

---

# 📌 Dictionary Cheat Sheet

| Operation | Syntax |
|---|---|
| Create | `student = {}` |
| Add | `student["city"] = "Bangalore"` |
| Access | `student["name"]` |
| Safe access | `student.get("name")` |
| Update | `student["marks"] = 95` |
| Delete | `del student["marks"]` |
| Remove + return | `student.pop("marks")` |
| Get keys | `student.keys()` |
| Get values | `student.values()` |
| Get pairs | `student.items()` |
| Count items | `len(student)` |

---

# 🎯 Practice Challenge

Create a dictionary called `employee` containing:

```text
name → your name
id → 101
department → IT
salary → 30000
```

Then:

1. Print the employee's name.
2. Change salary to `35000`.
3. Add `"location": "Bangalore"`.
4. Delete the `id`.
5. Print all keys.
6. Print all values.
7. Print all key-value pairs.

### Expected concepts

```python
employee["name"]

employee["salary"] = 35000

employee["location"] = "Bangalore"

del employee["id"]

employee.keys()
employee.values()
employee.items()
```

---

# 📝 Homework

Create a student dictionary with:

- `name`
- `roll_no`
- `course`
- `marks`

Then:

- Add one new key
- Update one existing key
- Delete one key
- Print the final dictionary

---

## 🔄 Day 24 Final Recap

> **Dictionary = Key + Value**

```python
student = {
    "name": "Pavan",
    "age": 21
}
```

The most important things to remember:

```text
Access  → dictionary[key]
Add     → dictionary[new_key] = value
Update  → dictionary[existing_key] = new_value
Delete  → del dictionary[key]
Remove  → dictionary.pop(key)

keys()   → keys
values() → values
items()  → key + value
get()    → safely access a value
len()    → number of key-value pairs
```

---

**Next Topic: Day 25 — Dictionaries – II**
