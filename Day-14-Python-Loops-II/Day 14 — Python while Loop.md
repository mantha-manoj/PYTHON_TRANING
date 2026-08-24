# 🐍 Python 45 Days — Day 14

## 🔁 Topic: `while` Loop

**Duration:** 1 Hour 30 Minutes  
**Day:** 14  
**Level:** Beginner

---

## 🎯 Learning Objectives

By the end of this lesson, you will be able to:

- Understand the `while` loop
- Write the syntax of a `while` loop
- Use conditions with `while`
- Increment and decrement variables
- Avoid infinite loops
- Use `while` loops with user input
- Calculate sums using loops
- Generate multiplication tables
- Calculate factorials

---

## 1. What is a `while` Loop?

A `while` loop is used to repeatedly execute a block of code **as long as a condition is `True`**.

### Syntax

```python
while condition:
    # statements
```

### Example

```python
i = 1

while i <= 5:
    print(i)
    i = i + 1
```

### Output

```text
1
2
3
4
5
```

---

## 2. How Does a `while` Loop Work?

The execution happens in this order:

```text
Initialize variable
       ↓
Check condition
       ↓
Condition True?
   ↓          ↓
  Yes         No
   ↓           ↓
Execute       Exit
   ↓
Update variable
   ↓
Check condition again
```

### Example

```python
i = 1

while i <= 3:
    print(i)
    i = i + 1
```

Execution:

```text
i = 1 → print 1 → i = 2
i = 2 → print 2 → i = 3
i = 3 → print 3 → i = 4
i = 4 → condition False → stop
```

---

# 3. Print Numbers from 1 to 10

```python
i = 1

while i <= 10:
    print(i)
    i = i + 1
```

### Output

```text
1
2
3
4
5
6
7
8
9
10
```

### Important

The statement:

```python
i = i + 1
```

changes the value of `i`.

Without it, the loop can become an infinite loop.

---

# 4. Print Numbers from 10 to 1

```python
i = 10

while i >= 1:
    print(i)
    i = i - 1
```

### Output

```text
10
9
8
7
6
5
4
3
2
1
```

For an increasing loop:

```python
i = i + 1
```

For a decreasing loop:

```python
i = i - 1
```

---

# 5. Sum of Numbers from 1 to N

Suppose the user enters:

```text
5
```

We need to calculate:

```text
1 + 2 + 3 + 4 + 5 = 15
```

### Program

```python
n = int(input("Enter N: "))

i = 1
total = 0

while i <= n:
    total = total + i
    i = i + 1

print("Sum =", total)
```

### Output

```text
Enter N: 5
Sum = 15
```

---

# 6. Understanding the `total` Variable

Initially:

```python
total = 0
```

For `N = 5`:

| `i` | `total` |
|---:|---:|
| 1 | 1 |
| 2 | 3 |
| 3 | 6 |
| 4 | 10 |
| 5 | 15 |

The statement:

```python
total = total + i
```

keeps adding the current value of `i`.

---

# 7. Sum of Even Numbers

```python
n = int(input("Enter N: "))

i = 1
total = 0

while i <= n:
    if i % 2 == 0:
        total = total + i

    i = i + 1

print("Sum of even numbers =", total)
```

For:

```text
N = 10
```

The calculation is:

```text
2 + 4 + 6 + 8 + 10 = 30
```

Output:

```text
Sum of even numbers = 30
```

---

# 8. Multiplication Table

```python
num = int(input("Enter a number: "))

i = 1

while i <= 10:
    print(num, "x", i, "=", num * i)
    i = i + 1
```

### Example

```text
Enter a number: 5

5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

---

# 9. Infinite Loop

An infinite loop occurs when the condition never becomes `False`.

### Incorrect

```python
i = 1

while i <= 10:
    print(i)
```

Here, `i` never changes.

Therefore:

```text
1 <= 10
```

is always `True`.

### Correct

```python
i = 1

while i <= 10:
    print(i)
    i = i + 1
```

---

# 10. `while` vs `for`

Both loops can be used for repetition.

### `for` Loop

Usually useful when the number of iterations is known.

```python
for i in range(1, 11):
    print(i)
```

### `while` Loop

Useful when repetition depends on a condition.

```python
i = 1

while i <= 10:
    print(i)
    i = i + 1
```

### Quick Comparison

| `for` | `while` |
|---|---|
| Commonly used with sequences/ranges | Commonly used with conditions |
| Often easier for known iterations | Useful when the stopping condition is dynamic |
| Uses `range()` frequently | Requires condition management |
| Iteration is handled by the loop | Programmer usually updates the variable |

---

# 11. Factorial Using `while`

Factorial of `5`:

```text
5 × 4 × 3 × 2 × 1 = 120
```

### Program

```python
n = int(input("Enter a number: "))

i = 1
factorial = 1

while i <= n:
    factorial = factorial * i
    i = i + 1

print("Factorial =", factorial)
```

### Output

```text
Enter a number: 5
Factorial = 120
```

---

# 12. Important Operators

## Comparison Operators

```python
<     # less than
>     # greater than
<=    # less than or equal
>=    # greater than or equal
==    # equal
!=    # not equal
```

Example:

```python
i <= 10
```

---

## Increment

```python
i = i + 1
```

Short form:

```python
i += 1
```

---

## Decrement

```python
i = i - 1
```

Short form:

```python
i -= 1
```

---

# 13. Common Mistakes

### ❌ Forgetting to update the variable

```python
i = 1

while i <= 10:
    print(i)
```

This can create an infinite loop.

### ❌ Wrong indentation

```python
while i <= 10:
print(i)
```

Python requires indentation.

### ✅ Correct

```python
while i <= 10:
    print(i)
    i += 1
```

---

# 🧪 Practice Programs

Try solving these without looking at the previous examples.

### Practice 1

Print numbers from **1 to 20** using a `while` loop.

### Practice 2

Print all even numbers from **1 to 50**.

### Practice 3

Print all odd numbers from **1 to 50**.

### Practice 4

Calculate the sum:

```text
1 + 2 + 3 + ... + N
```

### Practice 5

Calculate the sum of all even numbers from `1` to `N`.

### Practice 6

Take a number from the user and print its multiplication table from `1` to `10`.

### Practice 7

Calculate the factorial of a number using a `while` loop.

---

# ⭐ Challenge Program

Write a program that asks the user for a number and prints:

- Numbers from `1` to the number
- Sum of the numbers
- Sum of even numbers
- Sum of odd numbers

### Example

```text
Enter N: 10

Numbers:
1 2 3 4 5 6 7 8 9 10

Sum = 55
Even Sum = 30
Odd Sum = 25
```

---

# 📝 Key Takeaways

Remember the basic structure:

```python
initialize

while condition:
    statements
    update
```

The four important steps are:

```text
1. Initialize
2. Check condition
3. Execute statements
4. Update variable
```

### Most Important Rule

> Always make sure your `while` loop has a way to eventually make its condition `False`.

---

## 🚀 Day 14 Summary

Today we learned:

- `while` loop
- Conditions
- Increment and decrement
- Infinite loops
- Sum using loops
- Even/odd numbers
- Multiplication tables
- Factorials
- Difference between `for` and `while`

**Next:** Continue building more practical programs using loops and conditional statements.