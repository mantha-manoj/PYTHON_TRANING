# Day 36 – Exception Handling – I

## Topics Covered
- What is an exception?
- `try`
- `except`
- `ZeroDivisionError`
- `ValueError`
- Handling multiple exceptions

## 1. What is an Exception?
An exception is an error that occurs while a program is running.

Example:

```python
a = 10
b = 0
print(a / b)
```

This causes `ZeroDivisionError`.

## 2. try-except

```python
try:
    a = 10
    b = 0
    print(a / b)
except:
    print("Something went wrong")
```

## 3. ZeroDivisionError

```python
try:
    a = int(input("Enter number: "))
    b = int(input("Enter divisor: "))
    print(a / b)
except ZeroDivisionError:
    print("Cannot divide by zero")
```

## 4. ValueError

```python
try:
    num = int(input("Enter a number: "))
    print(num)
except ValueError:
    print("Please enter a valid number")
```

## 5. Handling Multiple Exceptions

```python
try:
    a = int(input("Enter first number: "))
    b = int(input("Enter second number: "))
    print("Result:", a / b)

except ValueError:
    print("Please enter numbers only")

except ZeroDivisionError:
    print("Cannot divide by zero")
```

## Practice Programs
1. Create a division program with exception handling.
2. Handle invalid integer input.
3. Create a calculator using `try-except`.
4. Ask for age and handle invalid input.

## Quick Revision
- `try` contains risky code.
- `except` handles exceptions.
- `ValueError` occurs when a value has an invalid type/format for the operation.
- `ZeroDivisionError` occurs when dividing by zero.
