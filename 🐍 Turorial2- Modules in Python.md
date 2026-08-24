# 🐍  Modules in Python

> **📚 Python Programming |**  
> Learn how Python modules help organize, reuse, and manage code efficiently.

---

## 📌 2.1 Modules in Python

### 🔹 What is a Module?

Modules provide a way to organize your code logically. Instead of having all your code in a single file, you can split it into multiple modules based on their purpose.

For example, you might have:

- 📥 One module for handling **Input/Output operations**
- 🧮 Another module for **mathematical calculations**
- 📊 Another module for **data manipulation**

When you want to use functionality from a module, you can **import it** into your current program or another module.

This allows you to access and use the **functions, classes, and variables** defined within that module.

By importing a module, you can avoid writing the same code repeatedly and instead reuse the code defined in the module.

### 💡 Example: Creating and Importing a Module

Suppose we create a file called `calculator.py`:

```python
# calculator.py

def add(a, b):
    return a + b

def multiply(a, b):
    return a * b
```

Now we can import this module into another Python program:

```python
# main.py

import calculator

result1 = calculator.add(10, 20)
result2 = calculator.multiply(5, 4)

print("Addition:", result1)
print("Multiplication:", result2)
```

### 🖥️ Output

```text
Addition: 30
Multiplication: 20
```

---

# 🧩 2.2 Three Main Types of Modules

Python modules can be broadly classified into three types:

```text
                 📦 Python Modules
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
      Built-in      External     User-defined
      Modules       Modules        Modules
```

---

## 1️⃣ Built-in Modules

Built-in modules come **pre-installed with Python**.

They are part of the **standard library** and provide a wide range of functionalities.

Examples include:

| Module | Purpose |
|---|---|
| `math` | Mathematical operations |
| `random` | Generating random numbers |
| `datetime` | Working with dates and times |
| `os` | Operating-system-related operations |

Built-in modules are readily available for use without the need for additional installation.

### 💡 Example: `math`

```python
import math

number = 25

print("Square root:", math.sqrt(number))
print("Power:", math.pow(2, 3))
```

### 🖥️ Output

```text
Square root: 5.0
Power: 8.0
```

### 💡 Example: `random`

```python
import random

number = random.randint(1, 10)

print("Random number:", number)
```

Possible output:

```text
Random number: 7
```

> ⚠️ The random number can be different every time the program runs.

---

## 2️⃣ External Modules

External modules are modules created by **third-party developers** and are not part of Python's standard library.

They extend Python's capabilities by providing additional functionality for specific purposes.

External modules can be downloaded and installed using package managers such as **`pip` (Python Package Index)**.

Popular external modules include:

- 🔢 `numpy` — Numerical computations
- 🐼 `pandas` — Data manipulation and analysis
- 📊 `matplotlib` — Data visualization
- 🌐 `requests` — Making HTTP requests

### 💡 Example: NumPy

After installing NumPy:

```bash
pip install numpy
```

Python program:

```python
import numpy as np

numbers = np.array([10, 20, 30, 40, 50])

print("Array:", numbers)
print("Mean:", np.mean(numbers))
```

### 🖥️ Output

```text
Array: [10 20 30 40 50]
Mean: 30.0
```

### 💡 Example: Pandas

```python
import pandas as pd

data = {
    "Name": ["Ali", "Sara", "John"],
    "Marks": [85, 90, 78]
}

df = pd.DataFrame(data)

print(df)
```

---

## 3️⃣ User-Defined Modules

User-defined modules are modules created by **Python programmers themselves**.

They allow users to organize their code into separate files and reuse functionality across multiple programs.

User-defined modules can contain:

- Functions
- Classes
- Variables
- Other Python code

These can be imported and used in other Python scripts or modules.

### 💡 Example: User-Defined Module

Create a file named `student.py`:

```python
# student.py

name = "Rahul"

def display_student():
    print("Student Name:", name)
```

Now create another file named `main.py`:

```python
import student

student.display_student()
```

### 🖥️ Output

```text
Student Name: Rahul
```

---

# 💬 2.3 Comments in Python

Comments in Python are used to provide explanatory notes within the code that are **not executed** by the Python interpreter.

They are useful for:

- 📖 Improving code readability
- 📝 Leaving reminders
- 👨‍💻 Explaining code to other developers
- 🔍 Documenting the purpose of code

Python comments are denoted by the **hash symbol (`#`)** followed by the comment text.

Comments are meant for human readers and are not executed by the Python interpreter. Therefore, they have no impact on the program's functionality or performance.

---

# 📝 Types of Comments

Python primarily uses:

1. **Single-line Comments**
2. **Multi-line Comments**

---

## 1️⃣ Single-Line Comments

Single-line comments are used to add explanatory notes or comments on a single line of code.

