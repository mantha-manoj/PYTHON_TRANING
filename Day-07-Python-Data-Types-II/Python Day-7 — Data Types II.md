# 🐍 Python Day-7 — Data Types II

## 📚 Topic
**Python Data Types – II**

Today we learn four important collection data types in Python:

- List
- Tuple
- Set
- Dictionary

These data types are used to store and manage **multiple values in a single variable**.

---

## 🎯 Learning Objectives

By the end of this session, you will understand:

- What collection data types are
- How to create Lists
- How to create Tuples
- How to create Sets
- How to create Dictionaries
- Difference between List, Tuple, Set and Dictionary
- How to access and modify collection elements
- Basic methods of each collection
- When to use each collection type

---

# 1. 📋 List

A **List** is an ordered and changeable collection of elements.

### Syntax

```python
list_name = [value1, value2, value3]
```

### Example

```python
students = ["Pavan", "Rahul", "Anil", "Kiran"]

print(students)
```

### Output

```text
['Pavan', 'Rahul', 'Anil', 'Kiran']
```

### Important Properties

- Ordered
- Mutable (changeable)
- Allows duplicate values
- Allows different data types
- Supports indexing

### Example

```python
data = [10, 20, 30, 40, 50]

print(data[0])
print(data[2])
print(data[-1])
```

Output:

```text
10
30
50
```

---

## 🔄 Modifying a List

Lists are mutable.

```python
students = ["Pavan", "Rahul", "Anil"]

students[1] = "Kiran"

print(students)
```

Output:

```text
['Pavan', 'Kiran', 'Anil']
```

---

## ➕ Adding Elements

### append()

Adds an element at the end.

```python
students = ["Pavan", "Rahul"]

students.append("Anil")

print(students)
```

Output:

```text
['Pavan', 'Rahul', 'Anil']
```

### insert()

Adds an element at a specific position.

```python
students = ["Pavan", "Rahul"]

students.insert(1, "Anil")

print(students)
```

Output:

```text
['Pavan', 'Anil', 'Rahul']
```

---

## ❌ Removing Elements

### remove()

```python
students = ["Pavan", "Rahul", "Anil"]

students.remove("Rahul")

print(students)
```

### pop()

Removes an element using its index.

```python
students = ["Pavan", "Rahul", "Anil"]

students.pop(1)

print(students)
```

### clear()

Removes all elements.

```python
students = [10, 20, 30]

students.clear()

print(students)
```

Output:

```text
[]
```

---

# 2. 🔒 Tuple

A **Tuple** is an ordered collection that **cannot be changed after creation**.

### Syntax

```python
tuple_name = (value1, value2, value3)
```

### Example

```python
marks = (85, 90, 78, 92)

print(marks)
```

Output:

```text
(85, 90, 78, 92)
```

### Important Properties

- Ordered
- Immutable (cannot be changed)
- Allows duplicate values
- Allows different data types
- Supports indexing

---

## Tuple Indexing

```python
numbers = (10, 20, 30, 40)

print(numbers[0])
print(numbers[2])
print(numbers[-1])
```

Output:

```text
10
30
40
```

---

## ❌ Tuple Cannot Be Modified

```python
numbers = (10, 20, 30)

numbers[0] = 100
```

This produces an error because tuples are immutable.

```text
TypeError
```

### When should we use Tuple?

Use a tuple when the data should **not be changed**.

Example:

```python
days = ("Monday", "Tuesday", "Wednesday", "Thursday", "Friday")
```

---

# 3. 🔵 Set

A **Set** is an unordered collection of unique elements.

### Syntax

```python
set_name = {value1, value2, value3}
```

### Example

```python
numbers = {10, 20, 30, 40}

print(numbers)
```

### Important Properties

- Unordered
- Mutable
- Does not allow duplicate values
- Does not support indexing
- Useful for removing duplicates

---

## Duplicate Values in Set

```python
numbers = {10, 20, 20, 30, 30, 40}

print(numbers)
```

The duplicate values are automatically removed.

Possible output:

```text
{10, 20, 30, 40}
```

---

## Adding Elements to Set

### add()

```python
numbers = {10, 20, 30}

numbers.add(40)

print(numbers)
```

---

