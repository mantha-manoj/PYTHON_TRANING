# Day 12 – Conditional Statements II

## 📅 Day 12
**Topic:** Conditional Statements – II  
**Duration:** 1 Hour 30 Minutes  
**Language:** Python

---

## 🎯 Learning Objectives

By the end of this session, you will be able to:

- Use `if`, `elif`, and `else`
- Write programs with multiple conditions
- Use relational operators in conditions
- Use logical operators: `and`, `or`, and `not`
- Understand nested `if` statements
- Build a Student Grade Calculator
- Validate user input using conditions

---

# 1. Conditional Statements

Conditional statements allow a program to make decisions based on conditions.

### Basic `if`

```python
age = 20

if age >= 18:
    print("Eligible to vote")
```

The code inside the `if` block executes only when the condition is `True`.

---

# 2. `if-else`

Use `else` when there are two possible outcomes.

```python
num = 10

if num > 0:
    print("Positive")
else:
    print("Negative")
```

### Output

```text
Positive
```

### Structure

```python
if condition:
    # Executes when condition is True
else:
    # Executes when condition is False
```

---

# 3. `if-elif-else`

When there are multiple possible conditions, use `elif`.

### Syntax

```python
if condition1:
    statement
elif condition2:
    statement
elif condition3:
    statement
else:
    statement
```

### Example

```python
marks = 75

if marks >= 90:
    print("A")
elif marks >= 75:
    print("B")
elif marks >= 60:
    print("C")
elif marks >= 40:
    print("D")
else:
    print("Fail")
```

### Output

```text
B
```

Python checks conditions from **top to bottom**. Once a condition becomes `True`, its block executes and the remaining `elif` conditions are skipped.

---

# 4. Importance of Condition Order

The order of conditions matters.

### ❌ Incorrect

```python
marks = 95

if marks >= 40:
    print("D")
elif marks >= 60:
    print("C")
elif marks >= 75:
    print("B")
elif marks >= 90:
    print("A")
```

### Output

```text
D
```

Why?

Because `95 >= 40` is already `True`.

### ✅ Correct

```python
marks = 95

if marks >= 90:
    print("A")
elif marks >= 75:
    print("B")
elif marks >= 60:
    print("C")
elif marks >= 40:
    print("D")
else:
    print("Fail")
```

### Rule

> For range-based conditions, check the higher/specific range first.

---

# 5. Relational Operators

Relational operators are commonly used inside conditions.

| Operator | Meaning | Example |
|---|---|---|
| `>` | Greater than | `a > b` |
| `<` | Less than | `a < b` |
| `>=` | Greater than or equal to | `marks >= 40` |
| `<=` | Less than or equal to | `age <= 60` |
| `==` | Equal to | `x == 10` |
| `!=` | Not equal to | `x != 10` |

### Important

```python
=   # Assignment
==  # Comparison
```

Example:

```python
x = 10

if x == 10:
    print("x is 10")
```

---

# 6. Logical Operators

Logical operators combine multiple conditions.

## `and`

Both conditions must be `True`.

```python
age = 25

if age >= 18 and age <= 60:
    print("Eligible")
```

---

## `or`

At least one condition must be `True`.

```python
day = "Saturday"

if day == "Saturday" or day == "Sunday":
    print("Weekend")
```

---

## `not`

Reverses a condition.

```python
is_raining = False

if not is_raining:
    print("Go outside")
```

### Quick Summary

| Operator | Meaning |
|---|---|
| `and` | Both conditions must be true |
| `or` | At least one condition must be true |
| `not` | Reverses the condition |

---

# 7. Nested `if`

A nested `if` means an `if` statement inside another `if` statement.

```python
marks = 85

if marks >= 40:
    print("Pass")

    if marks >= 75:
        print("Distinction")
else:
    print("Fail")
```

### Output

```text
Pass
Distinction
```

### Structure

```text
if condition
│
├── True
│   └── another if condition
│
└── False
    └── else block
```

---

# 8. Student Grade Calculator

## Basic Version

```python
marks = float(input("Enter your marks: "))

if marks >= 90:
    grade = "A"
elif marks >= 75:
    grade = "B"
elif marks >= 60:
    grade = "C"
elif marks >= 40:
    grade = "D"
else:
    grade = "Fail"

print("Grade:", grade)
```

