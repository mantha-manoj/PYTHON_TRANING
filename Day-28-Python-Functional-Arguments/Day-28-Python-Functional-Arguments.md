# Day 28 – Python Function Arguments

## 📌 Topics Covered

- Function parameters and arguments
- Positional arguments
- Keyword arguments
- Default arguments
- Variable-length arguments using `*args`
- Combining positional and keyword arguments

## 🎯 Learning Objectives

By the end of Day 28, students should be able to:

- Understand parameters and arguments.
- Use positional and keyword arguments.
- Use default argument values.
- Accept multiple positional arguments with `*args`.
- Build reusable functions using different argument types.

---

## 1. Parameters and Arguments

A **parameter** is a variable defined in a function. An **argument** is the actual value passed when calling the function.

```python
def greet(name):
    print("Hello", name)

greet("Pavan")
```

Output:

```text
Hello Pavan
```

Here:
- `name` → Parameter
- `"Pavan"` → Argument

---

## 2. Positional Arguments

Values are assigned according to their position.

```python
def student(name, age):
    print("Name:", name)
    print("Age:", age)

student("Pavan", 24)
```

Output:

```text
Name: Pavan
Age: 24
```

The order matters:

```python
student("Rahul", 22)
```

Here `name = "Rahul"` and `age = 22`.

---

## 3. Keyword Arguments

The parameter name is specified while passing the value.

```python
def student(name, age):
    print("Name:", name)
    print("Age:", age)

student(age=24, name="Pavan")
```

Output:

```text
Name: Pavan
Age: 24
```

The order does not matter because parameter names are specified.

---

## 4. Positional vs Keyword Arguments

### Positional

```python
student("Pavan", 24)
```

### Keyword

```python
student(name="Pavan", age=24)
```

Both produce the same result.

---

## 5. Default Arguments

A default argument already has a value. If no value is supplied, Python uses the default.

```python
def greet(name="Guest"):
    print("Hello", name)

greet()
```

Output:

```text
Hello Guest
```

Providing a value replaces the default:

```python
greet("Pavan")
```

Output:

```text
Hello Pavan
```

### Example

```python
def student(name, branch="CSE"):
    print("Name:", name)
    print("Branch:", branch)

student("Pavan")
```

Output:

```text
Name: Pavan
Branch: CSE
```

---

## 6. `*args`

Use `*args` when a function should accept a variable number of positional arguments.

```python
def add(*numbers):
    total = 0

    for n in numbers:
        total += n

    return total

print(add(10, 20))
print(add(10, 20, 30))
print(add(10, 20, 30, 40))
```

Output:

```text
30
60
100
```

Inside the function, `args` is stored as a tuple.

```python
def display(*args):
    print(args)

display(10, 20, 30)
```

Output:

```text
(10, 20, 30)
```

---

## 7. Using `sum()` with `*args`

```python
def add(*numbers):
    return sum(numbers)

print(add(10, 20, 30))
```

Output:

```text
60
```

---

## 8. Practical Student Example

```python
def student(name, age=18, *marks):
    print("Name:", name)
    print("Age:", age)

    if marks:
        print("Marks:", marks)
        print("Total:", sum(marks))

student("Pavan", 24, 80, 85, 90)
```

Output:

```text
Name: Pavan
Age: 24
Marks: (80, 85, 90)
Total: 255
```

---

## 9. Combining Positional and Keyword Arguments

Positional arguments should come before keyword arguments.

### Correct

```python
def student(name, age, branch):
    print(name, age, branch)

student("Pavan", age=24, branch="CSE")
```

### Incorrect

```python
student(name="Pavan", 24, branch="CSE")
```

---

# 💻 Practice Programs

## Program 1 – Calculate Two Numbers

```python
def calculate(a, b):
    print("Addition:", a + b)
    print("Subtraction:", a - b)
    print("Multiplication:", a * b)
    print("Division:", a / b)

calculate(20, 10)
```

## Program 2 – Employee Details Using Keyword Arguments

```python
def employee(name, salary, department):
    print("Name:", name)
    print("Salary:", salary)
    print("Department:", department)

employee(
    department="IT",
    salary=50000,
    name="Rahul"
)
```

## Program 3 – Default Argument

```python
def greet(name="Guest"):
    print("Hello", name)

greet()
greet("Pavan")
```

Output:

```text
Hello Guest
Hello Pavan
```

## Program 4 – Sum Using `*args`

```python
def add(*numbers):
    return sum(numbers)

print(add(10, 20, 30))
```

Output:

```text
60
```

## Program 5 – Maximum Using `*args`

```python
def maximum(*numbers):
    return max(numbers)

print(maximum(10, 50, 30, 90, 20))
```

Output:

```text
90
```

## Program 6 – Average Using `*args`

```python
def calculate_average(*marks):
    return sum(marks) / len(marks)

print(calculate_average(80, 90, 70, 60))
```

Output:

```text
75.0
```

---

# 📝 Practice Questions

1. Create a function using positional arguments to add two numbers.
2. Create a function using keyword arguments to display student details.
3. Create a function with a default argument for country name.
4. Create a function using `*args` to calculate the sum.
5. Create a function using `*args` to find the maximum number.
6. Create a function using `*args` to find the minimum number.
7. Create a function using `*args` to calculate average marks.
8. Create a function that accepts student name, age, branch and multiple marks.
9. Create a function using keyword arguments to calculate an employee's annual salary.
10. Create a function using `*args` to count how many numbers were passed.

---

# 🧠 Quick Quiz

### 1. What is a positional argument?

A. Argument passed using the parameter name  
B. Argument passed according to position  
C. Default value  
D. Return value

**Answer: B**

### 2. Which syntax is used for variable-length positional arguments?

A. `#args`  
B. `**args`  
C. `*args`  
D. `args*`

**Answer: C**

### 3. What is the output?

```python
def greet(name="Guest"):
    print("Hello", name)

greet()
```

**Answer:**

```text
Hello Guest
```

### 4. What is the output?

```python
def add(*numbers):
    return sum(numbers)

print(add(10, 20, 30))
```

**Answer:**

```text
60
```

### 5. Parameter vs Argument

**Parameter:** Variable defined in the function definition.

**Argument:** Actual value passed to the function.

---

# 🎯 Key Takeaways

```text
Positional Arguments
        ↓
Values are assigned according to position

Keyword Arguments
        ↓
Values are assigned using parameter names

Default Arguments
        ↓
Parameter has a default value

*args
        ↓
Accepts multiple positional arguments
```

### Important Syntax

```python
def function(a, b):
    pass
```

```python
def function(name="Guest"):
    pass
```

```python
def function(*args):
    pass
```

---

## 📚 Day 28 Summary

In Day 28, we learned how to pass different types of arguments to Python functions:

- Positional arguments
- Keyword arguments
- Default arguments
- Variable-length arguments using `*args`
- Parameters vs arguments
- Combining positional and keyword arguments

These concepts make Python functions more flexible and reusable.
