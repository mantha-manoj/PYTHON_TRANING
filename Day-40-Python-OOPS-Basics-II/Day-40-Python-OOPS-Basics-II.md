# Day 40 - OOP Basics II

## Topics
- Constructor
- `__init__()`
- `self`
- Methods
- Simple class-based programs

## Learning Objectives
Understand how constructors initialize objects and how methods perform actions.

## Constructor
Instead of assigning values separately, initialize them while creating the object.

```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

student1 = Student("Rahul", 85)

print(student1.name)
print(student1.marks)
```

## Understanding self
`self` refers to the current object.

For:
```python
student1 = Student("Rahul", 85)
```

Python stores:
```python
student1.name = "Rahul"
student1.marks = 85
```

## Methods
A function defined inside a class is called a method.

```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def display(self):
        print("Name:", self.name)
        print("Marks:", self.marks)

student1 = Student("Rahul", 85)
student1.display()
```

## Result Method
```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def result(self):
        if self.marks >= 35:
            print(self.name, "Pass")
        else:
            print(self.name, "Fail")

student1 = Student("Rahul", 85)
student2 = Student("Ravi", 25)

student1.result()
student2.result()
```

## Final Program
```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def display(self):
        print("Name:", self.name)
        print("Marks:", self.marks)

    def result(self):
        if self.marks >= 35:
            print("Result: Pass")
        else:
            print("Result: Fail")

student1 = Student("Rahul", 85)
student2 = Student("Priya", 92)
student3 = Student("Ravi", 25)

student1.display()
student1.result()

print()

student2.display()
student2.result()

print()

student3.display()
student3.result()
```

## Practice Programs
1. Create a Book class using `__init__()` and a `display()` method.
2. Create an Employee class with name and salary and a display method.
3. Create a Student class with a `grade()` method:
   - 90+ -> A
   - 75-89 -> B
   - 50-74 -> C
   - Below 50 -> D
4. Create a BankAccount class with account holder and balance. Add display, deposit and withdraw methods.

## Key Points
- `__init__()` initializes object data.
- `self` refers to the current object.
- A function inside a class is called a method.
- Methods are called using `object.method()`.
