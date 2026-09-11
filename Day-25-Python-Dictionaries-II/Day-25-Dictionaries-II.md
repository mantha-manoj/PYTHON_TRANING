# Day 25 — Python Dictionaries II

## 📚 Topic
**Dictionaries – II: Iteration, Total, Average, Highest and Lowest Values**

**Duration:** 1 Hour 30 Minutes

---

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Store multiple records in a dictionary.
- Iterate through dictionary keys and values.
- Use `keys()`, `values()`, and `items()`.
- Calculate total and average values.
- Find the highest and lowest values.
- Find the key associated with the highest/lowest value.
- Apply dictionaries to practical problems such as student marks and employee salaries.

---

# 1. Dictionary with Multiple Records

A dictionary stores data as **key-value pairs**.

```python
students = {
    "Rahul": 85,
    "Priya": 92,
    "Arun": 78,
    "Sneha": 95,
    "Kiran": 88
}
```

Here:

- Student name → **key**
- Marks → **value**

Example:

```python
print(students["Rahul"])
```

Output:

```text
85
```

---

# 2. Dictionary Methods

## `keys()`

Returns all keys.

```python
print(students.keys())
```

Conceptually:

```text
Rahul
Priya
Arun
Sneha
Kiran
```

---

## `values()`

Returns all values.

```python
print(students.values())
```

Conceptually:

```text
85
92
78
95
88
```

---

## `items()`

Returns both key and value.

```python
print(students.items())
```

Conceptually:

```text
("Rahul", 85)
("Priya", 92)
("Arun", 78)
("Sneha", 95)
("Kiran", 88)
```

---

# 3. Iterating Through a Dictionary

## Print only keys

```python
for name in students:
    print(name)
```

Output:

```text
Rahul
Priya
Arun
Sneha
Kiran
```

---

## Print only values

```python
for marks in students.values():
    print(marks)
```

Output:

```text
85
92
78
95
88
```

---

## Print keys and values

The most useful approach:

```python
for name, marks in students.items():
    print(name, marks)
```

Output:

```text
Rahul 85
Priya 92
Arun 78
Sneha 95
Kiran 88
```

### Remember

```python
for key, value in dictionary.items():
```

means:

```text
key   → dictionary key
value → dictionary value
```

---

# 4. Finding the Total

We can calculate the total using a loop.

```python
total = 0

for name, marks in students.items():
    total += marks

print("Total:", total)
```

Output:

```text
Total: 438
```

### How it works

```text
0 + 85 = 85
85 + 92 = 177
177 + 78 = 255
255 + 95 = 350
350 + 88 = 438
```

Therefore:

```text
Total = 438
```

---

# 5. Finding the Average

### Formula

```text
Average = Total / Number of Students
```

Python:

```python
total = 0

for name, marks in students.items():
    total += marks

average = total / len(students)

print("Average:", average)
```

Output:

```text
Average: 87.6
```

### `len()`

```python
len(students)
```

returns the number of key-value pairs.

For this dictionary:

```text
5 students
```

---

# 6. Finding the Topper

We can find the student with the highest marks using a loop.

```python
topper = ""
highest_marks = 0

for name, marks in students.items():

    if marks > highest_marks:
        highest_marks = marks
        topper = name

print("Topper:", topper)
print("Marks:", highest_marks)
```

Output:

```text
Topper: Sneha
Marks: 95
```

## Logic

Initially:

```python
highest_marks = 0
topper = ""
```

For every student:

```python
if marks > highest_marks:
```

If the current marks are greater, update:

```python
highest_marks = marks
topper = name
```

---

# 7. Finding the Lowest Marks

The same logic can be used to find the lowest marks.

```python
lowest_marks = 999
lowest_student = ""

for name, marks in students.items():

    if marks < lowest_marks:
        lowest_marks = marks
        lowest_student = name

print("Lowest Student:", lowest_student)
print("Marks:", lowest_marks)
```

Output:

```text
Lowest Student: Arun
Marks: 78
```

> `999` is used as an initial value here because student marks are normally below 999. Another option is to initialize from the first dictionary value.

---

# 8. Using `max()`

Python has a built-in `max()` function.

To find the highest mark:

```python
highest_marks = max(students.values())

print(highest_marks)
```

Output:

```text
95
```

To find the student name:

```python
topper = max(students, key=students.get)

print("Topper:", topper)
print("Marks:", students[topper])
```

Output:

```text
Topper: Sneha
Marks: 95
```

### Important

First learn the loop-based approach because it helps you understand the logic. Then use `max()` as a shorter Python solution.

---

# 9. Complete Student Report Program

