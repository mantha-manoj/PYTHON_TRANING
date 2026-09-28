# Day 35 – Advanced File Handling in Python

## Topics Covered
- File pointer
- `tell()`
- `seek()`
- Reading and processing file content
- Counting lines, words, and characters
- File handling practice programs

## 1. tell()
`tell()` returns the current position of the file pointer.

```python
with open("data.txt", "r") as file:
    print(file.tell())
    print(file.read(5))
    print(file.tell())
```

## 2. seek()
`seek()` moves the file pointer to a specified position.

```python
with open("data.txt", "r") as file:
    print(file.read(5))
    file.seek(0)
    print(file.read(5))
```

## 3. Count Lines, Words and Characters

```python
with open("data.txt", "r") as file:
    data = file.read()

print("Lines:", len(data.splitlines()))
print("Words:", len(data.split()))
print("Characters:", len(data))
```

## Practice Programs
1. Count vowels in a text file.
2. Count uppercase and lowercase characters.
3. Find the longest word in a file.
4. Use `seek()` to return to the beginning of a file.

## Quick Revision
- `tell()` → returns current file pointer position.
- `seek()` → moves the file pointer.
- `read()` → reads file content.
- `readlines()` → returns lines as a list.
