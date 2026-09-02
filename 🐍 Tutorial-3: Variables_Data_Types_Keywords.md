# 🐍 Tutorial 3 — Variables, Data Types & Keywords in Python

> **Python Programming | Tutorial 3**  
> A practical introduction to variables, identifiers, data types, and keywords in Python.

---

## 📌 3.1 Variables in Python

In Python, variables are used to store values that can be used later in a program. You can think of variables as **containers that hold data**.

What makes Python unique is that you don't need to explicitly declare the type of a variable. You simply assign a value to it using the `=` operator.

For example, you can create a variable called `name` and assign a value to it.

Here, `name` is the variable name and `"Yagnesh"` is the value assigned to it. Python will automatically determine the type of the variable based on the value assigned to it.

### 💡 Example

```python
name = "Yagnesh"
age = 25

print(name)
print(age)
```

### 🖥️ Output

```text
Yagnesh
25
```

---

## 🔄 Changing the Value of a Variable

Variables in Python can hold different types of data, such as numbers, strings, lists, or even more complex objects.

You can change the value of a variable at any time by assigning a new value to it.

For instance:

```python
x = 5

# Updating the value
x = 3

print(x)
```

### 🖥️ Output

```text
3
```

---

## ➕➖✖️➗ Operations on Variables

Python also allows you to perform operations on variables.

You can:

- ➕ Add variables
- ➖ Subtract variables
- ✖️ Multiply variables
- ➗ Divide variables
- 🔗 Combine variables containing different types using appropriate operators

### 💡 Example

```python
x = 5
y = 3

z = x * y

greeting = "Hello"
name = "John"

message = greeting + " " + name

print("Value of z:", z)
print("Message:", message)
```

### 🖥️ Output

```text
Value of z: 15
Message: Hello John
```

---

# 🔑 3.1.1 Identifiers in Python

Variables provide a way to store and manipulate data in Python, making it easier to work with information throughout your program.

In Python, an **identifier** is a name used to identify a variable, function, class, module, or any other user-defined object.

An identifier can be made up of:

- Letters — uppercase and lowercase
- Digits
- Underscores (`_`)

However, it must start with a **letter or an underscore**.

---

## 📋 Important Rules for Identifiers

### 1️⃣ Valid Characters

Identifiers can contain:

- Letters (`a-z`, `A-Z`)
- Digits (`0-9`)
- Underscores (`_`)

### 2️⃣ Case Sensitivity

Python is **case-sensitive**.

This means uppercase and lowercase letters are considered different.

For example:

```python
Name = "Ali"
name = "Sara"

print(Name)
print(name)
```

`Name` and `name` are treated as two different identifiers.

### 3️⃣ Reserved Words

Python has reserved words, also known as **keywords**, that have predefined meanings in the language.

These words cannot be used as identifiers.

Examples include:

- `if`
- `while`
- `def`

### 4️⃣ Spaces and Special Characters

Identifiers cannot contain spaces or special characters such as `#` or `$`.

### 5️⃣ Length

Identifiers can be of any length. However, it is recommended to use meaningful and descriptive names that are not excessively long.

### 6️⃣ Readability

It is good practice to choose descriptive names for identifiers that convey their purpose or meaning. This makes the code more readable and understandable.

---

## ✅ Examples of Valid Identifiers

```python
my_variable = 10
count = 5
total_sum = 100
_my_value = 20
MyClass = "Example"
```

---

## ❌ Examples of Invalid Identifiers

```python
123abc = 10       # Starts with a digit
my-variable = 20  # Contains a hyphen
if = 5            # Reserved keyword
my variable = 10  # Contains a space
```

---

# 📦 3.2 Data Types in Python

Data types in Python refer to the different kinds of values that can be assigned to variables.

They determine the nature of the data and the operations that can be performed on them.

Python provides several built-in data types.

---

# 🔢 1. Numeric Data Types

Python supports different numerical data types, including:

- **Integer (`int`)**
- **Floating-point (`float`)**
- **Complex (`complex`)**

---

## 🔹 Integer (`int`)

Integers represent whole numbers without any fractional part.

### 💡 Example

```python
age = 25
temperature = -5

print(age)
print(temperature)
```

### 🖥️ Output

```text
25
-5
```

---

## 🔹 Floating-Point Numbers (`float`)

Floating-point numbers represent numbers with decimal parts or fractions.

For example, `pi = 3.14`.

### 💡 Example

```python
pi = 3.14
price = 99.50

print(pi)
print(price)
```

### 🖥️ Output

```text
3.14
99.5
```

---

