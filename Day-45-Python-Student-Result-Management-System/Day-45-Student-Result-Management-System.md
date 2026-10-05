# Day 45 – Python Final Revision & Student Result Management System

## 📅 Day 45
**Duration:** 3 Hours  
**Topic:** Final Revision + Student Result Management System  
**Language:** Python

---

# 🎯 Learning Objectives

By the end of Day 45, students will be able to:

- Revise important Python concepts.
- Create classes and objects.
- Use constructors and instance variables.
- Create and use methods.
- Work with lists and loops.
- Use conditional statements.
- Handle exceptions.
- Read from and write to files.
- Build a menu-driven Python application.
- Create a complete Student Result Management System.

---

# 1. Python Concepts Revision

## Variables

A variable stores a value.

```python
name = "Pavan"
age = 22
marks = 85.5
```

## Data Types

```python
name = "Pavan"       # str
age = 22             # int
percentage = 85.5    # float
passed = True         # bool
```

Common collection types:

```python
subjects = ["Python", "Java", "SQL"]

student = {
    "name": "Pavan",
    "age": 22
}
```

---

# 2. Conditional Statements

Used for decision making.

```python
marks = 75

if marks >= 40:
    print("Pass")
else:
    print("Fail")
```

Multiple conditions:

```python
marks = 85

if marks >= 90:
    print("A+")
elif marks >= 80:
    print("A")
elif marks >= 70:
    print("B")
else:
    print("C")
```

---

# 3. Loops

## for Loop

```python
for i in range(1, 6):
    print(i)
```

## while Loop

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

---

# 4. Functions

A function is a reusable block of code.

```python
def add(a, b):
    return a + b

result = add(10, 20)
print(result)
```

---

# 5. Lists

A list stores multiple values.

```python
marks = [80, 75, 90, 65]

marks.append(85)
marks.remove(65)
marks.sort()
```

Accessing an element:

```python
print(marks[0])
```

---

# 6. Dictionaries

A dictionary stores key-value pairs.

```python
student = {
    "name": "Pavan",
    "age": 22,
    "marks": 85
}

print(student["name"])
```

---

# 7. Exception Handling

Exception handling prevents the program from crashing because of runtime errors.

```python
try:
    number = int(input("Enter number: "))
    print(10 / number)

except ZeroDivisionError:
    print("Cannot divide by zero")

except ValueError:
    print("Please enter a valid number")
```

Important keywords:

- `try`
- `except`
- `else`
- `finally`
- `raise`

---

# 8. File Handling

## Writing to a File

```python
with open("students.txt", "w") as file:
    file.write("Pavan - 85")
```

## Reading from a File

```python
with open("students.txt", "r") as file:
    data = file.read()

print(data)
```

Using `with` automatically closes the file.

---

# 9. OOP Revision

Important Object-Oriented Programming concepts:

- Class
- Object
- Constructor
- Instance Variables
- Instance Methods
- Inheritance
- Method Overriding
- Polymorphism
- Abstraction
- Encapsulation

Example:

```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def display(self):
        print(self.name)
        print(self.marks)


student = Student("Pavan", 85)
student.display()
```

---

# 10. Final Project

# Student Result Management System

The final project combines the concepts learned throughout the course.

## Project Features

The application will support:

1. Add Student
2. Display All Students
3. Search Student
4. Update Student
5. Delete Student
6. Calculate Total Marks
7. Calculate Percentage
8. Calculate Grade
9. Determine Pass/Fail
10. Display Class Topper
11. Display Class Statistics
12. Save Student Data
13. Load Student Data
14. Exception Handling
15. Menu-driven operation

---

# 11. Student Class

Each student contains:

- Student ID
- Name
- Python Marks
- Java Marks
- SQL Marks

```python
class Student:

    def __init__(self, student_id, name, python, java, sql):
        self.student_id = student_id
        self.name = name
        self.python = python
        self.java = java
        self.sql = sql
```

---

# 12. Calculate Total

```python
def calculate_total(self):
    return self.python + self.java + self.sql
```

Maximum marks:

```text
100 + 100 + 100 = 300
```

---

# 13. Calculate Percentage

Formula:

```text
Percentage = (Total Marks / 300) × 100
```

Python:

```python
def calculate_percentage(self):
    return (self.calculate_total() / 300) * 100
```

---

# 14. Calculate Grade

```python
def calculate_grade(self):

    percentage = self.calculate_percentage()

    if percentage >= 90:
        return "A+"
    elif percentage >= 80:
        return "A"
    elif percentage >= 70:
        return "B"
    elif percentage >= 60:
        return "C"
    elif percentage >= 50:
        return "D"
    else:
        return "F"
```

---

# 15. Calculate Result

A student must score at least 40 marks in every subject.

```python
def calculate_result(self):

    if (
        self.python >= 40
        and self.java >= 40
        and self.sql >= 40
    ):
        return "PASS"

    return "FAIL"
```

---

# 16. Display Student

