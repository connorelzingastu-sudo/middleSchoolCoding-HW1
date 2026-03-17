# Python File Reading with Loops 

## Goal

Today you will learn how to:

* Open a text file
* Read data from the file
* Use a loop to read every line
* Convert text into numbers
* Display results neatly

---

# Part 1: Create Your Text File

Create a file called:

`numbers.txt`

Put these values inside:

```txt
12
25
8
41
19
```

Save it in the same folder as your Python program.

---

# Part 2: Read One Line First

Start with this code:

```python
file = open("numbers.txt", "r")

line = file.readline()

print(line)

file.close()
```

## What happens?

✅ It opens the file
✅ Reads only the first line
✅ Prints it

---

# Part 3: Read Every Line with a While Loop

Now use a loop:

```python
file = open("numbers.txt", "r")

line = file.readline()

while line != "":
    print(line)
    line = file.readline()

file.close()
```

## Important Idea

The loop keeps running until Python reaches the end of the file.

When there are no more lines:

```python
line == ""
```

That means stop.

---

# Part 4: Clean Up Extra Spaces

You may notice blank lines appear.

Use `.strip()`:

```python
file = open("numbers.txt", "r")

line = file.readline()

while line != "":
    print(line.strip())
    line = file.readline()

file.close()
```

## Why?

`.strip()` removes:

* invisible spaces
* enter keys (`\n`)

---

# Part 5: Convert Text to Numbers

Everything in a file is read as text.

Convert each line:

```python
file = open("numbers.txt", "r")

line = file.readline()

while line != "":
    number = int(line)
    print(number)
    line = file.readline()

file.close()
```

---

# Part 6: Add a Running Total

Now total everything:

```python
file = open("numbers.txt", "r")

total = 0

line = file.readline()

while line != "":
    number = int(line)
    total += number
    line = file.readline()

file.close()

print("Total =", total)
```

---

# Challenge 🚀

Can you also find:

* largest number
* smallest number
* average

---

# Advanced Version (for loop style)

Python can read lines even easier:

```python
file = open("numbers.txt", "r")

for line in file:
    print(line.strip())

file.close()
```

---

# Exit Ticket 🎯

Answer:

1. Why do we use `line = file.readline()` before the loop?
2. What does `.strip()` do?
3. Why do we convert to `int()`?

---

# Bonus Challenge

Create your own file called:

`highscores.txt`

Add 5 game scores and calculate the total.

---
