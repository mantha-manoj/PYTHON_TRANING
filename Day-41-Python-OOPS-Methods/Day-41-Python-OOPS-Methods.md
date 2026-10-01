# Day 41 – Python OOP Methods

## Topics
- Instance Method
- Class Method
- Static Method
- `self`
- `cls`
- `@classmethod`
- `@staticmethod`

## Learning Objectives
Students should be able to explain and implement the three main types of methods in Python.

## 1. What is OOP?
OOP means **Object-Oriented Programming**. It is a programming approach based on classes and objects.

### Important Words
- **Class:** A blueprint/template used to create objects.
- **Object:** An instance of a class.
- **Method:** A function written inside a class.
- **Instance:** An object created from a class.
- **Attribute:** Data/variable belonging to an object or class.

## 2. Instance Method
An instance method works with object data and normally takes `self` as its first parameter.

```python
class Student:
    def display(self):
        print("Student is studying")

s1 = Student()
s1.display()
```

### `self`
`self` represents the current object.

```python
class Employee:
    def set_name(self, name):
        self.name = name

    def display(self):
        print("Employee Name:", self.name)

e1 = Employee()
e1.set_name("Pavan")
e1.display()
```

## 3. Class Method
A class method works with class-level data. It uses `@classmethod` and normally takes `cls` as its first parameter.

### `cls`
`cls` represents the current class.

```python
class Student:
    college = "ABC College"

    @classmethod
    def display_college(cls):
        print(cls.college)

Student.display_college()
```

## 4. Static Method
A static method does not require `self` or `cls`. It is commonly used for utility/helper operations.

```python
class Calculator:

    @staticmethod
    def add(a, b):
        return a + b

print(Calculator.add(10, 20))
```

## Comparison

| Method | Decorator | First Parameter | Main Use |
|---|---|---|---|
| Instance | None | `self` | Object data |
| Class | `@classmethod` | `cls` | Class data |
| Static | `@staticmethod` | None | Utility operation |

## Main Practical

```python
class Employee:
    company = "ABC Technologies"

    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def display(self):
        print("Name:", self.name)
        print("Salary:", self.salary)

    @classmethod
    def show_company(cls):
        print("Company:", cls.company)

    @staticmethod
    def is_valid_salary(salary):
        return salary > 0

e1 = Employee("Pavan", 30000)

e1.display()
Employee.show_company()
print(Employee.is_valid_salary(30000))
```

## Student Practice
1. Create a `Student` class with `display()`, `show_school()`, and `is_pass()`.
2. Create a `BankAccount` class with an instance method, class method, and static method.
3. Create a `Calculator` class with static methods for addition, subtraction, multiplication, and division.

## Quick Revision
- `self` → current object
- `cls` → current class
- `@classmethod` → class method
- `@staticmethod` → static method
- Instance method → works mainly with object data
- Class method → works mainly with class data
- Static method → independent utility operation
