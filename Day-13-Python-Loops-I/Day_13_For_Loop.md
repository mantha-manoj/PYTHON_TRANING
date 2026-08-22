# Day 13 – For Loop and range() in Python

## 📌 Learning Objectives

By the end of this lesson, you should be able to:

- Understand what loops are and why they are used.
- Use the `for` loop in Python.
- Understand the `range()` function.
- Use `range(start, stop)` and `range(start, stop, step)`.
- Print sequences of numbers.
- Generate even and odd numbers.
- Calculate squares and sums using loops.
- Create multiplication tables.
- Use counters and accumulator variables.

---

## 1. What is a Loop?

A **loop** is used to execute a block of code repeatedly.

### Without a loop

```python
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
```

### Using a loop

```python
for i in range(5):
    print("Hello")
```

A loop helps us avoid writing the same code multiple times.

---

## 2. Types of Loops in Python

Python mainly provides two types of loops:

1. `for` loop
2. `while` loop

In Day 13, we focus on the **`for` loop**.

---

# 3. `for` Loop

### Syntax

```python
for variable in sequence:
    statement
```

### Example

```python
for i in range(5):
    print(i)
```

### Output

```text
0
1
2
3
4
```

### Important

The ending value in `range()` is **not included**.

```python
range(5)
```

generates:

```text
0 1 2 3 4
```

---

# 4. `range()` Function

The `range()` function generates a sequence of numbers.

There are three commonly used forms.

## A. `range(stop)`

```python
for i in range(5):
    print(i)
```

Output:

```text
0
1
2
3
4
```

---

## B. `range(start, stop)`

```python
for i in range(1, 6):
    print(i)
```

Output:

```text
1
2
3
4
5
```

Here:

- Start = `1`
- Stop = `6`
- `6` is excluded

---

## C. `range(start, stop, step)`

```python
for i in range(1, 11, 2):
    print(i)
```

Output:

```text
1
3
5
7
9
```

Here:

- Start = `1`
- Stop = `11`
- Step = `2`

---

# 5. Reverse Loop

We can use a negative step to move backwards.

```python
for i in range(10, 0, -1):
    print(i)
```

Output:

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

---

# 6. Print Numbers from 1 to 20

```python
for i in range(1, 21):
    print(i)
```

Remember:

```python
range(1, 21)
```

includes `1` but excludes `21`.

---

# 7. Print Even Numbers

## Method 1 – Using Step

```python
for i in range(2, 21, 2):
    print(i)
```

Output:

```text
2
4
6
8
10
12
14
16
18
20
```

## Method 2 – Using Condition

```python
for i in range(1, 21):
    if i % 2 == 0:
        print(i)
```

---

# 8. Print Odd Numbers

```python
for i in range(1, 21, 2):
    print(i)
```

Output:

```text
1
3
5
7
9
11
13
15
17
19
```

---

# 9. Squares of Numbers

We can calculate the square of every number inside a loop.

```python
for i in range(1, 11):
    print(i, "=", i * i)
```

Output:

```text
1 = 1
2 = 4
3 = 9
4 = 16
5 = 25
6 = 36
7 = 49
8 = 64
9 = 81
10 = 100
```

### Using the exponent operator

```python
for i in range(1, 11):
    print(i, "=", i ** 2)
```

Both `i * i` and `i ** 2` calculate the square.

---

# 10. Multiplication Table

```python
num = int(input("Enter a number: "))

for i in range(1, 11):
    print(num, "x", i, "=", num * i)
```

### Example

Input:

```text
5
```

Output:

```text
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

### Using an f-string

```python
num = int(input("Enter a number: "))

for i in range(1, 11):
    print(f"{num} x {i} = {num * i}")
```

---

# 11. Sum of Numbers

To calculate a sum, we can use an **accumulator variable**.

```python
total = 0

for i in range(1, 11):
    total = total + i

print("Sum =", total)
```

Output:

```text
Sum = 55
```

### How it works

```text
total = 0

