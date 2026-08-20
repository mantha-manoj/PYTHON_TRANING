# Day 11 – Conditional Statements in Python

## 📚 Topics Covered

- Conditional statements
- `if` statement
- `if-else` statement
- `if-elif-else` statement
- Comparison operators
- Modulus operator `%`
- Indentation in Python
- Nested `if` statements
- Basic decision-making programs

---

## 1. What are Conditional Statements?

Conditional statements are used to make decisions in a Python program based on whether a condition is `True` or `False`.

### Real-Life Example

> If it is raining → Take an umbrella  
> Otherwise → Don't take an umbrella

Python allows us to implement the same logic using `if`, `elif`, and `else`.

---

## 2. Comparison Operators

Comparison operators are commonly used inside conditions.

| Operator | Meaning | Example |
|---|---|---|
| `>` | Greater than | `a > b` |
| `<` | Less than | `a < b` |
| `>=` | Greater than or equal to | `a >= b` |
| `<=` | Less than or equal to | `a <= b` |
| `==` | Equal to | `a == b` |
| `!=` | Not equal to | `a != b` |

---

## 3. `if` Statement

The `if` statement executes a block of code only when the condition is `True`.

### Syntax

```python
if condition:
    statement
```

### Example

```python
age = 20

if age >= 18:
    print("Eligible to vote")
```

### Important

Python uses **indentation** to identify the statements belonging to the `if` block.

---

## 4. `if-else` Statement

Use `if-else` when there are two possible outcomes.

### Example

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("Eligible to vote")
else:
    print("Not eligible to vote")
```

### Flow

```text
          age >= 18?
          /       \
        YES        NO
         |          |
     Eligible   Not Eligible
```

---

## 5. `if-elif-else`

Use `if-elif-else` when there are multiple conditions.

### Example

```python
marks = int(input("Enter marks: "))

if marks >= 90:
    print("A+")
elif marks >= 75:
    print("A")
elif marks >= 60:
    print("B")
elif marks >= 50:
    print("C")
else:
    print("Fail")
```

Python checks the conditions from **top to bottom** and executes the first matching condition.

---

## 6. Positive, Negative or Zero

```python
num = int(input("Enter a number: "))

if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")
```

### Sample Output

```text
Input: 25
Output: Positive

Input: -10
Output: Negative

Input: 0
Output: Zero
```

---

## 7. Even or Odd

The modulus operator `%` returns the remainder.

```python
num = int(input("Enter a number: "))

if num % 2 == 0:
    print("Even")
else:
    print("Odd")
```

### Example

```python
10 % 2
```

Output:

```text
0
```

Therefore, `10` is even.

---

## 8. Nested `if`

An `if` statement inside another `if` statement is called a **nested if**.

### Example

```python
num = int(input("Enter a number: "))

if num > 0:
    print("Positive")

    if num % 2 == 0:
        print("Even")
    else:
        print("Odd")

elif num < 0:
    print("Negative")

    if num % 2 == 0:
        print("Even")
    else:
        print("Odd")

else:
    print("Zero")
```

### Sample Output

```text
Enter a number: 15

Positive
Odd
```

---

## 9. Important Difference: `=` vs `==`

### `=`

Used for **assignment**.

```python
age = 20
```

### `==`

Used for **comparison**.

```python
age == 20
```

### Common Mistake

❌ Wrong:

```python
if age = 18:
```

✅ Correct:

```python
if age == 18:
```

---

## 10. Common Python Mistakes

### Missing colon

❌

```python
if age >= 18
```

✅

```python
if age >= 18:
```

### Incorrect indentation

❌

```python
if age >= 18:
print("Eligible")
```

✅

```python
if age >= 18:
    print("Eligible")
```

---

# 🧑‍💻 Practice Programs

Try writing these programs without looking at the solutions:

1. Check whether a number is positive, negative or zero.
2. Check whether a number is even or odd.
3. Check whether a person is eligible to vote.
4. Find the largest of two numbers.
5. Check whether a student passed or failed.
6. Check whether a number is divisible by 5.
7. Check whether a person is eligible for a driving license.
8. Check whether a number is greater than, less than, or equal to 100.
9. Check whether a year is a leap year.
10. Create a simple login system using username and password.

---

# 🚀 Day 11 Mini Project – Number Analyzer

Create a program that accepts one number and displays:

- Positive / Negative / Zero
- Even / Odd
- Greater than 100 / Less than or equal to 100

### Expected Example

```text
Enter a number: 150

Positive
Even
Greater than 100
```

---

## 📝 Quick Revision

```text
if
    ↓
One condition

if-else
    ↓
Two possible outcomes

if-elif-else
    ↓
Multiple conditions

nested if
    ↓
Condition inside another condition
```

### Key Points

- Conditions evaluate to `True` or `False`.
- Use `:` after `if`, `elif`, and `else`.
- Python uses indentation to define blocks.
- Use `==` for comparison.
- Use `%` to check divisibility and even/odd numbers.
- Conditions are evaluated from top to bottom in an `if-elif-else` chain.

---

## 🎯 Day 11 Goal

By the end of Day 11, you should be able to:

- Write `if` statements.
- Write `if-else` statements.
- Write `if-elif-else` statements.
- Use comparison operators.
- Use `%` with conditions.
- Build basic decision-making programs.
- Combine multiple conditions using nested `if`.

---

**Python 45 Days Challenge – Day 11** 🐍