## Removing Elements from Set

### remove()

```python
numbers = {10, 20, 30}

numbers.remove(20)

print(numbers)
```

### discard()

```python
numbers = {10, 20, 30}

numbers.discard(50)

print(numbers)
```

`discard()` does not produce an error if the element does not exist.

---

# 4. 📖 Dictionary

A **Dictionary** stores data in **key-value pairs**.

### Syntax

```python
dictionary_name = {
    "key": "value"
}
```

### Example

```python
student = {
    "name": "Pavan",
    "age": 23,
    "course": "Python",
    "marks": 85
}

print(student)
```

Output:

```text
{
    'name': 'Pavan',
    'age': 23,
    'course': 'Python',
    'marks': 85
}
```

---

## 🔑 Accessing Dictionary Values

Values are accessed using their keys.

```python
student = {
    "name": "Pavan",
    "age": 23,
    "marks": 85
}

print(student["name"])
print(student["marks"])
```

Output:

```text
Pavan
85
```

---

## 🔄 Modifying Dictionary Values

```python
student = {
    "name": "Pavan",
    "age": 23
}

student["age"] = 24

print(student)
```

---

## ➕ Adding New Key-Value Pair

```python
student = {
    "name": "Pavan",
    "age": 23
}

student["course"] = "Python"

print(student)
```

Output:

```text
{'name': 'Pavan', 'age': 23, 'course': 'Python'}
```

---

## ❌ Removing Dictionary Elements

### pop()

```python
student = {
    "name": "Pavan",
    "age": 23,
    "course": "Python"
}

student.pop("age")

print(student)
```

### clear()

```python
student.clear()

print(student)
```

Output:

```text
{}
```

---

# 5. 🔍 Checking the Type

Python provides the `type()` function to identify the data type.

```python
numbers = [10, 20, 30]
names = ("Pavan", "Rahul")
cities = {"Bangalore", "Hyderabad"}
student = {"name": "Pavan", "age": 23}

print(type(numbers))
print(type(names))
print(type(cities))
print(type(student))
```

Output:

```text
<class 'list'>
<class 'tuple'>
<class 'set'>
<class 'dict'>
```

---

# 6. 🧑‍🎓 Student Details Using Collections

We can represent student information using different collection types.

### List

```python
students = ["Pavan", "Rahul", "Anil", "Kiran"]

print(students)
```

### Tuple

```python
marks = (85, 90, 78, 92)

print(marks)
```

### Set

```python
courses = {"Python", "Java", "SQL", "Python"}

print(courses)
```

Duplicate `"Python"` will be removed.

### Dictionary

```python
student = {
    "name": "Pavan",
    "age": 23,
    "course": "Python",
    "marks": 85
}

print(student)
```

---

# 7. 🆚 List vs Tuple vs Set vs Dictionary

| Feature | List | Tuple | Set | Dictionary |
|---|---|---|---|---|
| Syntax | `[]` | `()` | `{}` | `{key:value}` |
| Ordered | Yes | Yes | No* | Yes |
| Mutable | Yes | No | Yes | Yes |
| Duplicates | Yes | Yes | No | Keys: No |
| Indexing | Yes | Yes | No | Key-based |
| Stores | Values | Values | Unique values | Key-value pairs |

> **Note:** Modern Python sets are unordered, while dictionaries preserve insertion order.

---

# 8. 🧠 Real-World Examples

### List

Use a list when you need an ordered collection that can change.

```python
shopping_cart = ["Laptop", "Mouse", "Keyboard"]
```

### Tuple

Use a tuple for fixed data.

```python
coordinates = (12.9716, 77.5946)
```

### Set

Use a set when you need unique values.

```python
unique_courses = {"Python", "Java", "Python", "SQL"}
```

### Dictionary

Use a dictionary when information has labels/keys.

```python
employee = {
    "id": 101,
    "name": "Pavan",
    "department": "IT",
    "salary": 50000
}
```

---

# 9. 💡 Important Interview Questions

### Q1. What is a List?

A List is an ordered and mutable collection that allows duplicate values.

### Q2. What is a Tuple?

A Tuple is an ordered and immutable collection.

### Q3. What is a Set?

A Set is an unordered collection of unique elements.