i = 1  → total = 1
i = 2  → total = 3
i = 3  → total = 6
...
i = 10 → total = 55
```

---

# 12. Counter Variable

A counter is used to count how many times something happens.

### Example – Count Even Numbers

```python
count = 0

for i in range(1, 21):
    if i % 2 == 0:
        count = count + 1

print("Even numbers =", count)
```

Output:

```text
Even numbers = 10
```

### Important Pattern

```python
count = 0

for i in range(...):
    if condition:
        count = count + 1
```

This pattern is useful in many programming problems.

---

# 13. Difference Between `for` and `if`

### `if`

Used to make a decision.

```python
if age >= 18:
    print("Eligible")
```

### `for`

Used to repeat code.

```python
for i in range(5):
    print("Hello")
```

### Combining Both

```python
for i in range(1, 21):
    if i % 2 == 0:
        print(i)
```

Here:

- `for` controls repetition.
- `if` checks a condition.

---

# 🧪 Practice Programs

Try solving these without looking at the examples above.

### 1. Print Numbers

Print numbers from `10` to `50`.

### 2. Even Numbers

Print all even numbers from `1` to `50`.

### 3. Odd Numbers

Print all odd numbers from `1` to `50`.

### 4. Squares

Print squares of numbers from `1` to `20`.

### 5. Multiplication Table

Take a number from the user and print its multiplication table from `1` to `20`.

### 6. Sum

Calculate the sum of numbers from `1` to `100`.

### 7. Reverse

Print numbers from `20` to `1`.

### 8. Multiples of 5

Print multiples of `5` from `5` to `100`.

---

# ⭐ Challenge Programs

## Challenge 1 – Sum from 1 to N

Take `N` from the user and calculate:

```text
1 + 2 + 3 + ... + N
```

Example:

```text
Enter N: 5
Sum = 15
```

---

## Challenge 2 – Sum of Even Numbers

Take `N` from the user and calculate the sum of all even numbers from `1` to `N`.

Example:

```text
Enter N: 10
Sum = 30
```

---

## Challenge 3 – Count Odd Numbers

Take `N` from the user and count how many odd numbers exist between `1` and `N`.

---

# 📝 Quick Quiz

### Q1. What is the output?

```python
for i in range(1, 5):
    print(i)
```

Answer:

```text
1
2
3
4
```

---

### Q2. What is the output?

```python
for i in range(2, 11, 2):
    print(i)
```

Answer:

```text
2
4
6
8
10
```

---

### Q3. What does `range(1, 10)` mean?

It starts at `1` and stops before `10`.

---

### Q4. How many times does this print `Python`?

```python
for i in range(5):
    print("Python")
```

Answer:

```text
5 times
```

---

### Q5. Find the error.

```python
for i in range(1, 5)
    print(i)
```

The `:` is missing.

Correct code:

```python
for i in range(1, 5):
    print(i)
```

---

# 🏠 Homework

Solve the following programs:

1. Print numbers from `1` to `100`.
2. Print multiples of `3` between `1` and `100`.
3. Print the multiplication table of a user-given number.
4. Calculate the sum of all even numbers from `1` to `100`.
5. Print numbers from `10` to `1`.
6. Calculate the factorial of a number using a `for` loop.
7. Count how many numbers between `1` and `100` are divisible by both `3` and `5`.

---

# 🎯 Key Points to Remember

```text
for loop → used for repetition

range(stop)
→ starts from 0
→ stops before stop

range(start, stop)
→ starts from start
→ stops before stop

range(start, stop, step)
→ controls the increment/decrement

range(1, 11)
→ 1 to 10

range(10, 0, -1)
→ 10 to 1
```

### Most Important Syntax

```python
for i in range(start, stop, step):
    # code
```

---

## 📚 Day 13 Summary

Today we learned:

- Loops
- `for` loop
- `range()`
- Start and stop values
- Step value
- Reverse loops
- Even and odd numbers
- Squares
- Multiplication tables
- Accumulator variables
- Counter variables
- Combining `for` with `if`

