# 🐍 Day 5 – Python Variables & Keywords – II

## 📚 Topics Covered

- Identifiers in Python
- Rules for naming identifiers
- Valid and invalid variable names
- Python keywords
- `keyword` module
- `keyword.kwlist`
- `keyword.iskeyword()`
- Identifying invalid variable names
- Practice programs

---

## 1. Identifiers

An **identifier** is a name used to identify something in a Python program.

Examples:

```python
name = "Pavan"
age = 23
student_marks = 85
```

Here:

- `name` is an identifier
- `age` is an identifier
- `student_marks` is an identifier

> Variable names are one common type of identifier.

---

## 2. Rules for Naming Identifiers

### Rule 1: Must start with a letter or underscore

Valid:

```python
name = "Pavan"
_age = 23
student = "Rahul"
```

Invalid:

```python
1student = "Rahul"
```

---

### Rule 2: Can contain letters, digits and underscore

Valid:

```python
student1 = "Pavan"
student_1 = "Rahul"
student_marks = 85
```

---

### Rule 3: Spaces are not allowed

❌ Invalid:

```python
student name = "Pavan"
```

✅ Correct:

```python
student_name = "Pavan"
```

---

### Rule 4: Special characters are not allowed

❌ Invalid:

```python
student-name = "Pavan"
student@name = "Pavan"
student$name = "Pavan"
```

✅ Correct:

```python
student_name = "Pavan"
```

---

### Rule 5: Python is case-sensitive

Python treats uppercase and lowercase letters as different.

```python
name = "Pavan"
Name = "Rahul"
NAME = "Kiran"
```

These are three different identifiers.

---

### Rule 6: Keywords cannot normally be used as identifiers

❌ Invalid:

```python
class = "CSE"
if = 10
for = 20
```

These words are Python keywords.

---

# 3. Valid vs Invalid Identifiers

| Identifier | Valid? | Reason |
|---|---|---|
| `name` | ✅ | Valid |
| `student1` | ✅ | Number is not at the beginning |
| `student_name` | ✅ | Underscore is allowed |
| `_age` | ✅ | Can start with `_` |
| `1student` | ❌ | Starts with a number |
| `student-name` | ❌ | `-` is not allowed |
| `student name` | ❌ | Spaces are not allowed |
| `student@name` | ❌ | `@` is not allowed |
| `class` | ❌ | Python keyword |
| `for` | ❌ | Python keyword |

---

# 4. Python Keywords

**Keywords** are reserved words in Python that have a predefined meaning.

Examples:

```text
if
else
elif
for
while
class
def
return
import
from
try
except
finally
break
continue
pass
and
or
not
in
is
True
False
None
```

Keywords cannot normally be used as variable names.

Example:

```python
if = 10
```

❌ Invalid because `if` is a keyword.

---

# 5. Why Are Keywords Reserved?

Keywords already have a specific purpose in Python.

### `if`

Used for conditions:

```python
age = 20

if age >= 18:
    print("Adult")
```

### `for`

Used for loops:

```python
for i in range(5):
    print(i)
```

### `class`

Used to define classes:

```python
class Student:
    pass
```

### `def`

Used to define functions:

```python
def greet():
    print("Hello")
```

Because these words have special meanings, they cannot normally be used as variable names.

---

# 6. Using the `keyword` Module

Python provides a built-in module called `keyword` to work with Python keywords.

Import it using:

```python
import keyword
```

---

# 7. Display All Python Keywords

Use:

```python
import keyword

print(keyword.kwlist)
```

`keyword.kwlist` returns the list of keywords recognized by the current Python version.

> The exact list can vary slightly between Python versions.

---

# 8. Check Whether a Word Is a Keyword

Python provides:

```python
keyword.iskeyword()
```

Example:

```python
import keyword

print(keyword.iskeyword("if"))
```

Output:

```text
True
```

Because `if` is a keyword.

---

### Example 2

```python
import keyword

print(keyword.iskeyword("student"))
```

Output:

```text
False
```

Because `student` is not a Python keyword.

---

# 9. Check Multiple Words

```python
import keyword

print(keyword.iskeyword("if"))
print(keyword.iskeyword("for"))
print(keyword.iskeyword("student"))
print(keyword.iskeyword("class"))
```

Output:

```text
True
True
False
True
```

---

# 10. Keyword Validator Program

```python
import keyword

word = input("Enter a word: ")

if keyword.iskeyword(word):
    print("It is a Python keyword")
else:
    print("It is not a Python keyword")
```

### Example

Input:

```text
if
```