```python
def display(self):

    print("Student ID:", self.student_id)
    print("Name:", self.name)
    print("Python:", self.python)
    print("Java:", self.java)
    print("SQL:", self.sql)
    print("Total:", self.calculate_total())
    print("Percentage:", round(self.calculate_percentage(), 2))
    print("Grade:", self.calculate_grade())
    print("Result:", self.calculate_result())
```

---

# 17. Store Students

Use a list to store multiple Student objects.

```python
students = []
```

Add an object:

```python
student = Student(101, "Pavan", 85, 78, 92)

students.append(student)
```

---

# 18. Add Student

The program should accept input from the user.

Important validations:

- Student ID must be numeric.
- Marks must be between 0 and 100.
- Duplicate Student IDs should not be allowed.

Example:

```python
student_id = int(input("Enter Student ID: "))
name = input("Enter Student Name: ")

python = int(input("Enter Python Marks: "))
java = int(input("Enter Java Marks: "))
sql = int(input("Enter SQL Marks: "))
```

---

# 19. Search Student

Search using Student ID.

```python
for student in students:

    if student.student_id == student_id:
        student.display()
        return
```

If no student is found:

```text
Student not found.
```

---

# 20. Update Student

The update operation should allow the user to change:

- Name
- Python marks
- Java marks
- SQL marks

Example:

```python
student.name = name
student.python = python
student.java = java
student.sql = sql
```

---

# 21. Delete Student

Find the student and remove the object from the list.

```python
students.remove(student)
```

---

# 22. Find Topper

Compare student percentages.

```python
topper = students[0]

for student in students:

    if student.calculate_percentage() > topper.calculate_percentage():
        topper = student
```

---

# 23. Class Statistics

Calculate:

- Total students
- Number of passed students
- Number of failed students
- Average percentage

Average formula:

```text
Average = Sum of percentages / Number of students
```

---

# 24. File Handling

Save student data into:

```text
students.txt
```

Example format:

```text
101|Pavan|85|78|92
102|Rahul|90|88|95
```

Use:

```python
with open("students.txt", "w") as file:
    ...
```

Load data using:

```python
with open("students.txt", "r") as file:
    ...
```

---

# 25. Menu-Driven Program

The final application uses a menu:

```text
========================================
     STUDENT RESULT MANAGEMENT SYSTEM
========================================

1. Add Student
2. Display All Students
3. Search Student
4. Update Student
5. Delete Student
6. Display Topper
7. Display Statistics
8. Save Students
9. Exit

========================================
Enter your choice:
```

The menu should continue until the user selects Exit.

---

# 26. Complete Project Flow

```text
Start
  |
  ↓
Load saved student data
  |
  ↓
Display Main Menu
  |
  ├── Add Student
  |
  ├── Display Students
  |
  ├── Search Student
  |
  ├── Update Student
  |
  ├── Delete Student
  |
  ├── Display Topper
  |
  ├── Display Statistics
  |
  ├── Save Students
  |
  └── Exit
```

---

# 27. Complete Project Code

