# Day 17 – Python Strings II

## 📚 Topics Covered

- String indexing and slicing
- Reversing a string
- Palindrome checking
- `lower()` method
- Looping through strings
- Counting vowels
- Counting vowels and consonants
- Character checking with `isalpha()`
- Practice programs and challenge

---

## 1. String Indexing and Slicing

A string is a sequence of characters.

```python
name = "Python"

print(name[0])
print(name[1])
print(name[-1])
```

### Output

```text
P
y
n
```

### Reverse a String

Python allows us to reverse a string using slicing:

```python
name = "Python"

print(name[::-1])
```

### Output

```text
nohtyP
```

### Syntax

```python
string[start:stop:step]
```

To reverse:

```python
string[::-1]
```

---

## 2. What is a Palindrome?

A palindrome is a word or sequence that reads the same forward and backward.

### Examples

```text
madam
level
radar
racecar
121
```

### Not Palindromes

```text
python
hello
computer
```

---

## 3. Palindrome Program

```python
word = input("Enter a word: ")

reverse = word[::-1]

if word == reverse:
    print("Palindrome")
else:
    print("Not a palindrome")
```

### Example

```text
Enter a word: madam
Palindrome
```

---

## 4. Palindrome with `lower()`

Python is case-sensitive.

```python
print("Madam" == "madam")
```

Output:

```text
False
```

To ignore case:

```python
word = input("Enter a word: ")

word = word.lower()

if word == word[::-1]:
    print("Palindrome")
else:
    print("Not a palindrome")
```

### Important Method

```python
text.lower()
```

Converts all alphabetic characters to lowercase.

---

## 5. Reverse a String Using a Loop

A string can also be reversed without slicing.

```python
word = input("Enter a word: ")

reverse = ""

for ch in word:
    reverse = ch + reverse

print("Reverse:", reverse)
```

### Example

For:

```text
abc
```

The reverse becomes:

```text
cba
```

---

## 6. Count Vowels in a Sentence

The vowels are:

```text
a, e, i, o, u
```

We can use the `in` operator to check whether a character is a vowel.

```python
sentence = input("Enter a sentence: ")

count = 0

for ch in sentence.lower():
    if ch in "aeiou":
        count += 1

print("Number of vowels:", count)
```

### Example

```text
Enter a sentence: Python Programming
Number of vowels: 4
```

---

## 7. Why Use `lower()`?

Suppose the input is:

```text
PYTHON
```

Without converting to lowercase:

```python
"P" in "aeiou"
```

returns:

```text
False
```

Using:

```python
sentence.lower()
```

converts:

```text
PYTHON
```

to:

```text
python
```

Now vowels can be detected correctly.

---

## 8. Count Each Vowel Separately

```python
sentence = input("Enter a sentence: ")

a = 0
e = 0
i = 0
o = 0
u = 0

for ch in sentence.lower():
    if ch == 'a':
        a += 1
    elif ch == 'e':
        e += 1
    elif ch == 'i':
        i += 1
    elif ch == 'o':
        o += 1
    elif ch == 'u':
        u += 1

print("a =", a)
print("e =", e)
print("i =", i)
print("o =", o)
print("u =", u)
```

---

## 9. Count Vowels Using a Vowel String

A cleaner approach is:

```python
sentence = input("Enter a sentence: ")

vowels = "aeiou"
count = 0

for ch in sentence.lower():
    if ch in vowels:
        count += 1

print("Total vowels:", count)
```

### Important Operator

```python
ch in vowels
```

checks whether `ch` exists inside the string `vowels`.

Example:

```python
print('a' in "aeiou")
print('x' in "aeiou")
```

Output:

```text
True
False
```

---

## 10. Count Vowels and Consonants

```python
sentence = input("Enter a sentence: ")

vowels = 0
consonants = 0

for ch in sentence.lower():
    if ch in "aeiou":
        vowels += 1
    elif ch.isalpha():
        consonants += 1

print("Vowels:", vowels)
print("Consonants:", consonants)
```

### Why `isalpha()`?

```python
ch.isalpha()
```

checks whether a character is an alphabetic character.

Example:

```python
print('A'.isalpha())
print('5'.isalpha())
```

Output:

```text
True
False
```

This prevents spaces, numbers, and symbols from being counted as consonants.

---

# 🧪 Practice Programs

## Program 1 – Palindrome

Write a program that:

1. Takes a word from the user.
2. Reverses the word.
3. Checks whether it is a palindrome.

### Example

```text
Input: level
Output: Palindrome
```

---

## Program 2 – Vowel Counter

Take a sentence and count the total number of vowels.

### Example

```text
Input: I love Python
Output: 4
```

---

## Program 3 – Vowels and Consonants

Take a sentence and count:

- Number of vowels
- Number of consonants

Ignore spaces, numbers, and special characters.

---

## Program 4 – Case-Insensitive Palindrome

Check whether the following is a palindrome:

```text
Madam
```

Expected result:

```text
Palindrome
```

Hint:

```python
word = word.lower()
```

---

# 🔥 Day 17 Challenge

Create one program that displays all of the following:

```text
Enter a word: Madam

Original word: Madam
Reverse word: madaM
Palindrome: Yes
Vowels: 2
```

### Requirements

- Take input from the user.
- Display the original word.
- Reverse the word.
- Check whether it is a palindrome without considering case.
- Count the vowels.
- Display the results.

---

# 📝 Quick Revision

| Concept | Example |
|---|---|
| String length | `len(text)` |
| Reverse string | `text[::-1]` |
| Lowercase | `text.lower()` |
| Loop through string | `for ch in text` |
| Membership | `ch in "aeiou"` |
| Alphabet check | `ch.isalpha()` |
| String comparison | `word == reverse` |
| Increment counter | `count += 1` |

---

# 🎯 Key Takeaways

1. Strings can be accessed character by character.
2. `[::-1]` reverses a string.
3. A palindrome is the same forward and backward.
4. `lower()` helps perform case-insensitive comparisons.
5. `in` can check whether a character belongs to a string.
6. `isalpha()` checks whether a character is an alphabet.
7. Counters such as `count += 1` are useful for counting characters.
8. Loops are commonly used to process every character in a string.

---

## 🚀 Practice Goal

Before moving to Day 18, practice:

- 3 palindrome programs
- 3 vowel-counting programs
- 2 vowel/consonant programs
- 1 combined Day 17 challenge