Output:

```text
It is a Python keyword
```

Input:

```text
student
```

Output:

```text
It is not a Python keyword
```

---

# 11. Practice Program – Check Multiple Words

```python
import keyword

words = ["if", "else", "name", "class", "student", "return"]

for word in words:
    print(word, keyword.iskeyword(word))
```

Possible output:

```text
if True
else True
name False
class True
student False
return True
```

---

# 12. Identify Invalid Variable Names

### Example 1

```python
1name = "Pavan"
```

❌ Invalid

**Reason:** Identifier cannot start with a number.

---

### Example 2

```python
student-name = "Pavan"
```

❌ Invalid

**Reason:** `-` cannot be used in an identifier.

---

### Example 3

```python
student name = "Pavan"
```

❌ Invalid

**Reason:** Spaces are not allowed.

---

### Example 4

```python
class = "CSE"
```

❌ Invalid

**Reason:** `class` is a Python keyword.

---

### Example 5

```python
student@name = "Pavan"
```

❌ Invalid

**Reason:** `@` cannot be used in a normal identifier.

---

# 13. Recommended Naming Style

Python commonly uses **snake_case** for variable names.

Recommended:

```python
student_name = "Pavan"
student_age = 23
student_marks = 85
college_name = "ABC College"
```

Use meaningful names instead of unclear names.

❌ Less descriptive:

```python
x = "Pavan"
y = 23
z = 85
```

✅ Better:

```python
student_name = "Pavan"
student_age = 23
student_marks = 85
```

---

# 🧪 Practice Exercises

## Exercise 1 – Valid or Invalid?

Identify whether each name is valid or invalid:

```text
name
student1
1student
student_name
student-name
_age
student name
class
marks2026
student@name
```

For every invalid name, write the reason.

---

## Exercise 2 – Create Valid Variables

Create variables for:

- Student name
- Student age
- College name
- Branch
- Marks

Example:

```python
student_name = "Pavan"
student_age = 23
college_name = "ABC College"
branch = "CSE"
student_marks = 85
```

---

## Exercise 3 – Display Keywords

Write a Python program to display all Python keywords.

```python
import keyword

print(keyword.kwlist)
```

---

## Exercise 4 – Keyword Checker

Write a program that accepts a word from the user and checks whether it is a Python keyword.

```python
import keyword

word = input("Enter a word: ")

print(keyword.iskeyword(word))
```

---

## Exercise 5 – Find Five Invalid Names

Identify at least **5 invalid variable names** and explain why they are invalid.

Example:

```text
1name
student-name
student name
class
student@name
```

---

# 🧠 Quick Revision

### What is an identifier?

A name used to identify something in a Python program.

### What is a keyword?

A reserved word with a predefined meaning in Python.

### Can an identifier start with a number?

❌ No.

### Can an identifier contain a number?

✅ Yes, as long as it does not start with a number.

```python
student1 = "Pavan"
```

### Can an identifier contain `_`?

✅ Yes.

```python
student_name = "Pavan"
```

### Can we use `class` as a variable name?

❌ No. It is a keyword.

### How do we get the keyword list?

```python
import keyword

print(keyword.kwlist)
```

### How do we check whether a word is a keyword?

```python
keyword.iskeyword("if")
```

---

# 🎯 Day 5 Key Takeaways

```text
IDENTIFIER
    ↓
Name used to identify something in Python

VALID IDENTIFIER
    ↓
Letters + digits + underscore
But cannot start with a digit

INVALID
    ↓
❌ Starts with number
❌ Contains spaces
❌ Contains invalid special characters
❌ Uses Python keyword

KEYWORD
    ↓
Reserved word with special meaning

keyword module
    ↓
import keyword

keyword.kwlist
    ↓
Displays keywords

keyword.iskeyword("if")
    ↓
Checks whether a word is a keyword
```

---

# 🚀 Final Challenge

Create a program that asks the user for a word and tells whether it is a Python keyword.

Then test it with:

```text
if
for
class
student
hello
return
```

Expected result:

```text
if       → Keyword
for      → Keyword
class    → Keyword
student  → Not a keyword
hello    → Not a keyword
return   → Keyword
```

---

## 📌 Day 5 Assignment

1. Create **10 valid variable names**.
2. Identify **5 invalid variable names** and give reasons.
3. Print Python's keyword list using `keyword.kwlist`.
4. Check 5 words using `keyword.iskeyword()`.
5. Create a **Keyword Checker** program using user input.

> **Commit your Day 5 programs to the GitHub repository before the next class.**