# Day 42 – Python Inheritance

## Topics
- Parent Class
- Child Class
- Inheritance
- Inherited Methods
- Method Overriding
- `super()`
- Multilevel Inheritance

## Learning Objectives
Students should be able to create parent and child classes, reuse parent methods, override methods, and use `super()`.

## 1. What is Inheritance?
Inheritance is an OOP mechanism in which one class acquires properties and methods from another class.

### Important Words
- **Inheritance:** Acquiring features of another class.
- **Parent Class:** The class whose features are inherited.
- **Base Class:** Another name for parent class.
- **Superclass:** Another name for parent class.
- **Child Class:** The class that inherits from a parent.
- **Derived Class:** Another name for child class.
- **Subclass:** Another name for child class.
- **Reuse:** Using existing code again instead of rewriting it.

## Basic Syntax

```python
class Parent:
    pass

class Child(Parent):
    pass
```

`Child(Parent)` means Child inherits from Parent.

## 2. Simple Inheritance Example

```python
class Person:

    def speak(self):
        print("Person can speak")


class Student(Person):

    def study(self):
        print("Student can study")


s1 = Student()

s1.speak()
s1.study()
```

The `Student` object can use `speak()` because it inherited that method from `Person`.

## 3. Method Overriding
Method overriding happens when a child class defines a method with the same name as a method in the parent class.

```python
class Person:

    def display(self):
        print("I am a person")


class Student(Person):

    def display(self):
        print("I am a student")


s1 = Student()
s1.display()
```

Output:

```text
I am a student
```

## 4. `super()`
`super()` is used to access parent-class functionality from the child class.

```python
class Person:

    def display(self):
        print("Person method")


class Student(Person):

    def display(self):
        super().display()
        print("Student method")


s1 = Student()
s1.display()
```

## 5. Using `super()` with a Constructor

```python
class Person:

    def __init__(self, name):
        self.name = name

    def display_person(self):
        print("Name:", self.name)


class Student(Person):

    def __init__(self, name, marks):
        super().__init__(name)
        self.marks = marks

    def display_student(self):
        self.display_person()
        print("Marks:", self.marks)


s1 = Student("Pavan", 85)
s1.display_student()
```

## Main Practical – Employee and Manager

```python
class Employee:

    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def display(self):
        print("Name:", self.name)
        print("Salary:", self.salary)


class Manager(Employee):

    def __init__(self, name, salary, department):
        super().__init__(name, salary)
        self.department = department

    def display(self):
        print("Name:", self.name)
        print("Salary:", self.salary)
        print("Department:", self.department)


m1 = Manager("Rahul", 50000, "IT")
m1.display()
```

## 6. Multilevel Inheritance
Multilevel inheritance means inheritance through more than one level.

```text
Person
   ↓
Student
   ↓
CollegeStudent
```

```python
class Person:

    def speak(self):
        print("Person can speak")


class Student(Person):

    def study(self):
        print("Student can study")


class CollegeStudent(Student):

    def attend_class(self):
        print("College student attends class")


c1 = CollegeStudent()

c1.speak()
c1.study()
c1.attend_class()
```

## Student Practice

1. Create `Animal` → `Dog` and override `sound()`.
2. Create `Vehicle` → `Car` with `start()` and `drive()`.
3. Create `Person` → `Teacher` and use `super()`.
4. Create `Employee` → `Developer` with name, salary, and programming language.
5. Challenge: Create `Person` → `Student` → `CollegeStudent`.

## Quick Revision
- Parent → gives inherited features
- Child → receives inherited features
- Inheritance → code reuse through classes
- Overriding → child provides its own version of a parent method
- `super()` → accesses parent-class functionality