### Sample Output

```text
Enter your marks: 82
Grade: B
```

---

# 9. Grade Calculator with Validation

We should also make sure the user enters marks between `0` and `100`.

```python
marks = float(input("Enter your marks: "))

if marks < 0 or marks > 100:
    print("Invalid marks")

elif marks >= 90:
    print("Grade: A")

elif marks >= 75:
    print("Grade: B")

elif marks >= 60:
    print("Grade: C")

elif marks >= 40:
    print("Grade: D")

else:
    print("Fail")
```

### Test Cases

| Marks | Result |
|---:|---|
| 95 | A |
| 82 | B |
| 65 | C |
| 45 | D |
| 30 | Fail |
| 105 | Invalid marks |
| -10 | Invalid marks |

---

# 10. Advanced Student Grade Calculator

```python
name = input("Enter student name: ")
marks = float(input("Enter marks: "))

if marks < 0 or marks > 100:
    print("Invalid marks")

elif marks >= 90:
    grade = "A"
    result = "Excellent"

elif marks >= 75:
    grade = "B"
    result = "Very Good"

elif marks >= 60:
    grade = "C"
    result = "Good"

elif marks >= 40:
    grade = "D"
    result = "Pass"

else:
    grade = "F"
    result = "Fail"

print("\nStudent:", name)
print("Marks:", marks)
print("Grade:", grade)
print("Result:", result)
```

### Sample Output

```text
Enter student name: Pavan
Enter marks: 86

Student: Pavan
Marks: 86.0
Grade: B
Result: Very Good
```

---

# 11. Practice Programs

## Program 1 – Age Category

Write a program to classify a person's age.

```text
0–12    → Child
13–19   → Teenager
20–59   → Adult
60+     → Senior Citizen
```

---

## Program 2 – Largest of Three Numbers

Take three numbers and find the largest.

### Example

```text
Enter a: 25
Enter b: 40
Enter c: 15

Largest = 40
```

---

## Program 3 – Electricity Bill

Create an electricity bill calculator.

```text
0–100 units       → ₹5/unit
101–200 units     → ₹7/unit
201–300 units     → ₹10/unit
Above 300 units   → ₹15/unit
```

---

## Program 4 – Login System

```python
username = input("Username: ")
password = input("Password: ")

if username == "admin" and password == "1234":
    print("Login successful")
else:
    print("Invalid username or password")
```

---

# 12. Final Challenge

Create a Python program that accepts:

- Student name
- Marks in 5 subjects

Then calculate:

1. Total marks
2. Average marks
3. Grade

### Grade Criteria

```text
Average >= 90 → A
Average >= 75 → B
Average >= 60 → C
Average >= 40 → D
Below 40      → Fail
```

### Concepts to Use

```text
input()
float()
+
/
if
elif
else
```

---

# 13. Quick Quiz

### Q1. What is the purpose of `elif`?

A. Repeat code  
B. Check another condition  
C. Create a variable  
D. Stop Python

**Answer: B**

---

### Q2. What is the output?

```python
x = 80

if x >= 90:
    print("A")
elif x >= 75:
    print("B")
else:
    print("C")
```

**Answer:**

```text
B
```

---

### Q3. Which operator means "equal to"?

A. `=`  
B. `==`  
C. `!=`  
D. `===`

**Answer: B**

---

### Q4. What does `and` mean?

A. Any one condition is true  
B. Both conditions are true  
C. Reverse the condition  
D. None

**Answer: B**

---

### Q5. What happens when no `if` or `elif` condition is true?

**Answer:** The `else` block executes.

---

# 14. Key Takeaways

```text
if       → Checks the first condition
elif     → Checks additional conditions
else     → Executes when no condition is true

and      → Both conditions must be true
or       → At least one condition must be true
not      → Reverses a condition

Nested if → An if statement inside another if
```

## 💡 Important Rule

> Python evaluates `if` / `elif` conditions from top to bottom and executes only the first matching block.

---

## 🚀 Day 12 Summary

Today we learned how to make Python programs smarter by allowing them to make decisions based on multiple conditions.

The main practical program was the **Student Grade Calculator**, which combines:

- Input
- Type conversion
- Relational operators
- Logical operators
- `if`
- `elif`
- `else`
- Validation

**Next Topic: Day 13 – Looping Statements I (`for` loop)**
