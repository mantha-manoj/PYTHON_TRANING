# Day 16 - Python Strings - I

## Topics Covered

- What is a String?
- Creating Strings
- Taking String Input
- String Indexing
- Negative Indexing
- `len()` Function
- String Slicing
- Slicing with Step
- Reversing a String
- Practical String Programs

---

## 1. What is a String?

A **string** is a sequence of characters enclosed inside quotes.

```python
name = "Pavan"
```

Python supports:

```python
"Hello"
'Hello'
"""Hello"""
'''Hello'''
```

Example:

```python
name = "Python"

print(name)
print(type(name))
```

Output:

```text
Python
<class 'str'>
```

> **Remember:** String = sequence of characters

---

## 2. Taking String Input

The `input()` function is used to take input from the user.

```python
name = input("Enter your name: ")

print("Hello", name)
```

Example:

```text
Enter your name: Pavan
Hello Pavan
```

### Important

`input()` always returns a **string**.

```python
age = input("Enter your age: ")

print(type(age))
```

Output:

```text
<class 'str'>
```

---

## 3. String Indexing

Each character in a string has an index position.

For:

```python
name = "Pavan"
```

```text
 P   a   v   a   n
 0   1   2   3   4
```

Example:

```python
name = "Pavan"

print(name[0])
print(name[1])
print(name[2])
print(name[3])
print(name[4])
```

Output:

```text
P
a
v
a
n
```

> **Important:** Python indexing starts from `0`.

---

## 4. Negative Indexing

Python also supports negative indexes.

```text
 P   a   v   a   n
 0   1   2   3   4
-5  -4  -3  -2  -1
```

Example:

```python
name = "Pavan"

print(name[-1])
print(name[-2])
print(name[-3])
```

Output:

```text
n
a
v
```

> **Remember:** `-1` means the last character.

---

## 5. `len()` Function

The `len()` function returns the number of characters in a string.

```python
name = "Pavan"

print(len(name))
```

Output:

```text
5
```

Spaces are also counted:

```python
text = "Hello World"

print(len(text))
```

Output:

```text
11
```

---

## 6. First and Last Character

```python
text = input("Enter a string: ")

print("First character:", text[0])
print("Last character:", text[-1])
```

Example:

```text
Enter a string: Python
First character: P
Last character: n
```

---

## 7. String Slicing

Slicing is used to extract a part of a string.

### Syntax

```python
string[start:end]
```

> **Important:** Start index is included, but end index is excluded.

Example:

```python
name = "Pavan"

print(name[0:3])
```

Output:

```text
Pav
```

---

## 8. More Slicing Examples

```python
text = "Python"

print(text[0:2])
print(text[2:5])
print(text[:4])
print(text[2:])
print(text[:])
```

Output:

```text
Py
tho
Pyth
thon
Python
```

### Shortcuts

```text
text[:4]   -> beginning to index 3
text[2:]   -> index 2 to the end
text[:]    -> complete string
```

---

## 9. Slicing with Step

### Syntax

```python
string[start:end:step]
```

Example:

```python
text = "Python"

print(text[0:6:2])
```

Output:

```text
Pto
```

It takes every second character.

---

## 10. Reverse a String

A string can be reversed using slicing.

```python
text = "Python"

print(text[::-1])
```

Output:

```text
nohtyP
```

### Remember

> `[::-1]` = Reverse the string

---

## 11. String Analyzer Program

```python
text = input("Enter a string: ")

print("String:", text)
print("First character:", text[0])
print("Last character:", text[-1])
print("Length:", len(text))
print("Reverse:", text[::-1])
print("First 3 characters:", text[:3])
print("Last 3 characters:", text[-3:])
```

Example:

```text
Enter a string: Python

String: Python
First character: P
Last character: n
Length: 6
Reverse: nohtyP
First 3 characters: Pyt
Last 3 characters: hon
```

---

## 12. Practice Programs

### Program 1 - First and Last Character

```python
text = input("Enter a string: ")

print("First:", text[0])
print("Last:", text[-1])
```

### Program 2 - Reverse a String

```python
text = input("Enter a string: ")

print("Reverse:", text[::-1])
```

### Program 3 - Find String Length

```python
text = input("Enter a string: ")

print("Number of characters:", len(text))
```

### Program 4 - First and Last 3 Characters

```python
text = input("Enter a string: ")

print("First 3:", text[:3])
print("Last 3:", text[-3:])
```

### Program 5 - String Analyzer

```python
text = input("Enter a string: ")

print("Original:", text)
print("Length:", len(text))
print("First character:", text[0])
print("Last character:", text[-1])
print("Reverse:", text[::-1])
print("First half:", text[:len(text)//2])
```

---

## 13. Important Concepts at a Glance

| Concept | Example |
|---|---|
| String | `"Python"` |
| Positive Index | `text[0]` |
| Negative Index | `text[-1]` |
| Length | `len(text)` |
| Slicing | `text[1:4]` |
| From Beginning | `text[:4]` |
| To End | `text[2:]` |
| Complete String | `text[:]` |
| Step | `text[::2]` |
| Reverse | `text[::-1]` |

---

## 14. Quick Quiz

### Q1. What is the first index in Python?

**Answer:** `0`

### Q2. What does `text[-1]` return?

**Answer:** The last character.

### Q3. What does `len(text)` return?

**Answer:** Number of characters in the string.

### Q4. What is the output?

```python
x = "Python"
print(x[1:4])
```

**Answer:**

```text
yth
```

### Q5. What is the output?

```python
x = "Python"
print(x[::-1])
```

**Answer:**

```text
nohtyP
```

### Q6. What type of value does `input()` return?

**Answer:** `str`

---

## 15. Homework

Write programs for:

1. Take a name and print its first and last character.
2. Take a word and print it in reverse.
3. Take a sentence and print its length.
4. Take a string and print its first 4 and last 4 characters.
5. Take a string and print characters at even indexes.

### Challenge

Write a program that produces output like:

```text
Enter a word: programming

Original: programming
Length: 11
First character: p
Last character: g
Reverse: gnimmargorp
First 5: progr
Last 5: mming
```

---

## Day 16 Key Takeaways

```text
Indexing       -> text[0]
Negative Index -> text[-1]
Length         -> len(text)
Slicing        -> text[start:end]
Reverse        -> text[::-1]
```

> **Golden Rule:** Python strings are sequences, and indexing starts from `0`.
