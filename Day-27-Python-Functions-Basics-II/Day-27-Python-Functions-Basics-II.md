# Day 27 – Python Functions: Basics II

## 📌 Topics Covered

- Functions with parameters
- Parameters vs Arguments
- `return` statement
- Creating reusable functions
- Prime number checking using functions
- Factorial using functions
- Taking user input and passing it to functions

---

## 1. Functions with Parameters

A parameter is a variable defined inside the function definition. It receives a value when the function is called.

### Example

```python
def greet(name):
    print("Hello", name)

greet("Pavan")
```

### Output

```text
Hello Pavan
```

- `name` → Parameter
- `"Pavan"` → Argument

---

## 2. Function with Multiple Parameters

A function can accept multiple parameters.

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

### Output

```text
30
```

---

## 3. `return` Statement

The `return` statement sends a value back from the function.

### Example

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

### Output

```text
30
```

### `print()` vs `return`

`print()` displays a value:

```python
def add(a, b):
    print(a + b)
```

`return` sends the value back:

```python
def add(a, b):
    return a + b
```

The returned value can be stored in a variable or used in another expression.

---

## 4. Square of a Number

```python
def square(n):
    return n * n

result = square(5)

print(result)
```

### Output

```text
25
```

---

# 5. Prime Number Using a Function

A prime number is a number greater than 1 that has exactly two factors:

- 1
- The number itself

Examples:

```text
2, 3, 5, 7, 11, 13
```

Numbers such as `1`, `4`, `6`, `8`, and `9` are not prime.

### Program

```python
def is_prime(n):
    if n <= 1:
        return False

    for i in range(2, n):
        if n % i == 0:
            return False

    return True


print(is_prime(7))
print(is_prime(10))
```

### Output

```text
True
False
```

### Explanation

```python
if n <= 1:
    return False
```

Numbers less than or equal to 1 are not prime.

```python
for i in range(2, n):
```

Checks possible divisors from 2 up to `n - 1`.

```python
if n % i == 0:
```

If the remainder is `0`, the number is divisible by `i`.

```python
return False
```

The number is not prime.

```python
return True
```

If no divisor is found, the number is prime.

---

# 6. Prime Number with User Input

```python
def is_prime(n):
    if n <= 1:
        return False

    for i in range(2, n):
        if n % i == 0:
            return False

    return True


num = int(input("Enter a number: "))

if is_prime(num):
    print("Prime number")
else:
    print("Not a prime number")
```

### Sample Output

```text
Enter a number: 17
Prime number
```

---

# 7. Factorial Using a Function

Factorial of a positive integer `n` is the product of all positive integers from `1` to `n`.

### Example

```text
5! = 5 × 4 × 3 × 2 × 1
   = 120
```

### Program

```python
def factorial(n):
    result = 1

    for i in range(1, n + 1):
        result = result * i

    return result


print(factorial(5))
```

### Output

```text
120
```

---

# 8. Factorial with User Input

```python
def factorial(n):
    result = 1

    for i in range(1, n + 1):
        result = result * i

    return result


num = int(input("Enter a number: "))

print("Factorial =", factorial(num))
```

### Sample Output

```text
Enter a number: 6
Factorial = 720
```

---

# 9. Important Concepts

| Concept | Meaning |
|---|---|
| `def` | Used to define a function |
| Parameter | Variable in the function definition |
| Argument | Actual value passed to a function |
| `return` | Sends a value back from a function |
| Function call | Executing a function |
| Reusability | Using the same function multiple times |

---

# 10. Practice Programs

## Program 1 – Cube of a Number

```python
def cube(n):
    return n * n * n

print(cube(4))
```

Output:

```text
64
```

---

## Program 2 – Check Even Number

```python
def is_even(n):
    if n % 2 == 0:
        return True
    return False

print(is_even(10))
```

Output:

```text
True
```

---

## Program 3 – Count Digits

```python
def count_digits(n):
    count = 0

    while n != 0:
        n = n // 10
        count += 1

    return count


print(count_digits(12345))
```

Output:

```text
5
```

---

## Program 4 – Print Prime Numbers from 1 to 50

```python
def is_prime(n):
    if n <= 1:
        return False

    for i in range(2, n):
        if n % i == 0:
            return False

    return True


for i in range(1, 51):
    if is_prime(i):
        print(i, end=" ")
```

### Output

```text
2 3 5 7 11 13 17 19 23 29 31 37 41 43 47
```

---

# 📝 Day 27 Practice Questions

1. Write a function to find the square of a number.
2. Write a function to find the cube of a number.
3. Write a function to check whether a number is even or odd.
4. Write a function to check whether a number is prime.
5. Write a function to calculate factorial.
6. Write a function to count the digits of a number.
7. Write a function to calculate the sum of digits.
8. Write a function to reverse a number.
9. Print all prime numbers between 1 and 100 using a function.
10. Write a function that accepts two numbers and returns the larger number.

---

# 🎯 Key Takeaways

- Functions help us write reusable code.
- Parameters allow functions to receive input.
- Arguments are the actual values passed to parameters.
- `return` sends a result back to the caller.
- Functions can contain conditions and loops.
- Complex logic such as prime checking and factorial calculation can be organized into reusable functions.

---

## 📚 Day 27 Summary

Today we learned how to create functions that accept input and return results. We also implemented practical problems such as **prime number checking** and **factorial calculation** using functions.

### Next Step

Continue practicing functions with different parameters, return values, conditions, and loops.
