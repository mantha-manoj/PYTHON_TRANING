# Day 18 — Python String Methods – I

## 📚 Topics Covered

In Day 18, we learned commonly used Python string methods for modifying, searching, replacing, and splitting strings.

### String Methods

| Method | Purpose | Example |
|---|---|---|
| `upper()` | Converts string to uppercase | `"hello".upper()` → `"HELLO"` |
| `lower()` | Converts string to lowercase | `"HELLO".lower()` → `"hello"` |
| `title()` | Capitalizes the first letter of every word | `"hello python".title()` → `"Hello Python"` |
| `capitalize()` | Capitalizes only the first character | `"hello python".capitalize()` → `"Hello python"` |
| `find()` | Finds the index/position of a substring | `"I love Python".find("Python")` → `7` |
| `replace()` | Replaces one substring with another | `"I love Java".replace("Java", "Python")` |
| `split()` | Splits a string into a list | `"Python is easy".split()` |

---

## 1. `upper()`

Converts all letters in a string to uppercase.

```python
text = "hello python"

print(text.upper())
```

### Output

```text
HELLO PYTHON
```

---

## 2. `lower()`

Converts all letters in a string to lowercase.

```python
text = "HELLO PYTHON"

print(text.lower())
```

### Output

```text
hello python
```

### Example

```python
email = "PAVAN@GMAIL.COM"

print(email.lower())
```

Output:

```text
pavan@gmail.com
```

---

## 3. `title()`

Converts the first letter of every word to uppercase.

```python
text = "python programming language"

print(text.title())
```

### Output

```text
Python Programming Language
```

---

## 4. `capitalize()`

Converts only the first character of the string to uppercase.

```python
text = "python programming language"

print(text.capitalize())
```

### Output

```text
Python programming language
```

### Difference Between `title()` and `capitalize()`

```python
text = "python programming language"

print(text.title())
print(text.capitalize())
```

Output:

```text
Python Programming Language
Python programming language
```

---

## 5. `find()`

The `find()` method searches for a substring and returns its index.

```python
text = "I love Python"

print(text.find("Python"))
```

Output:

```text
7
```

Python uses **zero-based indexing**, so the first character has index `0`.

### If the text is not found

```python
text = "I love Python"

print(text.find("Java"))
```

Output:

```text
-1
```

---

## 6. `replace()`

The `replace()` method replaces one piece of text with another.

```python
text = "I love Java"

new_text = text.replace("Java", "Python")

print(new_text)
```

Output:

```text
I love Python
```

### Replacing Multiple Occurrences

```python
text = "Java is easy. Java is popular."

print(text.replace("Java", "Python"))
```

Output:

```text
Python is easy. Python is popular.
```

---

## 7. `split()`

The `split()` method divides a string into a list.

```python
sentence = "Python is easy to learn"

words = sentence.split()

print(words)
```

Output:

```text
['Python', 'is', 'easy', 'to', 'learn']
```

### Splitting Using a Separator

```python
data = "Pavan,Harsh,Manoj"

names = data.split(",")

print(names)
```

Output:

```text
['Pavan', 'Harsh', 'Manoj']
```

Another example:

```python
data = "Python-Java-Spring-AWS"

print(data.split("-"))
```

Output:

```text
['Python', 'Java', 'Spring', 'AWS']
```

---

# 🎯 Practical Program

## String Methods Program

```python
sentence = input("Enter a sentence: ")

print("Uppercase:", sentence.upper())
print("Lowercase:", sentence.lower())
print("Title Case:", sentence.title())

word = input("Enter word to find: ")
print("Position:", sentence.find(word))

old_word = input("Enter word to replace: ")
new_word = input("Enter new word: ")

print("Updated sentence:", sentence.replace(old_word, new_word))

print("Words:", sentence.split())
```

### Example

Input:

```text
Python is easy to learn
easy
Python
Java
```

Output:

```text
Uppercase: PYTHON IS EASY TO LEARN
Lowercase: python is easy to learn
Title Case: Python Is Easy To Learn
Position: 10
Updated sentence: Java is easy to learn
Words: ['Python', 'is', 'easy', 'to', 'learn']
```

---

# 🎯 Mini Project — Student Name Formatter

```python
name = input("Enter your full name: ")

print("Uppercase:", name.upper())
print("Lowercase:", name.lower())
print("Title:", name.title())
```

### Example

Input:

```text
pAvAn TeJ
```

Output:

```text
Uppercase: PAVAN TEJ
Lowercase: pavan tej
Title: Pavan Tej
```

---

# 📝 Practice Programs

## Exercise 1

Take a sentence from the user and print:

- Uppercase
- Lowercase
- Title Case

## Exercise 2

Take a sentence and ask the user for a word. Find its position using `find()`.

## Exercise 3

Replace `difficult` with `easy`.

```text
Python is difficult
```

Expected output:

```text
Python is easy
```

## Exercise 4

Convert this string into a list:

```text
Apple,Banana,Mango,Orange
```

Expected:

```python
['Apple', 'Banana', 'Mango', 'Orange']
```

## Exercise 5 — Challenge ⭐

Take:

```text
pavan, harsh, manoj
```

Split the names and display each name in title case.

Expected:

```text
Pavan
Harsh
Manoj
```

---

# ⚠️ Important Concept — Strings Are Immutable

String methods do not modify the original string.

```python
text = "hello"

text.upper()

print(text)
```

Output:

```text
hello
```

To store the modified value:

```python
text = "hello"

text = text.upper()

print(text)
```

Output:

```text
HELLO
```

### Why?

Python strings are **immutable**, which means their existing characters cannot be changed directly.

---

# 🧠 Quick Revision

```text
upper()       → Converts to uppercase
lower()       → Converts to lowercase
title()       → Capitalizes every word
capitalize()  → Capitalizes first character
find()        → Finds the position of text
replace()     → Replaces text
split()       → Converts string into a list
```

---

# 💡 Key Points

1. String methods are called using `string.method()`.
2. Python string indexing starts from `0`.
3. `find()` returns `-1` when the substring is not found.
4. `split()` converts a string into a list.
5. `replace()` returns a new string.
6. `upper()`, `lower()`, `title()`, and `capitalize()` return new strings.
7. Strings are immutable in Python.

---

## 🚀 Day 18 Completed

**Next:** Day 19 — String Methods – II
