# 🐍 10 Beginner Python Projects for Undergraduate Students

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Level](https://img.shields.io/badge/Level-Beginner-success)]()
[![Projects](https://img.shields.io/badge/Projects-10-orange)]()
[![License](https://img.shields.io/badge/License-Educational-lightgrey)]()

> A collection of **10 practical Python projects** designed for undergraduate students.  
> Each project introduces important Python programming concepts through a small, hands-on application.

---

## 📚 Table of Contents

- [🎯 Learning Goals](#-learning-goals)
- [🗂️ Project Roadmap](#️-project-roadmap)
- [1. Number Guessing Game](#1--number-guessing-game)
- [2. Arithmetic Formatter](#2--arithmetic-formatter)
- [3. Time Calculator](#3--time-calculator)
- [4. Student Grade Management](#4--student-grade-management)
- [5. Expense Tracker](#5--expense-tracker)
- [6. Budget App](#6--budget-app)
- [7. Inventory Management System](#7--inventory-management-system)
- [8. Polygon Area Calculator](#8--polygon-area-calculator)
- [9. Probability Calculator](#9--probability-calculator)
- [10. Shape Calculator](#10--shape-calculator)
- [📁 Repository Structure](#-repository-structure)
- [🚀 Getting Started](#-getting-started)

---

## 🎯 Learning Goals

After completing these projects, students should be able to:

- Understand Python syntax and program structure
- Work with variables, operators, and data types
- Use conditional statements and loops
- Write reusable functions
- Work with lists and dictionaries
- Handle user input and invalid data
- Perform file-based data management
- Understand Object-Oriented Programming (OOP)
- Implement inheritance and polymorphism
- Apply randomization and simulation
- Develop small command-line applications

---

## 🗂️ Project Roadmap

| # | Project | Main Concepts | Level |
|---|---|---|:---:|
| 01 | 🔢 Number Guessing Game | Random numbers, loops, conditions | ⭐ |
| 02 | ➕ Arithmetic Formatter | Strings, functions, validation | ⭐ |
| 03 | ⏰ Time Calculator | Functions, arithmetic, time conversion | ⭐⭐ |
| 04 | 🎓 Student Grade Management | Lists, dictionaries, functions | ⭐⭐ |
| 05 | 💰 Expense Tracker | Lists, dictionaries, data management | ⭐⭐ |
| 06 | 💳 Budget App | Classes, objects, methods | ⭐⭐⭐ |
| 07 | 📦 Inventory Management | CRUD, dictionaries, functions | ⭐⭐⭐ |
| 08 | 📐 Polygon Area Calculator | Classes, inheritance | ⭐⭐⭐ |
| 09 | 🎲 Probability Calculator | Randomization, simulation, probability | ⭐⭐⭐ |
| 10 | 📏 Shape Calculator | OOP, inheritance, polymorphism | ⭐⭐⭐ |

---

# 1. 🔢 Number Guessing Game

## 📌 Problem Description

Build a game that generates a random number between **1 and 100**. The user keeps guessing until the correct number is found.

The program should indicate whether the guess is **too high** or **too low** and count the number of attempts.

## 🎯 Objectives

- Generate random numbers
- Accept and validate user input
- Use conditional statements
- Implement a `while` loop
- Count attempts

## 🧠 Concepts Used

`random` · `input()` · `if/elif/else` · `while` · exception handling

## 💻 Complete Python Code

```python
import random

print("=" * 40)
print("       NUMBER GUESSING GAME")
print("=" * 40)

secret_number = random.randint(1, 100)
attempts = 0

while True:
    try:
        guess = int(input("Enter your guess (1-100): "))

        if guess < 1 or guess > 100:
            print("Please enter a number between 1 and 100.")
            continue

        attempts += 1

        if guess < secret_number:
            print("Too low! Try again.")
        elif guess > secret_number:
            print("Too high! Try again.")
        else:
            print("\n🎉 Congratulations!")
            print(f"You guessed the number in {attempts} attempts.")
            break

    except ValueError:
        print("Please enter a valid number.")
```

## ▶️ Sample Output

```text
========================================
       NUMBER GUESSING GAME
========================================

Enter your guess (1-100): 40
Too low! Try again.

Enter your guess (1-100): 75
Too high! Try again.

Enter your guess (1-100): 62
🎉 Congratulations!
You guessed the number in 3 attempts.
```

## 📝 Exercises

- [ ] Limit the player to 10 attempts.
- [ ] Add Easy, Medium, and Hard difficulty levels.
- [ ] Store the best score.
- [ ] Allow multiple rounds.
- [ ] Add a replay option.

---

# 2. ➕ Arithmetic Formatter

## 📌 Problem Description

Create a program that formats arithmetic problems vertically, similar to handwritten arithmetic.

Example:

```text
  123
+ 456
-----
  579
```

## 🎯 Objectives

- Work with strings
- Validate arithmetic problems
- Format output neatly
- Create reusable functions

## 🧠 Concepts Used

`functions` · `strings` · `lists` · `split()` · validation · formatting

## 💻 Complete Python Code

```python
def arithmetic_formatter(problems, show_answers=False):

    if len(problems) > 5:
        return "Error: Too many problems."

    first_line = []
    second_line = []
    dashes = []
    answers = []

    for problem in problems:

        parts = problem.split()

        if len(parts) != 3:
            return "Error: Invalid problem format."

        first, operator, second = parts

        if operator not in ["+", "-"]:
            return "Error: Operator must be '+' or '-'."

        if not first.isdigit() or not second.isdigit():
            return "Error: Numbers must only contain digits."

        if len(first) > 4 or len(second) > 4:
            return "Error: Numbers cannot be more than four digits."

        width = max(len(first), len(second)) + 2

        first_line.append(first.rjust(width))
        second_line.append(operator + second.rjust(width - 1))
        dashes.append("-" * width)

        if operator == "+":
            result = int(first) + int(second)
        else:
            result = int(first) - int(second)

        answers.append(str(result).rjust(width))

    output = (
        "    ".join(first_line)
        + "\n"
        + "    ".join(second_line)
        + "\n"
        + "    ".join(dashes)
    )

    if show_answers:
        output += "\n" + "    ".join(answers)

    return output


problems = [
    "123 + 456",
    "999 - 123",
    "45 + 55"
]

print(arithmetic_formatter(problems, True))
```

## ▶️ Sample Output

```text
  123      999       45
+ 456    - 123     + 55
-----    -----     ----
  579      876      100
```

## 📝 Exercises

- [ ] Add multiplication.
- [ ] Add division.
- [ ] Allow interactive problem entry.
- [ ] Support negative numbers.
- [ ] Add configurable problem limits.

---

# 3. ⏰ Time Calculator

## 📌 Problem Description

Create a program that adds a duration to a starting time.

Example:

```text
Start:    3:00 PM
Duration: 2:30

Result:   5:30 PM
```

The program should also identify when the result occurs on the next day or several days later.

## 🎯 Objectives

- Perform time calculations
- Convert between 12-hour and 24-hour formats
- Handle AM/PM
- Use functions effectively

## 🧠 Concepts Used

`functions` · arithmetic · strings · conditionals · integer division

## 💻 Complete Python Code

```python
def add_time(start, duration):

    start_parts = start.split()
    time_part = start_parts[0]
    period = start_parts[1].upper()

    start_hour, start_minute = map(int, time_part.split(":"))
    duration_hour, duration_minute = map(int, duration.split(":"))

    # Convert 12-hour time to 24-hour time
    if period == "PM" and start_hour != 12:
        start_hour += 12

    if period == "AM" and start_hour == 12:
        start_hour = 0

    total_minutes = (
        start_hour * 60
        + start_minute
        + duration_hour * 60
        + duration_minute
    )

    days_later = total_minutes // (24 * 60)
    total_minutes %= (24 * 60)

    final_hour = total_minutes // 60
    final_minute = total_minutes % 60

    final_period = "PM" if final_hour >= 12 else "AM"

    display_hour = final_hour % 12

    if display_hour == 0:
        display_hour = 12

    result = f"{display_hour}:{final_minute:02d} {final_period}"

    if days_later == 1:
        result += " (next day)"
    elif days_later > 1:
        result += f" ({days_later} days later)"

    return result


print(add_time("3:00 PM", "2:30"))
print(add_time("11:30 PM", "2:30"))
print(add_time("8:00 AM", "24:00"))
```

## ▶️ Sample Output

```text
5:30 PM
2:00 AM (next day)
8:00 AM (next day)
```

## 📝 Exercises

- [ ] Add seconds.
- [ ] Validate invalid times.
- [ ] Support 24-hour input.
- [ ] Build a digital clock.
- [ ] Add user interaction.

---

# 4. 🎓 Student Grade Management System

## 📌 Problem Description

Build a student management program that stores student marks and calculates:

- Total marks
- Percentage
- Grade

## 🎯 Objectives

- Store structured student data
- Calculate academic results
- Use lists and dictionaries
- Create reusable functions

## 🧠 Concepts Used

`lists` · `dictionaries` · `functions` · loops · conditions

## 💻 Complete Python Code

```python
students = {}


def calculate_result(marks):
    total = sum(marks.values())
    percentage = total / len(marks)

    if percentage >= 90:
        grade = "A+"
    elif percentage >= 80:
        grade = "A"
    elif percentage >= 70:
        grade = "B"
    elif percentage >= 60:
        grade = "C"
    elif percentage >= 50:
        grade = "D"
    else:
        grade = "F"

    return total, percentage, grade


def add_student():
    name = input("Enter student name: ")

    marks = {}
    subjects = ["Python", "Mathematics", "Data Science"]

    for subject in subjects:
        marks[subject] = float(
            input(f"Enter marks for {subject}: ")
        )

    students[name] = marks
    print("Student added successfully!")


def display_students():

    if not students:
        print("No student records found.")
        return

    for name, marks in students.items():

        total, percentage, grade = calculate_result(marks)

        print("\n" + "=" * 40)
        print(f"Name       : {name}")
        print(f"Marks      : {marks}")
        print(f"Total      : {total}")
        print(f"Percentage : {percentage:.2f}%")
        print(f"Grade      : {grade}")


while True:

    print("\n===== STUDENT MANAGEMENT SYSTEM =====")
    print("1. Add Student")
    print("2. Display Students")
    print("3. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        add_student()
    elif choice == "2":
        display_students()
    elif choice == "3":
        print("Program terminated.")
        break
    else:
        print("Invalid choice.")
```

## ▶️ Sample Output

```text
===== STUDENT MANAGEMENT SYSTEM =====

1. Add Student
2. Display Students
3. Exit

Enter choice: 1
Enter student name: Rahul
Enter marks for Python: 85
Enter marks for Mathematics: 78
Enter marks for Data Science: 91

Student added successfully!
```

## 📝 Exercises

- [ ] Add student roll number.
- [ ] Add attendance.
- [ ] Add more subjects.
- [ ] Find the class topper.
- [ ] Export records to CSV.

---

# 5. 💰 Expense Tracker

## 📌 Problem Description

Develop an expense tracker that allows users to record expenses, categorize them, calculate total spending, and view category-wise summaries.

## 🎯 Objectives

- Record expenses
- Categorize expenses
- Calculate totals
- Generate reports

## 🧠 Concepts Used

`lists` · `dictionaries` · `functions` · loops · exception handling

## 💻 Complete Python Code

```python
expenses = []


def add_expense():

    category = input("Enter category: ")
    description = input("Enter description: ")

    try:
        amount = float(input("Enter amount: "))

        expense = {
            "category": category,
            "description": description,
            "amount": amount
        }

        expenses.append(expense)
        print("Expense added successfully.")

    except ValueError:
        print("Invalid amount.")


def show_expenses():

    if not expenses:
        print("No expenses recorded.")
        return

    print("\n===== EXPENSE REPORT =====")

    total = 0

    for expense in expenses:

        print(
            f"{expense['category']} | "
            f"{expense['description']} | "
            f"₹{expense['amount']:.2f}"
        )

        total += expense["amount"]

    print("-" * 40)
    print(f"Total Expense: ₹{total:.2f}")


def category_summary():

    summary = {}

    for expense in expenses:

        category = expense["category"]

        summary[category] = (
            summary.get(category, 0)
            + expense["amount"]
        )

    print("\n===== CATEGORY SUMMARY =====")

    for category, amount in summary.items():
        print(f"{category}: ₹{amount:.2f}")


while True:

    print("\n===== EXPENSE TRACKER =====")
    print("1. Add Expense")
    print("2. Show Expenses")
    print("3. Category Summary")
    print("4. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        add_expense()
    elif choice == "2":
        show_expenses()
    elif choice == "3":
        category_summary()
    elif choice == "4":
        break
    else:
        print("Invalid choice.")
```

## ▶️ Sample Output

```text
===== EXPENSE TRACKER =====

1. Add Expense
2. Show Expenses
3. Category Summary
4. Exit

Enter choice: 1
Enter category: Food
Enter description: Lunch
Enter amount: 150

Expense added successfully.
```

## 📝 Exercises

- [ ] Add date and time.
- [ ] Save data to CSV.
- [ ] Create monthly reports.
- [ ] Find the highest expense.
- [ ] Visualize expenses using Matplotlib.

---

# 6. 💳 Budget App

## 📌 Problem Description

Create a budget application that supports deposits, withdrawals, balances, and transfers between spending categories.

## 🎯 Objectives

- Understand Object-Oriented Programming
- Create classes and objects
- Implement methods
- Manage financial transactions

## 🧠 Concepts Used

`classes` · `objects` · `methods` · lists · dictionaries

## 💻 Complete Python Code

```python
class Category:

    def __init__(self, name):
        self.name = name
        self.ledger = []

    def deposit(self, amount, description=""):
        self.ledger.append({
            "amount": amount,
            "description": description
        })

    def withdraw(self, amount, description=""):

        if self.check_funds(amount):
            self.ledger.append({
                "amount": -amount,
                "description": description
            })
            return True

        return False

    def get_balance(self):
        return sum(item["amount"] for item in self.ledger)

    def check_funds(self, amount):
        return amount <= self.get_balance()

    def transfer(self, amount, category):

        if self.withdraw(
            amount,
            f"Transfer to {category.name}"
        ):
            category.deposit(
                amount,
                f"Transfer from {self.name}"
            )
            return True

        return False

    def __str__(self):

        title = self.name.center(30, "*")
        output = title + "\n"

        for item in self.ledger:

            description = item["description"][:23]
            amount = f"{item['amount']:.2f}"

            output += (
                f"{description:<23}"
                f"{amount:>7}\n"
            )

        output += f"Total: {self.get_balance():.2f}"

        return output


food = Category("Food")
education = Category("Education")

food.deposit(1000, "Initial Deposit")
food.withdraw(250, "Groceries")
education.deposit(500, "Scholarship")
food.transfer(200, education)

print(food)
print()
print(education)
```

## ▶️ Sample Output

```text
*************Food**************
Initial Deposit          1000.00
Groceries                -250.00
Transfer to Education    -200.00
Total: 550.00

**********Education***********
Scholarship               500.00
Transfer from Food        200.00
Total: 700.00
```

## 📝 Exercises

- [ ] Add transaction dates.
- [ ] Add monthly budgets.
- [ ] Prevent invalid deposits.
- [ ] Generate budget summaries.
- [ ] Visualize category spending.

---

# 7. 📦 Inventory Management System

## 📌 Problem Description

Create an inventory management application that supports:

- Adding products
- Displaying products
- Searching products
- Updating stock
- Deleting products

## 🎯 Objectives

- Understand CRUD operations
- Manage product information
- Work with dictionaries
- Build menu-driven programs

## 🧠 Concepts Used

`dictionaries` · `functions` · CRUD · loops · exception handling

## 💻 Complete Python Code

```python
inventory = {}


def add_product():

    product_id = input("Enter product ID: ")
    name = input("Enter product name: ")

    try:
        price = float(input("Enter price: "))
        quantity = int(input("Enter quantity: "))

        inventory[product_id] = {
            "name": name,
            "price": price,
            "quantity": quantity
        }

        print("Product added successfully.")

    except ValueError:
        print("Invalid input.")


def display_inventory():

    if not inventory:
        print("Inventory is empty.")
        return

    print("\n===== INVENTORY =====")

    for product_id, product in inventory.items():

        print(
            f"ID: {product_id} | "
            f"Name: {product['name']} | "
            f"Price: ₹{product['price']:.2f} | "
            f"Stock: {product['quantity']}"
        )


def search_product():

    product_id = input("Enter product ID: ")

    if product_id in inventory:

        product = inventory[product_id]

        print("\nProduct Found")
        print(f"Name: {product['name']}")
        print(f"Price: ₹{product['price']:.2f}")
        print(f"Quantity: {product['quantity']}")

    else:
        print("Product not found.")


def update_stock():

    product_id = input("Enter product ID: ")

    if product_id in inventory:

        try:
            quantity = int(input("Enter new quantity: "))
            inventory[product_id]["quantity"] = quantity
            print("Stock updated.")

        except ValueError:
            print("Invalid quantity.")

    else:
        print("Product not found.")


def delete_product():

    product_id = input("Enter product ID: ")

    if product_id in inventory:
        del inventory[product_id]
        print("Product deleted.")
    else:
        print("Product not found.")


while True:

    print("\n===== INVENTORY MANAGEMENT =====")
    print("1. Add Product")
    print("2. Display Inventory")
    print("3. Search Product")
    print("4. Update Stock")
    print("5. Delete Product")
    print("6. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        add_product()
    elif choice == "2":
        display_inventory()
    elif choice == "3":
        search_product()
    elif choice == "4":
        update_stock()
    elif choice == "5":
        delete_product()
    elif choice == "6":
        break
    else:
        print("Invalid choice.")
```

## ▶️ Sample Output

```text
===== INVENTORY MANAGEMENT =====

1. Add Product
2. Display Inventory
3. Search Product
4. Update Stock
5. Delete Product
6. Exit

Enter choice: 1
Enter product ID: P101
Enter product name: Keyboard
Enter price: 850
Enter quantity: 20

Product added successfully.
```

## 📝 Exercises

- [ ] Add supplier information.
- [ ] Add low-stock alerts.
- [ ] Save inventory as JSON.
- [ ] Add product categories.
- [ ] Generate inventory reports.

---

# 8. 📐 Polygon Area Calculator

## 📌 Problem Description

Create classes for rectangles and squares. The program calculates area, perimeter, diagonal, and displays a text representation of the shape.

## 🎯 Objectives

- Understand classes and objects
- Implement inheritance
- Create reusable methods
- Apply mathematical operations

## 🧠 Concepts Used

`classes` · `objects` · inheritance · methods · `math`

## 💻 Complete Python Code

```python
import math


class Rectangle:

    def __init__(self, width, height):
        self.width = width
        self.height = height

    def set_width(self, width):
        self.width = width

    def set_height(self, height):
        self.height = height

    def get_area(self):
        return self.width * self.height

    def get_perimeter(self):
        return 2 * (self.width + self.height)

    def get_diagonal(self):
        return math.sqrt(
            self.width ** 2 +
            self.height ** 2
        )

    def get_picture(self):

        if self.width > 50 or self.height > 50:
            return "Too big for picture."

        return "\n".join(
            "*" * self.width
            for _ in range(self.height)
        )

    def __str__(self):
        return (
            f"Rectangle(width={self.width}, "
            f"height={self.height})"
        )


class Square(Rectangle):

    def __init__(self, side):
        super().__init__(side, side)

    def set_side(self, side):
        self.width = side
        self.height = side

    def __str__(self):
        return f"Square(side={self.width})"


rectangle = Rectangle(10, 5)

print(rectangle)
print("Area:", rectangle.get_area())
print("Perimeter:", rectangle.get_perimeter())
print("Diagonal:", rectangle.get_diagonal())

square = Square(5)

print("\n", square)
print("Area:", square.get_area())
print("Perimeter:", square.get_perimeter())
print(square.get_picture())
```

## ▶️ Sample Output

```text
Rectangle(width=10, height=5)
Area: 50
Perimeter: 30
Diagonal: 11.180339887498949

Square(side=5)
Area: 25
Perimeter: 20

*****
*****
*****
*****
*****
```

## 📝 Exercises

- [ ] Add a triangle class.
- [ ] Add a circle class.
- [ ] Add 3D shape calculations.
- [ ] Accept user input.
- [ ] Build a graphical version using Tkinter.

---

# 9. 🎲 Probability Calculator

## 📌 Problem Description

Create a probability simulation that randomly draws balls from a hat and estimates the probability of obtaining a specified combination.

This project introduces students to **Monte Carlo simulation**.

## 🎯 Objectives

- Generate random samples
- Simulate repeated experiments
- Estimate experimental probability
- Use classes

## 🧠 Concepts Used

`classes` · `lists` · `random` · loops · simulation · probability

## 💻 Complete Python Code

```python
import random


class Hat:

    def __init__(self, **kwargs):

        self.contents = []

        for color, count in kwargs.items():

            for _ in range(count):
                self.contents.append(color)

    def draw(self, number):

        if number >= len(self.contents):
            drawn = self.contents.copy()
            self.contents.clear()
            return drawn

        return random.sample(self.contents, number)


def experiment(
    hat,
    expected_balls,
    num_balls_drawn,
    num_experiments
):

    success_count = 0

    for _ in range(num_experiments):

        new_hat = Hat(
            red=3,
            blue=2,
            green=6
        )

        drawn = new_hat.draw(num_balls_drawn)

        success = True

        for color, count in expected_balls.items():

            if drawn.count(color) < count:
                success = False
                break

        if success:
            success_count += 1

    return success_count / num_experiments


hat = Hat(
    red=3,
    blue=2,
    green=6
)

probability = experiment(
    hat,
    {"red": 2, "green": 1},
    4,
    10000
)

print(
    f"Experimental probability: "
    f"{probability:.4f}"
)
```

## ▶️ Sample Output

```text
Experimental probability: 0.1237
```

> **Note:** The result will vary between executions because the experiment uses random sampling.

## 📝 Exercises

- [ ] Allow the user to specify experiments.
- [ ] Add more colors.
- [ ] Calculate theoretical probability.
- [ ] Compare theoretical and experimental results.
- [ ] Plot simulation results using Matplotlib.

---

# 10. 📏 Shape Calculator

## 📌 Problem Description

Build a shape calculator using Object-Oriented Programming. The program should support multiple shapes and calculate their areas and perimeters.

## 🎯 Objectives

- Understand inheritance
- Implement polymorphism
- Create reusable classes
- Work with mathematical formulas

## 🧠 Concepts Used

`classes` · inheritance · polymorphism · methods · `math`

## 💻 Complete Python Code

```python
import math


class Shape:

    def area(self):
        raise NotImplementedError(
            "Subclass must implement area()"
        )

    def perimeter(self):
        raise NotImplementedError(
            "Subclass must implement perimeter()"
        )


class Circle(Shape):

    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return math.pi * self.radius ** 2

    def perimeter(self):
        return 2 * math.pi * self.radius


class Rectangle(Shape):

    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

    def perimeter(self):
        return 2 * (
            self.length + self.width
        )


class Triangle(Shape):

    def __init__(
        self,
        base,
        height,
        side1,
        side2,
        side3
    ):
        self.base = base
        self.height = height
        self.side1 = side1
        self.side2 = side2
        self.side3 = side3

    def area(self):
        return 0.5 * self.base * self.height

    def perimeter(self):
        return (
            self.side1 +
            self.side2 +
            self.side3
        )


shapes = [
    Circle(5),
    Rectangle(10, 5),
    Triangle(6, 4, 5, 5, 6)
]


for shape in shapes:

    print("\nShape:", type(shape).__name__)
    print(f"Area: {shape.area():.2f}")
    print(f"Perimeter: {shape.perimeter():.2f}")
```

## ▶️ Sample Output

```text
Shape: Circle
Area: 78.54
Perimeter: 31.42

Shape: Rectangle
Area: 50.00
Perimeter: 30.00

Shape: Triangle
Area: 12.00
Perimeter: 16.00
```

## 📝 Exercises

- [ ] Add a square class.
- [ ] Add an ellipse.
- [ ] Add a trapezoid.
- [ ] Create a menu-driven interface.
- [ ] Build a Tkinter GUI.

---

# 📁 Repository Structure

A recommended GitHub repository structure is:

```text
python-10-beginner-projects/
│
├── README.md
│
├── 01-number-guessing-game/
│   ├── README.md
│   └── main.py
│
├── 02-arithmetic-formatter/
│   ├── README.md
│   └── main.py
│
├── 03-time-calculator/
│   ├── README.md
│   └── main.py
│
├── 04-student-grade-management/
│   ├── README.md
│   └── main.py
│
├── 05-expense-tracker/
│   ├── README.md
│   └── main.py
│
├── 06-budget-app/
│   ├── README.md
│   └── main.py
│
├── 07-inventory-management/
│   ├── README.md
│   └── main.py
│
├── 08-polygon-area-calculator/
│   ├── README.md
│   └── main.py
│
├── 09-probability-calculator/
│   ├── README.md
│   └── main.py
│
└── 10-shape-calculator/
    ├── README.md
    └── main.py
```

---

# 🚀 Getting Started

## 1️⃣ Install Python

Download and install Python 3.x from the official Python website.

## 2️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/python-10-beginner-projects.git
cd python-10-beginner-projects
```

## 3️⃣ Run a Project

For example:

```bash
cd 01-number-guessing-game
python main.py
```

On some systems:

```bash
python3 main.py
```

---

# 🧭 Recommended Learning Path

```text
Variables & Input
       ↓
Conditions & Loops
       ↓
Functions
       ↓
Strings & Validation
       ↓
Lists & Dictionaries
       ↓
Data Management
       ↓
Object-Oriented Programming
       ↓
Inheritance
       ↓
Simulation & Probability
       ↓
Polymorphism
```

### ⭐ From Beginner to Intermediate

**Projects 1–3**  
Build programming fundamentals.

**Projects 4–5**  
Practice data structures and application logic.

**Projects 6–8**  
Introduce Object-Oriented Programming.

**Projects 9–10**  
Apply simulation, inheritance, and polymorphism.

---

# 👨‍🎓 Suggested Student Assessment

| Component | Suggested Weight |
|---|---:|
| Program Execution | 20% |
| Code Quality | 20% |
| Problem Solving | 20% |
| Documentation | 15% |
| Additional Features | 15% |
| Viva / Demonstration | 10% |
| **Total** | **100%** |

---

# 💡 Project Extension Ideas

Students can make these beginner projects more advanced by adding:

- 🖥️ **Tkinter GUI**
- 🗄️ **SQLite database**
- 📄 **CSV/JSON data storage**
- 📊 **Matplotlib visualization**
- 🌐 **Flask web interface**
- 🔐 **User authentication**
- 🧪 **Unit testing**
- 📦 **Python package structure**
- 🐳 **Docker deployment**
- 🤖 **AI-assisted features**

---

# 🏆 Final Challenge

After completing all 10 projects, students should select **one project** and convert it into a complete mini-project.

### Suggested progression

```text
Basic CLI Program
       ↓
Functions
       ↓
File / Database Storage
       ↓
GUI or Web Interface
       ↓
Data Visualization
       ↓
Testing
       ↓
Documentation
       ↓
Final Mini Project
```

---

## 📜 License

This repository is intended for **educational and academic purposes**.

Students and instructors are welcome to modify, extend, and use these projects for learning and classroom activities.

---

## ⭐ Learning Philosophy

> **Don't just read Python code — write it, run it, modify it, break it, debug it, and improve it.**

**Happy Coding! 🐍🚀**
