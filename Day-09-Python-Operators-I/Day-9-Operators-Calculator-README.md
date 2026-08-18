# Day 9 – Operators – I

## 📅 Date
**18 August 2026**

## 🎯 Today's Topic
**Operators – I**

Today we learned Python arithmetic operators and created a simple calculator using the topics covered from Day 1 to Day 9.

---

## 📚 Topics Covered

### 1. Arithmetic Operators

| Operator | Name | Example | Result |
|---|---|---:|---:|
| `+` | Addition | `10 + 3` | `13` |
| `-` | Subtraction | `10 - 3` | `7` |
| `*` | Multiplication | `10 * 3` | `30` |
| `/` | Division | `10 / 3` | `3.333...` |
| `%` | Modulus / Remainder | `10 % 3` | `1` |
| `//` | Floor Division | `10 // 3` | `3` |
| `**` | Exponent / Power | `10 ** 3` | `1000` |

---

## 🔹 Important Concepts

### `/` – Division

Returns the normal division result.

```python
print(10 / 3)
```

Output:

```text
3.3333333333333335
```

### `//` – Floor Division

Returns the floor value of the division.

```python
print(10 // 3)
```

Output:

```text
3
```

### `%` – Modulus

Returns the remainder.

```python
print(10 % 3)
```

Output:

```text
1
```

### `**` – Exponent

Used to calculate powers.

```python
print(2 ** 3)
```

Output:

```text
8
```

---

# 🧮 Day-9 Mini Project: Simple Calculator

This calculator uses the concepts learned so far:

- `print()`
- `input()`
- Variables
- Data types
- Type conversion
- Arithmetic operators

## Program

```python
print("========== SIMPLE CALCULATOR ==========")

num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

print("\n----- CALCULATOR RESULTS -----")

print("Addition       :", num1 + num2)
print("Subtraction    :", num1 - num2)
print("Multiplication :", num1 * num2)
print("Division       :", num1 / num2)
print("Modulus        :", num1 % num2)
print("Floor Division :", num1 // num2)
print("Power          :", num1 ** num2)

print("======================================")
```

---

## 🧪 Example

### Input

```text
Enter first number: 20
Enter second number: 3
```

### Output

```text
----- CALCULATOR RESULTS -----

Addition       : 23.0
Subtraction    : 17.0
Multiplication : 60.0
Division       : 6.666666666666667
Modulus        : 2.0
Floor Division : 6.0
Power          : 8000.0
```

---

# 🔍 Understanding the Calculator

### Taking input

```python
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
```

`input()` takes input as a string.

`float()` converts the input into a floating-point number.

Example:

```text
"10.5" → 10.5
 string    float
```

### Performing calculations

```python
num1 + num2
num1 - num2
num1 * num2
num1 / num2
num1 % num2
num1 // num2
num1 ** num2
```

Each expression uses one arithmetic operator.

---

# 📌 Operator Precedence

Python follows an order when multiple operators are used.

Basic order:

```text
()
**
*  /  //  %
+  -
```

Example:

```python
result = 10 + 5 * 2
print(result)
```

Output:

```text
20
```

Because multiplication happens before addition.

Using brackets:

```python
result = (10 + 5) * 2
print(result)
```

Output:

```text
30
```

---

# 🎓 Interview Questions

### 1. What is an operator?

An operator is a symbol used to perform an operation on values.

### 2. What is the difference between `/` and `//`?

`/` performs normal division, while `//` performs floor division.

### 3. What does `%` return?

It returns the remainder of a division.

### 4. What does `**` do?

It performs exponentiation (power).

### 5. What type does `input()` return?

`input()` returns a **string**.

### 6. Why do we use `float(input())` in the calculator?

Because `input()` returns a string and we need to convert it into a numeric value before performing arithmetic operations.

---

# 📝 Practice Programs

1. Take two numbers and perform all seven arithmetic operations.
2. Take length and breadth and calculate the area of a rectangle.
3. Take a number and print its square and cube.
4. Take total chocolates and number of students. Find chocolates per student using `//` and remaining chocolates using `%`.
5. Create a calculator that takes two numbers and displays all seven arithmetic results.

---

# ⚠️ Topics Not Yet Covered

At Day 9, avoid using concepts that are scheduled for later lessons, such as:

- `if`
- `elif`
- `else`
- Comparison operators
- Logical operators
- Loops
- Functions

The Day-9 calculator is intentionally built using only the concepts covered up to Day 9.

---

# ✅ Day-9 Takeaways

By the end of Day 9, you should be able to:

- Understand arithmetic operators.
- Use `+`, `-`, `*`, `/`, `%`, `//`, and `**`.
- Take numeric input from users.
- Convert input using `float()`.
- Store values in variables.
- Build a basic calculator.
- Understand basic operator precedence.

---

## 🚀 Next Step

Practice the calculator without looking at the solution and try to write it from scratch.

**Day 9 completed! 🎉**