They start with a hash symbol (`#`) and continue until the end of the line.

### 💡 Example

```python
# This is a single-line comment

x = 10  # Assigning a value to the variable x

print(x)
```

### 🖥️ Output

```text
10
```

Anything written after the hash symbol is considered a comment and is ignored by the Python interpreter.

### 🔍 Another Example

```python
# Calculate the total marks

marks1 = 80
marks2 = 90

total = marks1 + marks2

print(total)
```

---

# 2️⃣ Multi-Line Comments

Multi-line comments, also known as **block comments**, allow you to add comments that span multiple lines.

The source material notes that Python does not have a built-in syntax specifically for multi-line comments, but triple quotes can be used to create a string that is not assigned to a variable and therefore can function like a comment in this context.

### 💡 Example

```python
"""
This is a multi-line comment.

It can contain multiple lines
of explanatory text.
"""

x = 10

print(x)
```

### 🖥️ Output

```text
10
```

### 💡 Using Triple Single Quotes

```python
'''
This is another example
of a multi-line comment.

Multiple lines can be written here.
'''

name = "Python"

print(name)
```

### 🖥️ Output

```text
Python
```

> 💡 **Note:** Triple-quoted text is technically a string literal. It is commonly used for multi-line documentation/comments, especially when it is not assigned or otherwise used.

---

# 📦 2.4 What is `pip`?

## 🔹 Python Package Installer

In simple terms, **`pip` is a package manager for Python**.

When working with Python, you may need to use external libraries or modules that provide additional functionality beyond the standard library.

These libraries are often developed by the Python community and are available for anyone to use.

`pip` makes it easy to:

- 📥 Install packages
- 🔄 Manage packages
- 🗑️ Uninstall packages
- 🔍 Obtain packages from the Python Package Index (**PyPI**)

PyPI is a repository of Python packages maintained by the Python community.

---

## 💻 Installing a Package with `pip`

A package can be installed by running a simple command in the terminal or command prompt.

### Syntax

```bash
pip install package_name
```

### Example

```bash
pip install numpy
```

After installation, NumPy can be imported into a Python program:

```python
import numpy as np

numbers = np.array([1, 2, 3, 4, 5])

print(numbers)
```

### 🖥️ Output

```text
[1 2 3 4 5]
```

---

## 📌 Useful `pip` Commands

### Install a Package

```bash
pip install pandas
```

### Upgrade a Package

```bash
pip install --upgrade pandas
```

### Uninstall a Package

```bash
pip uninstall pandas
```

### Show Installed Packages

```bash
pip list
```

### Show Package Information

```bash
pip show numpy
```

---

# 🧠 Quick Revision

| Concept | Description | Example |
|---|---|---|
| 📦 Module | Organizes Python code logically | `import math` |
| 🐍 Built-in Module | Comes with Python | `math`, `random` |
| 🌐 External Module | Developed outside Python's standard library | `numpy`, `pandas` |
| 👨‍💻 User-Defined Module | Created by the programmer | `import student` |
| 💬 Comment | Explanation ignored by interpreter | `# comment` |
| 📝 Single-Line Comment | Comment on one line | `# This is a comment` |
| 📚 Multi-Line Comment | Comment spanning multiple lines | `""" ... """` |
| 📦 `pip` | Python package-management tool | `pip install numpy` |

---

# 🎯 Key Takeaways

- ✅ Modules help **organize Python code logically**.
- ✅ Modules allow **code reuse**.
- ✅ Python provides many **built-in modules**.
- ✅ External modules can extend Python's functionality.
- ✅ Programmers can create their own **user-defined modules**.
- ✅ Comments improve **code readability and documentation**.
- ✅ Single-line comments use `#`.
- ✅ Multi-line explanatory text can be written using triple quotes.
- ✅ `pip` is used to **install and manage Python packages**.
- ✅ **PyPI** provides a repository of Python packages.

---

## 🚀 Mini Practice Program

Try combining modules, comments, and functions in one program:

```python
# Import the built-in math module
import math

# Store a number
number = 64

# Calculate the square root
result = math.sqrt(number)

# Display the result
print("Square root of", number, "is:", result)
```

### Expected Output

```text
Square root of 64 is: 8.0
```

---

## 📚 Chapter Summary

```text
Python Modules
│
├── Built-in Modules
│   ├── math
│   ├── random
│   ├── datetime
│   └── os
│
├── External Modules
│   ├── numpy
│   ├── pandas
│   ├── matplotlib
│   └── requests
│
├── User-Defined Modules
│   └── Created by programmers
│
├── Comments
│   ├── Single-line
│   └── Multi-line
│
└── pip
    ├── Install
    ├── Upgrade
    ├── Uninstall
    └── Manage packages
```

