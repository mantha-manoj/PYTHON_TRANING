# 🐍 Day 31 – Python Modules II

## 📌 Overview
On Day 31, we learned about Python Modules II, focusing mainly on the built-in `math` and `random` modules.

## 🎯 Learning Objectives
- Understand Python modules
- Import built-in modules
- Use the `math` module
- Use the `random` module
- Build simple programs using modules

## 1. What is a Module?
A module is a Python file containing functions, variables, classes, or reusable code.

```python
import math
print(math.sqrt(25))
```

Output:
```text
5.0
```

## 2. The `math` Module
Common functions:
- `math.sqrt()` – square root
- `math.pow()` – power
- `math.ceil()` – round upward
- `math.floor()` – round downward
- `math.factorial()` – factorial
- `math.fabs()` – absolute value
- `math.pi` – π

### Examples
```python
import math

print(math.sqrt(25))
print(math.pow(2, 3))
print(math.ceil(4.2))
print(math.floor(4.8))
print(math.factorial(5))
```

## 3. The `random` Module
Common functions:
- `random.random()` – random float between 0 and 1
- `random.randint()` – random integer
- `random.randrange()` – random number from a range
- `random.choice()` – random item
- `random.shuffle()` – shuffle a list

### Examples
```python
import random

print(random.random())
print(random.randint(1, 10))

names = ["Pavan", "Rahul", "Anil", "Kiran"]
print(random.choice(names))

numbers = [1, 2, 3, 4, 5]
random.shuffle(numbers)
print(numbers)
```

## 4. Practical Program – Random Numbers
```python
import random

for i in range(5):
    print(random.randint(1, 100))
```

## 5. Practical Program – Dice Rolling
```python
import random

dice = random.randint(1, 6)
print("You got:", dice)
```

## 📝 Practice Programs
1. Find the square root of a number.
2. Find the factorial of a number.
3. Calculate the power of a number.
4. Generate a random number between 1 and 50.
5. Generate 5 random numbers between 1 and 100.
6. Select a random name from a list.
7. Create a dice rolling program.
8. Shuffle a list of numbers.

## 🔑 Key Takeaways
```text
Module
   ↓
Reusable Python code

math
   ↓
Mathematical operations

random
   ↓
Random values and selections
```

## 🚀 Day 31 Summary
We learned how to use Python's built-in `math` and `random` modules to perform mathematical operations and generate random values.

**Next:** Day 32 – Python Packages
