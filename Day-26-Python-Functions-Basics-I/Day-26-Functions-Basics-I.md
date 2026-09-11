# Day 26 — Python Functions: Basics I

## 📚 Topic

**Functions – Basics I**

**Duration:** 1 Hour 30 Minutes

**Main Program:** Calculator using functions — `add()`, `subtract()`, `multiply()`, and `divide()`.

---

## 🎯 Learning Objectives

By the end of this lesson, you should be able to:

- Understand what a function is.
- Create a function using `def`.
- Call a function.
- Understand parameters and arguments.
- Use the `return` statement.
- Understand the difference between `print()` and `return`.
- Create reusable calculator functions.
- Handle division by zero.
- Understand local variables.

---

# 1. What is a Function?

A **function** is a reusable block of code that performs a specific task.

Instead of writing the same code multiple times, we write it once inside a function and call it whenever required.

### Example

```python
def greet():
    print("Hello, Python!")

greet()
```

Output:

```text
Hello, Python!
```

---

# 2. Why Do We Use Functions?

Functions provide:

- **Code reusability**
- **Less code repetition**
- **Better organization**
- **Easy debugging**
- **Easy maintenance**
- **Improved readability**

Think of a function like a machine:

```text
Input → Function → Output
```

Example:

```text
10, 20 → add() → 30
```

---

# 3. Creating a Function

We use the `def` keyword to define a function.

### Syntax

```python
def function_name():
    # code
```

### Example

```python
def welcome():
    print("Welcome to Python")
```

Defining a function does not execute it.

We must call the function:

```python
welcome()
```

Output:

```text
Welcome to Python
```

---

# 4. Function Definition vs Function Call

### Function Definition

```python
def greet():
    print("Hello")
```

This creates the function.

### Function Call

```python
greet()
```

This executes the function.

### Remember

```text
def → create/define the function
function() → call/execute the function
```

---

# 5. Function Without Parameters

A function does not always need input.

```python
def welcome():
    print("Welcome to Python")

welcome()
```

Output:

```text
Welcome to Python
```

---

# 6. Function With Parameters

A **parameter** is a variable that receives a value when the function is called.

```python
def greet(name):
    print("Hello", name)
```

Call the function:

```python
greet("Rahul")
```

Output:

```text
Hello Rahul
```

Here:

```text
name → parameter
"Rahul" → argument
```

---

# 7. Parameters vs Arguments

This is an important interview question.

```python
def add(a, b):
    return a + b
```

Here:

```text
a and b → parameters
```

When we call:

```python
add(10, 20)
```

Here:

```text
10 and 20 → arguments
```

### Easy way to remember

**Parameter:** variable written in the function definition.

**Argument:** actual value passed during the function call.

---

# 8. Function With Multiple Parameters

A function can have multiple parameters.

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

Output:

```text
30
```

Another example:

```python
def student_info(name, age):
    print("Name:", name)
    print("Age:", age)

student_info("Rahul", 20)
```

Output:

```text
Name: Rahul
Age: 20
```

---

# 9. The `return` Statement ⭐

The `return` statement sends a result back to the place where the function was called.

```python
def add(a, b):
    return a + b
```

Now we can store the returned result:

```python
result = add(10, 20)

print(result)
```

Output:

```text
30
```

### Function flow

```text
add(10, 20)
     ↓
  10 + 20
     ↓
   return 30
     ↓
  result = 30
```

---

# 10. `print()` vs `return`

This is one of the most important concepts in functions.

## Using `print()`

```python
def add(a, b):
    print(a + b)
```

This displays the result.

## Using `return`

```python
def add(a, b):
    return a + b
```

This sends the result back so it can be stored or used later.

Example:

```python
result = add(10, 20)

print(result)
```

We can also perform another operation:

```python
result = add(10, 20) * 2

print(result)
```

Output:

```text
60
```

### Simple Difference

```text
print()  → displays a value
return   → sends a value back
```

---

# 11. Addition Function

```python
def add(a, b):
    return a + b

result = add(10, 20)

print("Addition:", result)
```

Output:

```text
Addition: 30
```

---

# 12. Subtraction Function

```python
def subtract(a, b):
    return a - b

result = subtract(20, 10)

print("Subtraction:", result)
```

Output:

```text
Subtraction: 10
```

---

# 13. Multiplication Function

```python
def multiply(a, b):
    return a * b

result = multiply(10, 5)

print("Multiplication:", result)
```

Output:

```text
Multiplication: 50
```

---

# 14. Division Function

```python
def divide(a, b):
    return a / b

result = divide(20, 5)

print("Division:", result)
```

Output:

```text
Division: 4.0
```

---

# 15. Handling Division by Zero ⚠️

Dividing by zero causes an error.

```python
10 / 0
```

Python raises:

```text
ZeroDivisionError
```

We can handle it inside our function:

```python
def divide(a, b):
    if b == 0:
        return "Cannot divide by zero"

    return a / b
```

Example:

```python
print(divide(10, 0))
```

Output:

```text
Cannot divide by zero
```

---

# 16. Complete Calculator Using Functions ⭐

This is the main program for Day 26.