```python
students = {
    "Rahul": 85,
    "Priya": 92,
    "Arun": 78,
    "Sneha": 95,
    "Kiran": 88
}

total = 0
topper = ""
highest_marks = 0
lowest_student = ""
lowest_marks = 999

for name, marks in students.items():

    print(name, ":", marks)

    total += marks

    if marks > highest_marks:
        highest_marks = marks
        topper = name

    if marks < lowest_marks:
        lowest_marks = marks
        lowest_student = name

average = total / len(students)

print("\nTotal Marks:", total)
print("Average Marks:", average)
print("Topper:", topper)
print("Highest Marks:", highest_marks)
print("Lowest Student:", lowest_student)
print("Lowest Marks:", lowest_marks)
```

### Output

```text
Rahul : 85
Priya : 92
Arun : 78
Sneha : 95
Kiran : 88

Total Marks: 438
Average Marks: 87.6
Topper: Sneha
Highest Marks: 95
Lowest Student: Arun
Lowest Marks: 78
```

---

# 10. Practical Example — Employee Salaries

Dictionaries are not limited to student marks.

```python
employees = {
    "John": 45000,
    "David": 55000,
    "Sara": 48000,
    "Mike": 60000
}
```

Find the employee with the highest salary:

```python
highest_salary = 0
highest_employee = ""

for name, salary in employees.items():

    if salary > highest_salary:
        highest_salary = salary
        highest_employee = name

print("Highest Salary:", highest_salary)
print("Employee:", highest_employee)
```

Output:

```text
Highest Salary: 60000
Employee: Mike
```

---

# 11. Count Students Scoring 80 or Above

This is another useful dictionary + loop problem.

```python
students = {
    "Rahul": 85,
    "Priya": 92,
    "Arun": 78,
    "Sneha": 95,
    "Kiran": 88
}

count = 0

for name, marks in students.items():

    if marks >= 80:
        count += 1

print("Students scoring 80 or above:", count)
```

Output:

```text
Students scoring 80 or above: 4
```

---

# 12. Key Concepts

| Concept | Syntax |
|---|---|
| Get keys | `dictionary.keys()` |
| Get values | `dictionary.values()` |
| Get key + value | `dictionary.items()` |
| Number of records | `len(dictionary)` |
| Highest value | `max(dictionary.values())` |
| Loop through dictionary | `for key, value in dictionary.items()` |
| Add to total | `total += value` |
| Compare values | `if value > highest:` |

---

# 🧠 Quick Revision

### Dictionary

```python
students = {
    "Rahul": 85,
    "Priya": 92
}
```

### Loop

```python
for name, marks in students.items():
    print(name, marks)
```

### Total

```python
total = 0

for marks in students.values():
    total += marks
```

### Average

```python
average = total / len(students)
```

### Highest

```python
highest = max(students.values())
```

### Topper

```python
topper = max(students, key=students.get)
```

---

# 💻 Practice Questions

## Question 1

Create a dictionary containing 5 students and their marks.

Write a program to:

1. Print all students and marks.
2. Calculate total marks.
3. Calculate average marks.
4. Find the topper.
5. Print topper's marks.

---

## Question 2

Using:

```python
students = {
    "Rahul": 85,
    "Priya": 92,
    "Arun": 78,
    "Sneha": 95,
    "Kiran": 88
}
```

Find the student with the lowest marks.

Expected output:

```text
Lowest Student: Arun
Marks: 78
```

---

## Question 3

Count how many students scored 80 or above.

Expected output:

```text
Students scoring 80 or above: 4
```

---

# 🚀 Challenge

Create a dictionary of 10 students and their marks.

Display:

```text
----- STUDENT REPORT -----

Student Name : Marks

Total Marks
Average Marks
Topper
Highest Marks
Lowest Student
Lowest Marks
Students scoring 80 or above
```

Try to solve the challenge **without using `max()` or `min()` first**. Use loops and conditions.

---

# ❓ Interview / Viva Questions

1. What is a dictionary?
2. What is the difference between `keys()` and `values()`?
3. What does `items()` return?
4. How do you iterate through a dictionary?
5. What does `len(dictionary)` return?
6. How can you calculate the total of dictionary values?
7. How can you find the highest value?
8. How can you find the key associated with the highest value?
9. What is the difference between `max(dictionary.values())` and `max(dictionary, key=dictionary.get)`?
10. Can dictionaries be used for data other than student marks?

---

# 📝 Homework

Create a dictionary containing **10 students and their marks**.

Write a Python program to find:

- All students and marks
- Total marks
- Average marks
- Highest marks
- Topper's name
- Lowest marks
- Lowest-scoring student's name
- Number of students who scored 80 or above

---

## 📌 Day-25 Summary

Today you learned how to use dictionaries with loops to process multiple records.

The most important pattern from today's lesson is:

```python
for key, value in dictionary.items():
    # process key and value
```

This pattern is widely used when working with structured data in Python.

---

**Previous:** Day 24 — Dictionaries I  
**Next:** Day 26 — Functions Basics I