## 🔹 Complex Numbers (`complex`)

Complex numbers have real and imaginary parts.

They are represented using a combination of a real number and an imaginary number, using `j`.

### 💡 Example

```python
z = 3 + 4j

print(z)
print("Real part:", z.real)
print("Imaginary part:", z.imag)
```

### 🖥️ Output

```text
(3+4j)
Real part: 3.0
Imaginary part: 4.0
```

---

# 🔘 2. Boolean (`bool`)

Booleans represent two values:

- `True`
- `False`

They are used for logical operations and conditions.

### 💡 Example

```python
is_valid = True
is_logged_in = False

print(is_valid)
print(is_logged_in)
```

### 🖥️ Output

```text
True
False
```

### 💡 Boolean with a Condition

```python
age = 20

is_adult = age >= 18

print(is_adult)
```

### 🖥️ Output

```text
True
```

---

# 🔤 3. Sequence Types

Sequences represent a collection of elements.

They include data types such as:

- **Strings**
- **Lists**
- **Tuples**

Strings are used to store textual data, while lists and tuples are used to store ordered collections.

---

## 🔹 String (`str`)

Strings are sequences of characters and are used for textual data.

They are enclosed within single or double quotes.

### 💡 Example

```python
name = "John"
message = 'Hello Python'

print(name)
print(message)
```

### 🖥️ Output

```text
John
Hello Python
```

---

## 🔹 List (`list`)

Lists are ordered sequences of elements enclosed in square brackets.

Each element can be of any data type.

### 💡 Example

```python
numbers = [1, 2, 3, 4]

print(numbers)
print(numbers[0])
```

### 🖥️ Output

```text
[1, 2, 3, 4]
1
```

### ✏️ Modifying a List

```python
numbers = [1, 2, 3]

numbers[0] = 10

print(numbers)
```

### 🖥️ Output

```text
[10, 2, 3]
```

---

## 🔹 Tuple (`tuple`)

Tuples are similar to lists but are **immutable**, meaning their elements cannot be changed once defined.

They are enclosed in parentheses.

For example:

```python
coordinates = (3, 4)

print(coordinates)
```

### 🖥️ Output

```text
(3, 4)
```

### 💡 Tuple Example

```python
coordinates = (3, 4)

print("X:", coordinates[0])
print("Y:", coordinates[1])
```

---

# 🟢 4. Set (`set`)

Sets are unordered collections of unique elements.

They are enclosed in curly braces.

Sets are useful for mathematical operations such as:

- Union
- Intersection
- Difference

### 💡 Example

```python
fruits = {"apple", "banana", "orange"}

print(fruits)
```

> ⚠️ Because sets are unordered collections, the display order may vary.

### 💡 Set Operations

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

print("Union:", A | B)
print("Intersection:", A & B)
print("Difference:", A - B)
```

---

# 🗂️ 5. Dictionary (`dict`)

Dictionaries are collections of **key-value pairs**.

Each value is associated with a unique key, allowing efficient lookup and retrieval.

A dictionary is enclosed in curly braces.

### 💡 Example

```python
person = {
    "name": "John",
    "age": 25,
    "city": "New York"
}

print(person)
```

### 🖥️ Output

```text
{'name': 'John', 'age': 25, 'city': 'New York'}
```

### 🔍 Accessing Dictionary Values

```python
person = {
    "name": "John",
    "age": 25,
    "city": "New York"
}

print("Name:", person["name"])
print("Age:", person["age"])
print("City:", person["city"])
```

### 🖥️ Output

```text
Name: John
Age: 25
City: New York
```

---

# 📊 Quick Data Types Reference

| Data Type | Description | Example |
|---|---|---|
| 🔢 `int` | Whole numbers | `age = 25` |
| 🔢 `float` | Decimal numbers | `pi = 3.14` |
| 🧮 `complex` | Real + imaginary numbers | `z = 3 + 4j` |
| 🔘 `bool` | `True` or `False` | `is_valid = True` |
| 🔤 `str` | Text / characters | `name = "John"` |
| 📋 `list` | Ordered, changeable collection | `numbers = [1, 2, 3]` |
| 📦 `tuple` | Ordered, immutable collection | `coordinates = (3, 4)` |
| 🟢 `set` | Unordered collection of unique elements | `{1, 2, 3}` |
| 🗂️ `dict` | Key-value collection | `{"name": "John"}` |

---

# 🔑 3.3 Keywords in Python

Keywords in Python are special words that have specific meanings and purposes within the Python language.

Keywords play a crucial role in defining the structure and behaviour of Python programs.

Keywords are like **building blocks** that allow us to:

- Create conditional statements
- Create loops
- Define functions
- Define classes
- Handle errors
- Perform other important operations

They help control the flow of the program and specify how different parts of the code should work.

Keywords are **reserved** and cannot be used as variable names or identifiers.

---

## 💡 Example: `if` Keyword

The `if` keyword is used to check a condition and perform specific actions based on that condition.

```python
age = 20