```python
def add(a, b):
    return a + b


def subtract(a, b):
    return a - b


def multiply(a, b):
    return a * b


def divide(a, b):
    if b == 0:
        return "Cannot divide by zero"

    return a / b


num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

print("Addition:", add(num1, num2))
print("Subtraction:", subtract(num1, num2))
print("Multiplication:", multiply(num1, num2))
print("Division:", divide(num1, num2))
```

### Example Output

```text
Enter first number: 20
Enter second number: 5

Addition: 25.0
Subtraction: 15.0
Multiplication: 100.0
Division: 4.0
```

---

# 17. How the Calculator Works

First, we define four functions:

```text
add()
subtract()
multiply()
divide()
```

Then we get input:

```python
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
```

Suppose:

```text
num1 = 20
num2 = 5
```

When we write:

```python
add(num1, num2)
```

Python executes:

```python
add(20, 5)
```

Inside the function:

```python
return 20 + 5
```

The result is:

```text
25
```

The same idea applies to the other functions.

---

# 18. Multiple Calls to the Same Function

A major advantage of functions is that we can reuse them.

```python
def add(a, b):
    return a + b

print(add(10, 20))
print(add(100, 200))
print(add(5, 15))
```

Output:

```text
30
300
20
```

We wrote the function only once.

---

# 19. Local Variables

A variable created inside a function is generally **local to that function**.

```python
def test():
    message = "Hello"
    print(message)

test()
```

`message` belongs to the function's local scope.

Trying to access it outside:

```python
print(message)
```

will cause a `NameError`.

### Simple idea

```text
Inside function → local variable
Outside function → cannot directly access that local variable
```

---

# 20. Example — Greeting Function

```python
def greet(name):
    return "Hello " + name


name = input("Enter your name: ")

print(greet(name))
```

Example:

```text
Enter your name: Pavan
Hello Pavan
```

---

# 21. Example — Even or Odd

```python
def check_even_odd(number):

    if number % 2 == 0:
        return "Even"
    else:
        return "Odd"


number = int(input("Enter a number: "))

print(check_even_odd(number))
```

Example:

```text
Enter a number: 15
Odd
```

---

# 22. Example — Square

```python
def square(number):
    return number * number


number = int(input("Enter a number: "))

print("Square:", square(number))
```

Example:

```text
Enter a number: 7
Square: 49
```

---

# 23. Practice Programs

## Practice 1 — Cube

Create:

```python
def cube(number):
    return number * number * number
```

Example:

```text
Input: 5
Output: 125
```

---

## Practice 2 — Largest Number

Create:

```python
def largest(a, b):
    if a > b:
        return a
    else:
        return b
```

Example:

```python
print(largest(10, 25))
```

Output:

```text
25
```

---

## Practice 3 — Percentage

Create:

```python
def calculate_percentage(total, obtained):
    return (obtained / total) * 100
```

Example:

```python
print(calculate_percentage(500, 425))
```

Output:

```text
85.0
```

---

# 24. ⭐ Challenge — Menu-Based Calculator

Create a calculator with:

```text
1. Addition
2. Subtraction
3. Multiplication
4. Division
```

Take the user's choice and two numbers.

Use separate functions:

```python
add()
subtract()
multiply()
divide()
```

The program should display the appropriate result based on the user's choice.

### Concepts Used

- Functions
- Parameters
- Arguments
- `return`
- `input()`
- `if-elif-else`
- Arithmetic operators

---

# 🧠 Day-26 Key Points

### 1. Define a function

```python
def greet():
    print("Hello")
```

### 2. Call a function

```python
greet()
```

### 3. Use parameters

```python
def greet(name):
    print("Hello", name)
```

### 4. Pass arguments

```python
greet("Pavan")
```

### 5. Return a result

```python
def add(a, b):
    return a + b
```

---

# 📌 Important Syntax

```python
def function_name(parameters):
    # statements
    return result
```

Example:

```python
def add(a, b):
    return a + b
```

---

# ❓ Viva / Interview Questions

1. What is a function?
2. Why do we use functions?
3. Which keyword is used to define a function?
4. What is a function call?
5. What is a parameter?
6. What is an argument?
7. What is the difference between a parameter and an argument?
8. What is the purpose of `return`?
9. What is the difference between `print()` and `return`?
10. Can a function be called multiple times?
11. What happens when a function has no `return` statement?
12. What is a local variable?
13. Why should we handle division by zero?
14. What is code reusability?

---

# 📝 Homework

Create the following functions:

```python
add(a, b)
subtract(a, b)
multiply(a, b)
divide(a, b)
square(n)
cube(n)
is_even(n)
```

Take values from the user and call each function.

### Bonus

Create a **menu-based calculator** using the four calculator functions.

---

# 🔄 Day-26 Summary

Today you learned the basics of Python functions.

The most important pattern is:

```python
def function_name(parameters):
    # logic
    return result
```

For example:

```python
def add(a, b):
    return a + b
```

### Remember

```text
def      → defines a function
()       → parameters/arguments
function() → calls the function
return   → sends a result back
```

---

**Previous:** Day 25 — Dictionaries II  
**Next:** Day 27 — Functions Basics II
