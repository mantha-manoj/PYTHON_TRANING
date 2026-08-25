# Day 15 — Loop Control Statements in Python

## 📚 Topics Covered

Today we will learn how to control the execution of loops using:

- `break`
- `continue`
- `pass`

These statements are useful when we need to change the normal flow of a `for` or `while` loop.

---

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Understand why loop-control statements are required.
- Use `break` to terminate a loop.
- Use `continue` to skip an iteration.
- Use `pass` as a placeholder.
- Combine `break` and `continue` with `if` conditions.
- Use loop-control statements in practical programs.

---

# 1. `break` Statement

The `break` statement is used to **immediately terminate a loop**.

When Python executes `break`, the loop stops and execution continues with the statement after the loop.

## Syntax

```python
break
```

## Example

```python
for i in range(1, 11):
    print(i)

    if i == 5:
        break
```

### Output

```text
1
2
3
4
5
```

When `i` becomes `5`, `break` terminates the loop.

### Execution Flow

```text
1 → print
2 → print
3 → print
4 → print
5 → print → break
```

The values `6` through `10` are never executed.

---

# 2. `break` with a Condition

`break` is commonly used with `if`.

```python
for i in range(1, 21):

    if i == 10:
        break

    print(i)
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
```

Here, the loop stops before printing `10`.

---

# 3. Searching Using `break`

`break` is very useful when searching for a value.

```python
numbers = [10, 20, 30, 40, 50]

for number in numbers:

    if number == 30:
        print("Number found")
        break

    print(number)
```

### Output

```text
10
20
Number found
```

Once `30` is found, there is no need to continue searching, so `break` terminates the loop.

---

# 4. `continue` Statement

The `continue` statement is used to **skip the current iteration** of a loop.

It does **not** terminate the loop.

After `continue`, Python immediately moves to the next iteration.

## Syntax

```python
continue
```

## Example

```python
for i in range(1, 11):

    if i == 5:
        continue

    print(i)
```

### Output

```text
1
2
3
4
6
7
8
9
10
```

The number `5` is skipped, but the loop continues.

---

# 5. `continue` with Multiples

We can use the `%` operator with `continue`.

### Example: Skip multiples of 3

```python
for i in range(1, 21):

    if i % 3 == 0:
        continue

    print(i)
```

### Output

```text
1
2
4
5
7
8
10
11
13
14
16
17
19
20
```

### Why?

The condition:

```python
i % 3 == 0
```

checks whether `i` is divisible by `3`.

For example:

```text
3 % 3  = 0
6 % 3  = 0
9 % 3  = 0
12 % 3 = 0
```

These values are skipped.

---

# 6. `break` vs `continue`

| Statement | Purpose | Loop Continues? |
|---|---|---|
| `break` | Terminates the loop | ❌ No |
| `continue` | Skips current iteration | ✅ Yes |
| `pass` | Does nothing | ✅ Yes |

### Easy way to remember

```text
break     → EXIT
continue  → SKIP
pass      → DO NOTHING
```

---

# 7. Using `break` and `continue` Together

We can use both statements in the same loop.

### Problem

Print numbers from `1` to `20`.

Rules:

- Skip multiples of `3`.
- Stop when the number reaches `15`.

```python
for i in range(1, 21):

    if i == 15:
        break

    if i % 3 == 0:
        continue

    print(i)
```

### Output

```text
1
2
4
5
7
8
10
11
13
14
```

### Explanation

When the value is:

```text
3  → continue
6  → continue
9  → continue
12 → continue
15 → break
```

---

# 8. `pass` Statement

The `pass` statement is a **placeholder**.

It tells Python:

> "Do nothing for now."

It is useful when we want to create a block of code but haven't written its implementation yet.

## Example

```python
for i in range(1, 6):

    if i == 3:
        pass

    print(i)
```

### Output

```text
1
2
3
4
5
```

`pass` does not stop or skip the loop.

---

# 9. Difference Between `break`, `continue`, and `pass`

Consider:

```python
for i in range(1, 6):

    if i == 3:
        break

    print(i)
```

Output:

```text
1
2
```

Because `break` terminates the loop.

---

Now:

```python
for i in range(1, 6):

    if i == 3:
        continue

    print(i)
```

Output:

```text
1
2
4
5
```

Because `continue` skips `3`.

---

Now:

```python
for i in range(1, 6):

    if i == 3:
        pass

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

Because `pass` does nothing.

---

# 10. Practical Example — Password Attempts

```python
correct_password = "python123"

for attempt in range(1, 4):

    password = input("Enter password: ")

    if password == correct_password:
        print("Login successful")
        break

    print("Wrong password")
```

### Why use `break`?

Once the correct password is entered, we don't need additional attempts.

---

# 11. Practical Example — Skip Even Numbers

```python
for i in range(1, 11):

    if i % 2 == 0:
        continue

    print(i)
```

### Output

```text
1
3
5
7
9
```

The even numbers are skipped.

---

# 12. Practical Example — Search for a Student

```python
students = ["Ravi", "Rahul", "Pavan", "Anil"]

search = input("Enter student name: ")

for student in students:

    if student == search:
        print("Student found")
        break
else:
    print("Student not found")
```

Here, `break` stops the search once the student is found.

---

# 13. Important `range()` Reminder

Remember:

```python
range(start, stop)
```

The `stop` value is **not included**.

Example:

```python
range(1, 6)
```

produces:

```text
1 2 3 4 5
```

---

# 14. Final Challenge — Number Analyzer

Write a program that prints numbers from `1` to `50`.

### Rules

1. Skip numbers divisible by `3`.
2. Stop when the number reaches `40`.
3. Print all other numbers.

### Starter Code

```python
for i in range(1, 51):

    # Stop at 40

    # Skip multiples of 3

    # Print number
```

### Solution

```python
for i in range(1, 51):

    if i == 40:
        break

    if i % 3 == 0:
        continue

    print(i)
```

---

# 📝 Practice Programs

## Practice 1 — Skip Multiples of 5

Print numbers from `1` to `50`, but skip numbers divisible by `5`.

**Concept:** `continue`

---

## Practice 2 — Stop at 20

Print numbers from `1` to `30`, but stop when the number reaches `20`.

**Concept:** `break`

---

## Practice 3 — Number Search

Given:

```python
numbers = [10, 25, 30, 45, 50]
```

Ask the user to enter a number.

If the number exists, print:

```text
Number found
```

Use `break`.

---

## Practice 4 — Skip Even Numbers

Print numbers from `1` to `30`, but skip all even numbers.

**Concept:** `continue`

---

## Practice 5 — Find First Multiple of 7

Print numbers from `1` to `100` and stop at the first number divisible by `7`.

**Concept:** `break`

---

# 🎤 Interview Questions

### 1. What is `break`?

`break` immediately terminates the loop.

### 2. What is `continue`?

`continue` skips the current iteration and moves to the next iteration.

### 3. Does `continue` terminate a loop?

No. It only skips the current iteration.

### 4. What is `pass`?

`pass` is a placeholder statement that performs no operation.

### 5. What is the difference between `break` and `continue`?

```text
break    → terminates the loop
continue → skips the current iteration
```

### 6. What is the purpose of `pass`?

It is used when Python requires a statement but we don't want to execute any operation yet.

### 7. Can `break` be used with a `for` loop?

Yes.

### 8. Can `break` be used with a `while` loop?

Yes.

### 9. Can `continue` be used with a `for` loop?

Yes.

### 10. Can `continue` be used with a `while` loop?

Yes.

---

# 🧠 Quick Revision

```text
break
  ↓
Stops the entire loop


continue
  ↓
Skips current iteration


pass
  ↓
Does nothing
```

## Remember

```python
break
```

**Stop**

```python
continue
```

**Skip**

```python
pass
```

**Do nothing**

```
import random

print("=" * 40)

print("       GUESS THE NUMBER GAME")

print("=" * 40)

random_number = random.randint(1,100)

user_name = input("Enter your name: ")

print("Your name : ", user_name)

for attempt in range(1, 11):

    guess_number = int(input("Enter your guess number : "))

    if guess_number == random_number:

        print("Congratulations! You guessed correctly.")
        break

    elif guess_number < random_number:

        print("Too Low!")

    else:

        print("Too High!")

print("The number was:", random_number)
```

---

# 🚀 Day 15 Summary

Today we learned:

- `break`
- `continue`
- `pass`
- Loop control with `if`
- Searching using `break`
- Skipping values using `continue`
- Combining `break` and `continue`
- Practical loop-control programs

### Next Step

Practice the programs without looking at the solutions. The goal is to understand **when to use `break`, `continue`, and `pass`**, not just memorize the syntax.
