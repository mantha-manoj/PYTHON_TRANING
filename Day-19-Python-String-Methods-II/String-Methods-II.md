# Day 19 — String Methods II

**Duration:** 1 Hour 30 Minutes  
**Topic:** Cleaning, splitting, joining, and counting strings

## Learning Objectives

By the end of this class, you should understand:

- `split()` — convert a string into a list
- `strip()` — remove unwanted spaces
- `join()` — convert a list into a string
- `count()` — count occurrences in a string
- How to combine multiple string methods in a practical program

---

## 1. `split()` Method

The `split()` method breaks a string into a list.

### Example

```python
names = "Pavan,Ravi,Sita,John"

result = names.split(",")

print(result)
```

### Output

```text
['Pavan', 'Ravi', 'Sita', 'John']
```

The value passed to `split()` tells Python where to split the string.

### More Examples

```python
text = "Python-Java-C++"

print(text.split("-"))
```

Output:

```text
['Python', 'Java', 'C++']
```

```python
text = "Python Java C++"

print(text.split(" "))
```

Output:

```text
['Python', 'Java', 'C++']
```

---

## 2. `strip()` Method

The `strip()` method removes unwanted spaces from the beginning and end of a string.

```python
name = "   Pavan   "

print(name)
print(name.strip())
```

Output:

```text
   Pavan   
Pavan
```

### Important

`strip()` does **not** remove spaces between words.

```python
name = "Pavan Tej"

print(name.strip())
```

Output:

```text
Pavan Tej
```

The space between `Pavan` and `Tej` remains.

---

## 3. Combining `split()` and `strip()`

Suppose the user enters:

```text
Pavan, Ravi,   Sita, John
```

If we only use `split()`:

```python
names = input("Enter names: ")

names = names.split(",")

print(names)
```

The result may contain unwanted spaces:

```text
['Pavan', ' Ravi', '   Sita', ' John']
```

We can clean each name using `strip()`:

```python
names = input("Enter names: ")

names = names.split(",")

clean_names = []

for name in names:
    clean_names.append(name.strip())

print(clean_names)
```

Output:

```text
['Pavan', 'Ravi', 'Sita', 'John']
```

---

## 4. `join()` Method

The `join()` method combines the elements of a list into a single string.

### Basic Syntax

```python
"separator".join(list)
```

### Example

```python
names = ["Pavan", "Ravi", "Sita", "John"]

result = " | ".join(names)

print(result)
```

Output:

```text
Pavan | Ravi | Sita | John
```

### Another Example

```python
words = ["Python", "is", "easy"]

sentence = " ".join(words)

print(sentence)
```

Output:

```text
Python is easy
```

### Remember

```text
split() → String → List
join()  → List → String
```

---

## 5. `count()` Method

The `count()` method tells us how many times a value occurs in a string.

```python
text = "python is easy and python is powerful"

print(text.count("python"))
```

Output:

```text
2
```

### Example

```python
text = "banana"

print(text.count("a"))
```

Output:

```text
3
```

---

## 6. `count()` Is Case-Sensitive

```python
text = "Python python PYTHON"

print(text.count("python"))
```

Output:

```text
1
```

Only lowercase `"python"` is counted.

For case-insensitive counting:

```python
text = "Python python PYTHON"

print(text.lower().count("python"))
```

Output:

```text
3
```

---

# 7. Main Program

### Problem

Take comma-separated names, clean spaces, join the names with ` | `, and count occurrences of a chosen name.

```python
names = input("Enter names separated by commas: ")

name_list = names.split(",")

clean_names = []

for name in name_list:
    clean_names.append(name.strip())

result = " | ".join(clean_names)

print("Names:", result)

search_name = input("Enter a name to count: ")

count = clean_names.count(search_name.strip())

print("Occurrences:", count)
```

### Sample Input

```text
Enter names separated by commas: Pavan, Ravi, Pavan, Sita, Ravi
Enter a name to count: Pavan
```

### Output

```text
Names: Pavan | Ravi | Pavan | Sita | Ravi
Occurrences: 2
```

---

# 8. Program Explanation

### Step 1 — Get input

```python
names = input("Enter names separated by commas: ")
```

Gets the complete comma-separated string from the user.

### Step 2 — Split the string

```python
name_list = names.split(",")
```

Converts the string into a list.

Example:

```text
"Pavan, Ravi, Sita"
```

becomes:

```python
["Pavan", " Ravi", " Sita"]
```

### Step 3 — Create an empty list

```python
clean_names = []
```

This list will store the cleaned names.

### Step 4 — Remove unwanted spaces

```python
for name in name_list:
    clean_names.append(name.strip())
```

Each name is cleaned before being added to the new list.

### Step 5 — Join the names

```python
result = " | ".join(clean_names)
```

Converts the cleaned list back into a single string.

### Step 6 — Ask for a name

```python
search_name = input("Enter a name to count: ")
```

Gets the name that the user wants to count.

### Step 7 — Count occurrences

```python
count = clean_names.count(search_name.strip())
```

Counts how many times the requested name appears in the list.

---

# 9. Practice Exercises

## Exercise 1 — Fruits

Take comma-separated fruits:

```text
Apple, Banana, Mango, Apple, Orange
```

Clean the spaces and display:

```text
Apple | Banana | Mango | Apple | Orange
```

Then ask the user for a fruit and count its occurrences.

---

## Exercise 2 — Programming Languages

Input:

```text
Python, Java, Python, C++, Java, Python
```

Ask:

```text
Enter language to count:
```

If the user enters:

```text
Python
```

Expected output:

```text
Python occurs 3 times
```

---

# 10. Challenge

Create a program that handles names without worrying about uppercase/lowercase differences.

### Example Input

```text
Enter names: pavan, Ravi, PAVAN, sita, pavan
Enter name to search: Pavan
```

Expected result:

```text
Pavan occurs 3 times
```

### Hint

Use:

```python
.lower()
```

Think about where you need to convert the names and search value to lowercase.

---

# 11. Quick Revision

| Method | Purpose | Example |
|---|---|---|
| `split()` | String → List | `"A,B".split(",")` |
| `strip()` | Remove spaces at beginning/end | `" A ".strip()` |
| `join()` | List → String | `" - ".join(items)` |
| `count()` | Count occurrences | `"banana".count("a")` |

## Key Takeaway

```text
split()  → String → List
strip()  → Removes unwanted spaces
join()   → List → String
count()  → Counts occurrences
```

---

# Day 19 Practice Checklist

- [ ] Understand `split()`
- [ ] Understand `strip()`
- [ ] Understand `join()`
- [ ] Understand `count()`
- [ ] Combine `split()` and `strip()`
- [ ] Convert a list back to a string using `join()`
- [ ] Count repeated values
- [ ] Complete the fruits exercise
- [ ] Complete the programming languages exercise
- [ ] Complete the case-insensitive challenge

---

**Previous:** Day 18 — String Methods I  
**Next:** Day 20 — Continue with the 45-Day Python Course
