# Day 37 – Exception Handling II

## Topic
Multiple `except`, `else`, `finally` and Safe Calculator

## Learning Objectives
- Understand multiple `except` blocks.
- Use `else` when no exception occurs.
- Use `finally` for code that must always execute.
- Build a safe calculator.

## 1. Multiple except
```python
try:
    a = int(input("Enter first number: "))
    b = int(input("Enter second number: "))
    print(a / b)
except ValueError:
    print("Enter numbers only")
except ZeroDivisionError:
    print("Cannot divide by zero")
```

## 2. else
`else` runs only when the `try` block completes without an exception.

```python
try:
    a = int(input("Enter a number: "))
    b = int(input("Enter another number: "))
    result = a / b
except ZeroDivisionError:
    print("Cannot divide by zero")
else:
    print("Result:", result)
```

## 3. finally
`finally` runs whether an exception occurs or not.

```python
try:
    print("Program started")
except:
    print("Error occurred")
finally:
    print("Program completed")
```

## 4. Safe Calculator
```python
try:
    a = float(input("Enter first number: "))
    b = float(input("Enter second number: "))
    operator = input("Enter operator (+, -, *, /): ")

    if operator == "+":
        result = a + b
    elif operator == "-":
        result = a - b
    elif operator == "*":
        result = a * b
    elif operator == "/":
        result = a / b
    else:
        print("Invalid operator")
        result = None

except ValueError:
    print("Please enter valid numbers")
except ZeroDivisionError:
    print("Cannot divide by zero")
else:
    if result is not None:
        print("Result:", result)
finally:
    print("Calculator closed")
```

## Practice
1. Handle `ValueError` and `IndexError`.
2. Handle `ValueError` and `KeyError`.
3. Create a calculator using `try`, `except`, `else`, and `finally`.
4. Add `%`, `//`, and `**` operations.
5. Make the calculator repeat until the user enters `exit`.

## Homework
Create a program that safely accepts two numbers and an operator and handles invalid input, division by zero, and invalid operators.