### Q4. What is a Dictionary?

A Dictionary stores data in key-value pairs.

### Q5. Which collection does not allow duplicate values?

**Set**

### Q6. Which collection is immutable?

**Tuple**

### Q7. Can a List contain different data types?

Yes.

```python
data = [10, "Python", 10.5, True]
```

### Q8. Can a Set contain duplicate values?

No.

### Q9. How do you access a dictionary value?

Using its key.

```python
student["name"]
```

### Q10. Which collection should you use for key-value data?

**Dictionary**

---

# 10. 💻 Day-7 Practice Program

## Program: Student Details Using Collections

Create a Python program that stores student information using List, Tuple, Set and Dictionary.

```python
# List
students = ["Pavan", "Rahul", "Anil"]

# Tuple
marks = (85, 90, 78)

# Set
courses = {"Python", "Java", "SQL"}

# Dictionary
student = {
    "name": "Pavan",
    "age": 23,
    "course": "Python",
    "marks": 85
}

print("Students:", students)
print("Type:", type(students))

print("Marks:", marks)
print("Type:", type(marks))

print("Courses:", courses)
print("Type:", type(courses))

print("Student Details:", student)
print("Type:", type(student))
```

---

# 11. 📝 Student Practice Tasks

### Task 1 — List

Create a list containing 5 student names.

Perform:

- Add one student
- Remove one student
- Change one student name
- Print the first student
- Print the last student

### Task 2 — Tuple

Create a tuple containing 5 subject names.

Perform:

- Print the first subject
- Print the last subject
- Find the number of subjects

### Task 3 — Set

Create a set containing:

```text
Python
Java
Python
SQL
Java
HTML
```

Print the set and observe what happens to duplicate values.

### Task 4 — Dictionary

Create a dictionary containing:

```text
Name
Age
Course
College
Marks
```

Then:

- Print the student's name
- Change the marks
- Add a new key called `city`
- Remove the age
- Print the complete dictionary

---

# 12. 🔥 Challenge Program

Create a student management program using a dictionary.

```python
student = {
    "name": "Pavan",
    "age": 23,
    "course": "Python",
    "marks": 85,
    "city": "Bangalore"
}

print("Student Name:", student["name"])
print("Age:", student["age"])
print("Course:", student["course"])
print("Marks:", student["marks"])
print("City:", student["city"])
```

### Challenge

Modify the program so that the student details are taken from the user using `input()`.

---

# 13. 📌 Key Takeaways

- **List** → Ordered + Mutable + Duplicates allowed
- **Tuple** → Ordered + Immutable + Duplicates allowed
- **Set** → Unique values + No indexing
- **Dictionary** → Key-value pairs
- `type()` → Used to identify the data type
- Lists use `[]`
- Tuples use `()`
- Sets use `{}` 
- Dictionaries use `{key: value}`

---

# 🎯 Day-7 Final Goal

You should now be able to answer:

> **"Which Python collection should I use?"**

### Quick Rule

```text
Need an ordered collection that can change?
        ↓
      LIST

Need fixed data that should not change?
        ↓
      TUPLE

Need only unique values?
        ↓
       SET

Need key-value information?
        ↓
   DICTIONARY
```

---

## 🚀 GitHub Practice Checklist

- [ ] Understand List
- [ ] Practice List methods
- [ ] Understand Tuple
- [ ] Practice Tuple indexing
- [ ] Understand Set
- [ ] Practice Set methods
- [ ] Understand Dictionary
- [ ] Practice Dictionary operations
- [ ] Complete Student Details Program
- [ ] Complete all Day-7 practice tasks
- [ ] Complete Challenge Program
- [ ] Push Day-7 code to GitHub

---

### 📅 Course Progress

**Day 1:** Python Overview  
**Day 2:** Python Installation  
**Day 3:** Python Basics – Syntax  
**Day 4:** Variables & Keywords – I  
**Day 5:** Variables & Keywords – II  
**Day 6:** Data Types – I  
**👉 Day 7:** **Data Types – II**  
**Day 8:** Next Topic

---

⭐ **Practice every program yourself. Don't just copy the code — type it, execute it, make mistakes, and fix them.**

**Happy Coding! 🐍💻**