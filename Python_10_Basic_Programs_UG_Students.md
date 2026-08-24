# 🐍 Python Programming — 10 Basic Programs for UG Students

> **🎓 Undergraduate Python Practical Guide**  
> A beginner-friendly collection of 10 Python programs covering variables, input/output, operators, conditional statements, loops, lists, and functions.

---

## 📚 Learning Objectives

After completing these programs, students should be able to:

- Understand basic Python syntax.
- Take input from users.
- Use variables and arithmetic operators.
- Apply `if-else` conditional statements.
- Use `for` loops and `range()`.
- Work with Python lists.
- Calculate totals and averages.
- Define and call functions.
- Use `return` statements.
- Develop simple problem-solving skills.

---

# 🟢 Program 1 — Add Two Numbers

### 📌 Description

This program accepts two numbers from the user and calculates their sum.

**Concepts Covered:** Variables, `input()`, `float()`, arithmetic operators, `print()`.

### 💻 Python Program

```python
# Program to add two numbers

num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

sum = num1 + num2

print("Sum =", sum)
```

### 🖥️ Sample Output

```text
Enter first number: 25
Enter second number: 15
Sum = 40.0
```

---

# 🟢 Program 2 — Check Even or Odd

### 📌 Description

This program determines whether a number entered by the user is **even or odd**. The modulus operator `%` is used to find the remainder after division by 2.

**Concepts Covered:** `if-else`, modulus operator `%`, user input, integer conversion.

### 💻 Python Program

```python
number = int(input("Enter a number: "))

if number % 2 == 0:
    print("The number is Even")
else:
    print("The number is Odd")
```

### 🖥️ Sample Output

```text
Enter a number: 17
The number is Odd
```

---

# 🟢 Program 3 — Find the Largest of Three Numbers

### 📌 Description

This program accepts three numbers and determines which one is the largest using conditional statements.

**Concepts Covered:** `if`, `elif`, `else`, comparison operators, logical operator `and`.

### 💻 Python Program

```python
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
c = float(input("Enter third number: "))

if a >= b and a >= c:
    largest = a
elif b >= a and b >= c:
    largest = b
else:
    largest = c

print("Largest number =", largest)
```

### 🖥️ Sample Output

```text
Enter first number: 25
Enter second number: 42
Enter third number: 18

Largest number = 42.0
```

---

# 🟢 Program 4 — Print a Multiplication Table

### 📌 Description

This program accepts a number and prints its multiplication table from 1 to 10 using a `for` loop.

**Concepts Covered:** `for` loop, `range()`, arithmetic operators, variables.

### 💻 Python Program

```python
number = int(input("Enter a number: "))

print("Multiplication Table of", number)

for i in range(1, 11):
    result = number * i
    print(number, "×", i, "=", result)
```

### 🖥️ Sample Output

```text
Enter a number: 5

Multiplication Table of 5

5 × 1 = 5
5 × 2 = 10
5 × 3 = 15
5 × 4 = 20
5 × 5 = 25
5 × 6 = 30
5 × 7 = 35
5 × 8 = 40
5 × 9 = 45
5 × 10 = 50
```

---

# 🟢 Program 5 — Sum of Numbers from 1 to N

### 📌 Description

This program calculates the sum of all integers from `1` up to a number `N` entered by the user.

**Concepts Covered:** `for` loop, `range()`, accumulator variable, arithmetic operators.

### 💻 Python Program

```python
n = int(input("Enter the value of N: "))

total = 0

for i in range(1, n + 1):
    total = total + i

print("Sum =", total)
```

### 🖥️ Sample Output

```text
Enter the value of N: 10
Sum = 55
```

---

# 🟡 Program 6 — Find the Factorial of a Number

### 📌 Description

The factorial of a positive integer `n` is the product of all positive integers from `1` to `n`.

For example: `5! = 5 × 4 × 3 × 2 × 1 = 120`

**Concepts Covered:** `for` loop, variables, multiplication, accumulator variable.

### 💻 Python Program

```python
n = int(input("Enter a number: "))

factorial = 1

for i in range(1, n + 1):
    factorial = factorial * i

print("Factorial =", factorial)
```

### 🖥️ Sample Output

```text
Enter a number: 5
Factorial = 120
```

---

# 🟡 Program 7 — Check Whether a Number is Prime

### 📌 Description

A prime number is a number greater than 1 that has no positive divisors other than 1 and itself.

This program checks whether the number entered by the user is prime.

**Concepts Covered:** `if-else`, `for` loop, modulus operator `%`, Boolean variable, `break`.

### 💻 Python Program