```python
class Student:

    def __init__(self, student_id, name, python, java, sql):
        self.student_id = student_id
        self.name = name
        self.python = python
        self.java = java
        self.sql = sql

    def calculate_total(self):
        return self.python + self.java + self.sql

    def calculate_percentage(self):
        return (self.calculate_total() / 300) * 100

    def calculate_grade(self):

        percentage = self.calculate_percentage()

        if percentage >= 90:
            return "A+"
        elif percentage >= 80:
            return "A"
        elif percentage >= 70:
            return "B"
        elif percentage >= 60:
            return "C"
        elif percentage >= 50:
            return "D"
        else:
            return "F"

    def calculate_result(self):

        if (
            self.python >= 40
            and self.java >= 40
            and self.sql >= 40
        ):
            return "PASS"

        return "FAIL"

    def display(self):

        print("\n----------------------------------------")
        print("          STUDENT DETAILS")
        print("----------------------------------------")

        print("Student ID :", self.student_id)
        print("Name       :", self.name)
        print("Python     :", self.python)
        print("Java       :", self.java)
        print("SQL        :", self.sql)
        print("Total      :", self.calculate_total())
        print(
            "Percentage :",
            round(self.calculate_percentage(), 2),
            "%"
        )
        print("Grade      :", self.calculate_grade())
        print("Result     :", self.calculate_result())
        print("----------------------------------------")


students = []


def add_student():

    try:

        student_id = int(input("Enter Student ID: "))

        for student in students:

            if student.student_id == student_id:
                print("Student ID already exists!")
                return

        name = input("Enter Student Name: ")

        python = int(input("Enter Python Marks: "))
        java = int(input("Enter Java Marks: "))
        sql = int(input("Enter SQL Marks: "))

        if (
            python < 0 or python > 100
            or java < 0 or java > 100
            or sql < 0 or sql > 100
        ):
            print("Marks must be between 0 and 100.")
            return

        student = Student(
            student_id,
            name,
            python,
            java,
            sql
        )

        students.append(student)

        print("Student added successfully!")

    except ValueError:
        print("Invalid input!")


def display_all_students():

    if len(students) == 0:
        print("No students available.")
        return

    for student in students:
        student.display()


def search_student():

    try:

        student_id = int(input("Enter Student ID: "))

        for student in students:

            if student.student_id == student_id:
                student.display()
                return

        print("Student not found.")

    except ValueError:
        print("Student ID must be a number.")


def update_student():

    try:

        student_id = int(input("Enter Student ID: "))

        for student in students:

            if student.student_id == student_id:

                student.name = input("Enter new name: ")
                student.python = int(
                    input("Enter new Python marks: ")
                )
                student.java = int(
                    input("Enter new Java marks: ")
                )
                student.sql = int(
                    input("Enter new SQL marks: ")
                )

                print("Student updated successfully!")
                return

        print("Student not found.")

    except ValueError:
        print("Invalid input.")


def delete_student():

    try:

        student_id = int(input("Enter Student ID: "))

        for student in students:

            if student.student_id == student_id:

                students.remove(student)

                print("Student deleted successfully!")
                return

        print("Student not found.")

    except ValueError:
        print("Invalid Student ID.")


def display_topper():

    if len(students) == 0:
        print("No students available.")
        return

    topper = students[0]

    for student in students:

        if (
            student.calculate_percentage()
            > topper.calculate_percentage()
        ):
            topper = student

    print("\nTOPPER")
    topper.display()


def display_statistics():

    if len(students) == 0:
        print("No students available.")
        return

    total_students = len(students)

    passed = 0
    failed = 0
    total_percentage = 0

    for student in students:

        total_percentage += student.calculate_percentage()

        if student.calculate_result() == "PASS":
            passed += 1
        else:
            failed += 1

    average = total_percentage / total_students

    print("\n========== STATISTICS ==========")
    print("Total Students     :", total_students)
    print("Passed Students    :", passed)
    print("Failed Students    :", failed)
    print("Average Percentage :", round(average, 2), "%")


def save_students():

    with open("students.txt", "w") as file:

        for student in students:

            file.write(
                f"{student.student_id}|"
                f"{student.name}|"
                f"{student.python}|"
                f"{student.java}|"
                f"{student.sql}\n"
            )

    print("Student data saved successfully!")


def load_students():

    try:

        with open("students.txt", "r") as file:

            for line in file:

                line = line.strip()

                if line == "":
                    continue

                data = line.split("|")

                student = Student(
                    int(data[0]),
                    data[1],
                    int(data[2]),
                    int(data[3]),
                    int(data[4])
                )

                students.append(student)

    except FileNotFoundError:

        print("No previous data found.")


def main():

    load_students()

    while True:

        print("\n========================================")
        print("     STUDENT RESULT MANAGEMENT SYSTEM")
        print("========================================")

        print("1. Add Student")
        print("2. Display All Students")
        print("3. Search Student")
        print("4. Update Student")
        print("5. Delete Student")
        print("6. Display Topper")
        print("7. Display Statistics")
        print("8. Save Students")
        print("9. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            add_student()

        elif choice == "2":
            display_all_students()

        elif choice == "3":
            search_student()

        elif choice == "4":
            update_student()

        elif choice == "5":
            delete_student()

        elif choice == "6":
            display_topper()

        elif choice == "7":
            display_statistics()

        elif choice == "8":
            save_students()

        elif choice == "9":

            save_students()

            print("Thank you for using the system!")
            break

        else:
            print("Invalid choice!")


if __name__ == "__main__":
    main()
```

---

# 🧪 Final Student Assessment

## Task 1 – Easy

Create a `Student` class with:

- Name
- Roll number
- Marks

Create three objects.

## Task 2 – Medium

Add:

- Total
- Percentage
- Grade

## Task 3 – Medium

Implement PASS/FAIL.

## Task 4 – Hard

Create a menu-driven application.

## Task 5 – Final Challenge

Add:

- File handling
- Exception handling
- Search
- Update
- Delete
- Topper
- Statistics

---

# ⏰ 3-Hour Day-45 Plan

| Time | Activity |
|---|---|
| 0–30 min | Python revision |
| 30–60 min | OOP revision |
| 60–90 min | Student class and calculations |
| 90–120 min | Add/Search/Update/Delete |
| 120–150 min | File handling and exceptions |
| 150–180 min | Complete project + assessment |

---

# ✅ Day-45 Completion Checklist

- [ ] Variables revised
- [ ] Data types revised
- [ ] Conditions revised
- [ ] Loops revised
- [ ] Functions revised
- [ ] Lists revised
- [ ] Dictionaries revised
- [ ] Exception handling revised
- [ ] File handling revised
- [ ] OOP revised
- [ ] Student class created
- [ ] Result calculation implemented
- [ ] CRUD operations implemented
- [ ] File persistence implemented
- [ ] Menu-driven system completed
- [ ] Final assessment completed

---

## 🎓 Final Outcome

After completing Day 45, students should be able to build a small real-world Python application using the major concepts learned throughout the 45-day Python course.

**Project:** Student Result Management System  
**Difficulty:** Intermediate  
**Technologies:** Python  
**Concepts:** OOP + Functions + Lists + Conditions + Loops + Exception Handling + File Handling
