# Day 38 – Custom Exceptions

## Topic
Creating and Raising Your Own Exceptions

## Learning Objectives
- Understand custom exceptions.
- Use the `raise` statement.
- Create an exception class.
- Handle custom exceptions using `try-except`.

## 1. The raise statement
`raise` is used to intentionally generate an exception.

```python
age = int(input("Enter age: "))

if age < 18:
    raise Exception("Age must be 18 or above")

print("Eligible")
```

## 2. Creating a custom exception
```python
class InvalidAgeError(Exception):
    pass
```

## 3. Handling a custom exception
```python
class InvalidAgeError(Exception):
    pass

try:
    age = int(input("Enter your age: "))

    if age < 18:
        raise InvalidAgeError("Age must be 18 or above")

    print("You are eligible")

except InvalidAgeError as e:
    print("Error:", e)
```

## 4. Complete Age Validation Program
```python
class InvalidAgeError(Exception):
    pass

try:
    age = int(input("Enter your age: "))

    if age < 0:
        raise InvalidAgeError("Age cannot be negative")

    if age < 18:
        raise InvalidAgeError("You must be 18 or above")

    print("You are eligible to vote.")

except ValueError:
    print("Please enter a valid number.")
except InvalidAgeError as e:
    print("Error:", e)
finally:
    print("Program completed.")
```

## Practice 1 – Invalid Marks
Create `InvalidMarksError` and raise it when marks are below 0 or above 100.

## Practice 2 – Bank Account
Create `InsufficientBalanceError` and raise it when withdrawal is greater than the balance.

## Practice 3 – Password
Create `InvalidPasswordError` and raise it when the password has fewer than 8 characters.

## Homework
Create a Bank Account program with:
- `deposit()`
- `withdraw()`
- `InsufficientBalanceError`
- `try-except`
- `finally`

## Key Syntax
```python
class MyException(Exception):
    pass

try:
    if condition:
        raise MyException("Something went wrong")
except MyException as e:
    print(e)
```
