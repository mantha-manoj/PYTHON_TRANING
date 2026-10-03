# Python Day 43 – Polymorphism & Abstraction

## Duration

3 Hours

## Topics

-   OOP revision
-   Abstraction
-   Abstract class
-   Abstract method
-   `ABC` and `@abstractmethod`
-   Polymorphism
-   Method overriding
-   Combined abstraction and polymorphism
-   Practical exercises

## Abstraction

Abstraction means hiding unnecessary implementation details and showing
only essential features.

Python provides the `abc` module:

``` python
from abc import ABC, abstractmethod
```

Example:

``` python
from abc import ABC, abstractmethod

class Shape(ABC):

    @abstractmethod
    def area(self):
        pass

class Rectangle(Shape):

    def __init__(self, length, breadth):
        self.length = length
        self.breadth = breadth

    def area(self):
        return self.length * self.breadth

class Circle(Shape):

    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

print(Rectangle(10, 5).area())
print(Circle(7).area())
```

## Polymorphism

Polymorphism means **one interface, multiple forms**.

The same method can behave differently depending on the object.

``` python
class Dog:
    def sound(self):
        print("Dog barks")

class Cat:
    def sound(self):
        print("Cat meows")

for animal in [Dog(), Cat()]:
    animal.sound()
```

## Combined Practical

``` python
from abc import ABC, abstractmethod

class Shape(ABC):

    @abstractmethod
    def area(self):
        pass

class Rectangle(Shape):

    def __init__(self, length, breadth):
        self.length = length
        self.breadth = breadth

    def area(self):
        return self.length * self.breadth

class Circle(Shape):

    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

class Triangle(Shape):

    def __init__(self, base, height):
        self.base = base
        self.height = height

    def area(self):
        return 0.5 * self.base * self.height

shapes = [Rectangle(10, 5), Circle(7), Triangle(10, 8)]

for shape in shapes:
    print("Area:", shape.area())
```

## Practice Tasks

1.  Create an abstract `Vehicle` class with `start()`, then implement
    `Car`, `Bike`, and `Bus`.
2.  Create `Employee`, `Developer`, `Tester`, and `Manager`, each with a
    different `work()` implementation.
3.  Create an abstract `Payment` class and implement `UPIPayment`,
    `CardPayment`, and `CashPayment`.

## Day 43 Summary

Students should understand abstraction, abstract classes, abstract
methods, `ABC`, `@abstractmethod`, polymorphism, and how to combine
abstraction with polymorphism.