```python
n = int(input("Enter a number: "))

if n <= 1:
    print("Not a Prime Number")
else:
    is_prime = True

    for i in range(2, n):
        if n % i == 0:
            is_prime = False
            break

    if is_prime:
        print("Prime Number")
    else:
        print("Not a Prime Number")
```

### 🖥️ Sample Output

```text
Enter a number: 17
Prime Number
```

---

# 🟡 Program 8 — Find the Largest Element in a List

### 📌 Description

This program stores several numbers in a list and finds the largest element by traversing the list with a `for` loop.

**Concepts Covered:** Lists, indexing, `for` loop, comparison, variables.

### 💻 Python Program

```python
numbers = [12, 45, 7, 89, 34, 23]

largest = numbers[0]

for number in numbers:
    if number > largest:
        largest = number

print("List:", numbers)
print("Largest element:", largest)
```

### 🖥️ Sample Output

```text
List: [12, 45, 7, 89, 34, 23]
Largest element: 89
```

---

# 🟡 Program 9 — Calculate Sum and Average of List Elements

### 📌 Description

This program calculates the **total** and **average** of the numbers stored in a list.

**Formula:** `Average = Total / Number of Elements`

**Concepts Covered:** Lists, `for` loop, `len()`, arithmetic operations, accumulator variable.

### 💻 Python Program

```python
marks = [75, 80, 65, 90, 85]

total = 0

for mark in marks:
    total = total + mark

average = total / len(marks)

print("Marks:", marks)
print("Total =", total)
print("Average =", average)
```

### 🖥️ Sample Output

```text
Marks: [75, 80, 65, 90, 85]
Total = 395
Average = 79.0
```

---

# 🟠 Program 10 — Calculate Square Using a Function

### 📌 Description

This program demonstrates how to create and use a Python function. The function accepts a number as a parameter and returns its square.

**Concepts Covered:** Functions, parameters, `return`, function calling, variables.

### 💻 Python Program

```python
def square(number):
    return number * number

n = int(input("Enter a number: "))

result = square(n)

print("Square =", result)
```

### 🖥️ Sample Output

```text
Enter a number: 8
Square = 64
```

---

# 📊 Concepts Covered

| No. | Program | Main Concepts | Difficulty |
|---:|---|---|:---:|
| 1 | Add Two Numbers | Variables, Input, Operators | 🟢 Basic |
| 2 | Even or Odd | `if-else`, `%` | 🟢 Basic |
| 3 | Largest of Three | Conditions, `and` | 🟢 Basic |
| 4 | Multiplication Table | `for`, `range()` | 🟢 Basic |
| 5 | Sum from 1 to N | Loop, Accumulator | 🟢 Basic |
| 6 | Factorial | Loop, Accumulator | 🟡 Intermediate |
| 7 | Prime Number | Loop, Condition, `break` | 🟡 Intermediate |
| 8 | Largest List Element | List, Loop, Comparison | 🟡 Intermediate |
| 9 | List Sum & Average | List, Loop, `len()` | 🟡 Intermediate |
| 10 | Square Using Function | Function, Parameter, `return` | 🟠 Intermediate |

---

# 📝 Practice Questions

1. Modify Program 1 to calculate sum, difference, product, and quotient.
2. Modify Program 2 to check whether a number is positive, negative, or zero.
3. Modify Program 3 to find the smallest of three numbers.
4. Modify Program 4 to allow the user to specify the starting and ending values.
5. Modify Program 5 to calculate the sum of even numbers from 1 to `N`.
6. Modify Program 6 using a `while` loop.
7. Modify Program 7 to print all prime numbers between `1` and `N`.
8. Modify Program 8 to find both the largest and smallest elements.
9. Modify Program 9 to calculate total, average, maximum, and minimum.
10. Modify Program 10 to create functions for square, cube, and fourth power.

---

# 🎯 Key Takeaways

- 🐍 Variables store data.
- 📥 `input()` accepts data from users.
- ⚙️ Operators perform calculations and comparisons.
- 🔀 Conditional statements control decisions.
- 🔁 Loops repeat a block of code.
- 📋 Lists store collections of values.
- 🧮 Accumulator variables are useful for totals and calculations.
- 🧩 Functions make code reusable and organized.

---

## 🚀 Learning Path

```text
Basic Python
     ↓
Strings
     ↓
Lists & Tuples
     ↓
Sets & Dictionaries
     ↓
Functions
     ↓
Modules
     ↓
File Handling
     ↓
NumPy
     ↓
Pandas
     ↓
Data Visualization
     ↓
Data Science & AI
```

> ⭐ **For UG Data Science & AI students:** These programs provide a foundation before moving into NumPy, Pandas, data analysis, visualization, machine learning, and AI.