if age >= 18:
    print("You are an adult.")
```

### 🖥️ Output

```text
You are an adult.
```

---

## 💡 Example: `for` Keyword

The `for` keyword is used to create loops that repeat a block of code.

```python
for number in range(1, 4):
    print(number)
```

### 🖥️ Output

```text
1
2
3
```

---

## 💡 Example: `while` Keyword

The `while` keyword is used to create a loop that repeats while a condition is true.

```python
count = 1

while count <= 3:
    print(count)
    count += 1
```

### 🖥️ Output

```text
1
2
3
```

---

## 💡 Example: `def` Keyword

The `def` keyword is used to define functions.

Functions are reusable blocks of code that perform specific tasks.

```python
def greet():
    print("Hello, Python!")

greet()
```

### 🖥️ Output

```text
Hello, Python!
```

---

# 📚 Python Keywords

The source material lists Python keywords including:

```text
False
await
else
None
True
and
as
assert
break
class
continue
def
del
except
finally
elif
for
from
global
import
in
is
lambda
nonlocal
not
or
pass
raise
return
try
while
with
yield
```

> 💡 **Note:** Keywords are reserved words and cannot be used as variable names or identifiers.

---

# 🧠 Quick Revision

| Topic | Key Idea |
|---|---|
| 📦 Variable | Stores a value for later use |
| 🔑 Identifier | Name used to identify a variable, function, class, module, or other user-defined object |
| 🔢 Numeric | Includes `int`, `float`, and `complex` |
| 🔘 Boolean | Represents `True` or `False` |
| 🔤 String | Stores textual data |
| 📋 List | Ordered and changeable collection |
| 📦 Tuple | Ordered and immutable collection |
| 🟢 Set | Unordered collection of unique elements |
| 🗂️ Dictionary | Key-value collection |
| 🔑 Keyword | Reserved word with a predefined meaning |

---

# 🎯 Key Takeaways

- ✅ Variables are used to **store values**.
- ✅ Python automatically determines the type of a variable from its assigned value.
- ✅ Variables can be updated by assigning a new value.
- ✅ Identifiers are names used to identify program elements.
- ✅ Python identifiers are **case-sensitive**.
- ✅ Identifiers cannot start with a digit.
- ✅ Identifiers cannot contain spaces or special characters such as `#` or `$`.
- ✅ Reserved keywords cannot be used as identifiers.
- ✅ Python provides several built-in data types.
- ✅ Numeric types include `int`, `float`, and `complex`.
- ✅ Boolean values are `True` and `False`.
- ✅ Sequence types include strings, lists, and tuples.
- ✅ Sets contain unique elements.
- ✅ Dictionaries store key-value pairs.
- ✅ Keywords control the structure and behaviour of Python programs.

---

# 🚀 Mini Practice Program

Try combining variables, data types, identifiers, and keywords in one program:

```python
# Variables
name = "John"
age = 25
marks = [80, 85, 90]

# Boolean condition
passed = age >= 18

# Keyword: if
if passed:
    print("Name:", name)
    print("Age:", age)
    print("Marks:", marks)
    print("Status: Eligible")
```

### Expected Output

```text
Name: John
Age: 25
Marks: [80, 85, 90]
Status: Eligible
```

---

## 📖 Chapter Summary

```text
Chapter 3: Variables, Data Types & Keywords
│
├── Variables
│   ├── Store values
│   ├── Assignment
│   ├── Updating values
│   └── Operations
│
├── Identifiers
│   ├── Valid characters
│   ├── Case sensitivity
│   ├── Reserved words
│   ├── Length
│   └── Readability
│
├── Data Types
│   ├── Numeric
│   │   ├── int
│   │   ├── float
│   │   └── complex
│   ├── Boolean
│   ├── Sequence
│   │   ├── str
│   │   ├── list
│   │   └── tuple
│   ├── set
│   └── dictionary
│
└── Keywords
    ├── Conditional statements
    ├── Loops
    ├── Functions
    ├── Classes
    └── Other language operations
```

> ⭐ **Remember:** Variables store data, identifiers give names to program elements, data types describe the kind of data, and keywords provide predefined meanings that control Python programs.
