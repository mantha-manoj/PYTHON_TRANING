# Day 39 - OOP Basics I

## Topics
- Object-Oriented Programming (OOP)
- Class
- Object
- Attributes / Properties
- Creating multiple objects

## Learning Objectives
Understand what a class and object are and how to store and access object attributes.

## Class and Object
OOP organizes programs using classes and objects.

- Class = Blueprint
- Object = Real thing created from the blueprint

```python
class Student:
    pass

student1 = Student()
```

## Adding Attributes
```python
class Student:
    pass

student1 = Student()

student1.name = "Rahul"
student1.marks = 85

print(student1.name)
print(student1.marks)
```

## Multiple Objects
```python
class Student:
    pass

student1 = Student()
student2 = Student()
student3 = Student()

student1.name = "Rahul"
student1.marks = 85

student2.name = "Priya"
student2.marks = 92

student3.name = "Ravi"
student3.marks = 76

print(student1.name, student1.marks)
print(student2.name, student2.marks)
print(student3.name, student3.marks)
```

## Practice Programs
1. Create a Book class with title, author and price. Create two objects.
2. Create a Mobile class with brand, model and price. Create three objects.
3. Create a Person class with name, age and city. Create three objects.
4. Create a Car class with brand, model, price and color. Create three objects.

## Key Points
- Class = Blueprint
- Object = Instance of a class
- Attribute = Data stored in an object
- `object.attribute` accesses an attribute.
