# 🐍 Python Basics to Advanced — Control Flow

> **Control Flow** directs program execution through structures like loops, conditionals, and functions, determining the order and path of operations.

---

## 📚 Table of Contents

- [5.1 Control Flow](#51-control-flow)
- [If Statements](#if-statements)
- [Else and Elif Statements](#else-and-elif-statements)
- [Nested If Statement](#nested-if-statement)
- [The While Loop](#the-while-loop)
- [The For Loop](#the-for-loop)
- [Loop Control Statements](#loop-control-statements)
  - [break](#break)
  - [continue](#continue)
- [Using range() in For Loop](#using-range-in-for-loop)
- [Quick Revision](#quick-revision)

---

# 5.1 Control Flow

Control Flow directs program execution through structures like loops, conditionals, and functions, determining the order and path of operations.

---

# 🟢 If Statements

An `if` statement in Python checks whether a condition is true or false. If the condition is true, the code inside the `if` block runs. If false, the code is skipped. It's used to make decisions in the program, executing specific actions based on conditions.

### Example

```python
age = 18

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")
```

### Output

```text
You are an adult
```

### 💡 Another Example

```python
marks = 75

if marks >= 40:
    print("Pass")
```

**Output:**

```text
Pass
```

---

# 🔵 Else and Elif Statements

In Python, `else` and `elif` statements are used alongside `if` to handle multiple conditions and alternative options.

### `elif` — Else If

`elif` checks another condition if the previous `if` was false. You can have multiple `elif` statements.

### `else`

`else` runs when none of the `elif` or `if` conditions are true. It is the default action.

### Example

```python
temperature = 75

if temperature > 85:
    print("It is too hot outside")

elif temperature >= 75:
    print("It is a nice day")

elif temperature > 50:
    print("It is a bit chilly")

else:
    print("It is cold outside")
```

### Output

```text
It is a nice day
```

### 💡 Another Example

```python
marks = 82

if marks >= 90:
    print("Grade A+")

elif marks >= 75:
    print("Grade A")

elif marks >= 60:
    print("Grade B")

else:
    print("Needs Improvement")
```

**Output:**

```text
Grade A
```

---

# 🟣 Nested If Statement

A nested `if` statement in Python is an `if` statement inside an `if`. It lets you check multiple related conditions in sequence.

### Example

If you first check the weather and it is sunny, you can then check how many guests are coming. Depending on the number of guests, you decide between different activities, like a barbecue or picnic.

If the weather isn't sunny, you skip the nested checks and go straight to an alternative action, like staying indoors.

```python
temperature = 75
humidity = 65

if temperature > 70:
    print("The weather is warm")

    if humidity > 60:
        print("It is also quite humid.")
    else:
        print("The humidity is low-")
else:
    print("The weather is cool")
```

### Output

```text
The weather is warm
It is also quite humid.
```

### 💡 Another Example

```python
age = 20
has_id = True

if age >= 18:
    if has_id:
        print("Entry allowed")
    else:
        print("Please show your ID")
else:
    print("Entry not allowed")
```

**Output:**

```text
Entry allowed
```

---

# 🔄 The While Loop

A `while` loop in Python repeatedly executes a block of code as long as a specified condition is true.

It first checks the condition. If the condition is true, the code inside runs. After each iteration, the condition is checked again. The loop continues until the condition becomes false.

A `while` loop can keep counting up as long as the count is below a certain number. It is useful for scenarios where you don't know in advance how many iterations are needed.

### Example

```python
count = 0

while count < 5:
    print("Count is", count)
    count += 1

print("Loop ended")
```

### Output

```text
Count is 0
Count is 1
Count is 2
Count is 3
Count is 4
Loop ended
```

### 💡 Another Example

```python
number = 1

while number <= 3:
    print("Number:", number)
    number += 1
```

**Output:**

```text
Number: 1
Number: 2
Number: 3
```

---

# 🔁 The For Loop

A `for` loop in Python is used to iterate over a sequence such as a list, tuple, or `range`, executing a block of code for each item in the sequence.

Unlike a `while` loop which runs until a condition is false, a `for` loop runs a set number of times based on the length of the sequence.

### Example

It can go through a list of numbers, processing each one. It is useful for iterating over data collections.

```python
Fruits = ["apple", "banana", "cherry"]

for fruit in Fruits:
    print(fruit)

print("Loop ended")
```

### Output

```text
apple
banana
cherry
Loop ended
```

---

# 🎛️ Loop Control Statements

Loop Control Statements in Python allow you to alter the flow of loop execution. They include:

- `break`
- `continue`

---

# 🛑 `break`

This statement immediately exits the loop, regardless of whether the loop's condition is still true. It's useful for stopping a loop when a specific condition is met, like when searching for an item in a list and finding it before the loop has iterated through the entire list.

### Example

```python
for i in range(10):
    if i == 5:
        break
    print("Current number:", i)

print("Loop ended")
```

### Output

```text
Current number: 0
Current number: 1
Current number: 2
Current number: 3
Current number: 4
Loop ended
```

### 💡 Another Example

```python
numbers = [10, 20, 30, 40, 50]

for number in numbers:
    if number == 30:
        break
    print(number)
```

**Output:**

```text
10
20
```

---

# ⏭️ `continue`

This statement skips the rest of the current loop iteration and proceeds to the next iteration. It's helpful for bypassing certain parts of the loop based on a condition, like skipping even numbers in a loop that processes a range of numbers.

### Example

```python
for i in range(10):
    if i % 2 == 0:
        continue
    print("Odd number:", i)

print("Loop ended")
```

### Output

```text
Odd number: 1
Odd number: 3
Odd number: 5
Odd number: 7
Odd number: 9
Loop ended
```

---

# 🔢 Using `range()` in For Loop

The `range()` function in Python is commonly used in `for` loops to iterate over a sequence of numbers.

### Example

```python
for i in range(5):
    print("Number:", i)
```

### Output

```text
Number: 0
Number: 1
Number: 2
Number: 3
Number: 4
```

---

## 📌 How `range()` Works

Here's a basic rundown of how it works:

### `start`

The starting value of the sequence **(inclusive)**.

If omitted, it defaults to `0`.

### `stop`

The ending value of the sequence **(exclusive)**.

The loop will run until it reaches this value.

### `step`

The amount by which the sequence is incremented.

If omitted, it defaults to `1`.

### Syntax

```python
range(start, stop, step)
```

---

## 🔽 Using a Negative Step

You can use `range()` with a negative step to count backwards.

### Example

```python
for i in range(10, 0, -1):
    print("Number:", i)
```

### Output

```text
Number: 10
Number: 9
Number: 8
Number: 7
Number: 6
Number: 5
Number: 4
Number: 3
Number: 2
Number: 1
```

---

# 🧪 More `range()` Examples

## Example 1 — Start and Stop

```python
for i in range(2, 6):
    print(i)
```

**Output:**

```text
2
3
4
5
```

## Example 2 — Start, Stop and Step

```python
for i in range(2, 11, 2):
    print(i)
```

**Output:**

```text
2
4
6
8
10
```

## Example 3 — Countdown

```python
for i in range(5, 0, -1):
    print(i)
```

**Output:**

```text
5
4
3
2
1
```

---

# 📊 Quick Revision

| Concept | Purpose | Example |
|---|---|---|
| `if` | Makes a decision based on a condition | `if age >= 18:` |
| `elif` | Checks another condition | `elif marks >= 75:` |
| `else` | Executes the default action | `else:` |
| Nested `if` | Checks conditions inside another condition | `if age >= 18: if has_id:` |
| `while` | Repeats while a condition is true | `while count < 5:` |
| `for` | Iterates over a sequence | `for item in items:` |
| `break` | Immediately exits a loop | `if x == 5: break` |
| `continue` | Skips the current iteration | `if x % 2 == 0: continue` |
| `range()` | Generates a sequence of numbers | `range(5)` |

---

# 🎯 Key Takeaways

- **Control flow** determines the order and path of program execution.
- The **`if` statement** is used for decision-making.
- **`elif`** allows multiple conditions to be checked.
- **`else`** provides a default action when conditions are false.
- A **nested `if`** places one conditional statement inside another.
- A **`while` loop** repeatedly executes code while a condition remains true.
- A **`for` loop** iterates over a sequence.
- **`break`** immediately terminates a loop.
- **`continue`** skips the current iteration and moves to the next one.
- **`range()`** is commonly used to generate number sequences for `for` loops.

---

# 📝 Practice Questions

### Beginner

1. Write a program to check whether a number is positive or negative.
2. Write a program to check whether a student has passed or failed.
3. Write a program to print numbers from 1 to 10 using a `while` loop.
4. Write a program to print the first 10 natural numbers using a `for` loop.
5. Write a program to print only even numbers from 1 to 20.

### Intermediate

6. Write a program to find the largest of three numbers using `if-elif-else`.
7. Write a program to print the multiplication table of a number using a `for` loop.
8. Use `break` to stop a loop when the number 7 is reached.
9. Use `continue` to skip multiples of 3.
10. Use `range()` to print numbers from 20 down to 1.

---

# 🚀 Learning Path

```text
Variables & Data Types
        ↓
Operators
        ↓
Conditional Statements
        ↓
if / elif / else
        ↓
Nested if
        ↓
while Loop
        ↓
for Loop
        ↓
break / continue
        ↓
range()
        ↓
Functions
        ↓
Advanced Python
```

---

> **📖 Source note:** The chapter title, explanations, examples, terminology, and organization above are based on the uploaded handwritten material. Formatting, headings, Markdown styling, and additional student-friendly examples have been added without changing the core learning content.
