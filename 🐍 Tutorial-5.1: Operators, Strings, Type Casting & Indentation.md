 Operators, Strings, Type Casting & Indentation

A comprehensive tutorial covering operator precedence, string operations, type casting, and indentation in Python — with detailed examples.

---

## Table of Contents

- [1. Operator Precedence and Associativity](#1-operator-precedence-and-associativity)
  - [Precedence Hierarchy](#precedence-hierarchy)
  - [Associativity](#associativity)
- [2. Operations on Strings](#2-operations-on-strings)
  - [String Creation](#string-creation)
  - [Concatenation & Repetition](#concatenation--repetition)
  - [Indexing & Slicing](#indexing--slicing)
  - [String Methods](#string-methods)
  - [String Formatting](#string-formatting)
  - [Immutability](#immutability)
- [3. Type Casting (Type Conversion)](#3-type-casting-type-conversion)
  - [Implicit Conversion](#implicit-conversion)
  - [Explicit Conversion](#explicit-conversion)
  - [Practical Scenarios](#practical-scenarios)
- [4. Indentation in Python](#4-indentation-in-python)
  - [Rules](#rules)
  - [Examples](#examples)
  - [Common Errors](#common-errors)
  - [Best Practices](#best-practices)

---

## 1. Operator Precedence and Associativity

### What is Operator Precedence?

Operator precedence determines the order in which operations are performed in an expression. Python follows a specific hierarchy — some operators are evaluated before others, just like in mathematics (PEMDAS/BODMAS).

### Precedence Hierarchy (Highest to Lowest)

| Precedence | Operator(s) | Description |
|------------|-------------|-------------|
| 1 | `()` | Parentheses |
| 2 | `**` | Exponentiation |
| 3 | `+x`, `-x`, `~x` | Unary plus, minus, bitwise NOT |
| 4 | `*`, `/`, `//`, `%` | Multiplication, division, floor division, modulo |
| 5 | `+`, `-` | Addition, subtraction |
| 6 | `<<`, `>>` | Bitwise shift |
| 7 | `&` | Bitwise AND |
| 8 | `^` | Bitwise XOR |
| 9 | `\|` | Bitwise OR |
| 10 | `==`, `!=`, `>`, `<`, `>=`, `<=`, `is`, `is not`, `in`, `not in` | Comparisons, identity, membership |
| 11 | `not` | Logical NOT |
| 12 | `and` | Logical AND |
| 13 | `or` | Logical OR |

### Detailed Examples

#### Example 1: Basic Arithmetic Precedence
```python
result = 10 + 3 * 2
print(result)  # Output: 16
# Multiplication (*) has higher precedence than addition (+)
# So: 3 * 2 = 6, then 10 + 6 = 16

result = (10 + 3) * 2
print(result)  # Output: 26
# Parentheses override precedence
```

#### Example 2: Exponentiation vs. Unary Minus
```python
result = -3 ** 2
print(result)  # Output: -9
# ** has higher precedence than unary minus
# So: 3**2 = 9, then -(9) = -9

result = (-3) ** 2
print(result)  # Output: 9
# Parentheses force -3 to be evaluated first
```

#### Example 3: Mixed Operators
```python
result = 100 / 10 * 5
print(result)  # Output: 50.0
# / and * have same precedence, so left-to-right associativity applies
# 100 / 10 = 10.0, then 10.0 * 5 = 50.0

result = 100 - 50 + 25
print(result)  # Output: 75
# + and - have same precedence, left-to-right
# 100 - 50 = 50, then 50 + 25 = 75
```

#### Example 4: Logical Operators
```python
result = True or False and False
print(result)  # Output: True
# 'and' has higher precedence than 'or'
# False and False = False, then True or False = True

result = (True or False) and False
print(result)  # Output: False
# Parentheses change the evaluation order
```

#### Example 5: Comparison Chaining
```python
x = 5
result = 1 < x < 10
print(result)  # Output: True
# Chained comparisons: equivalent to (1 < x) and (x < 10)

result = 1 < x > 3
print(result)  # Output: True
# Equivalent to (1 < x) and (x > 3)
```

### Associativity

Associativity determines the order when multiple operators of the **same precedence** appear in an expression.

| Associativity | Operators |
|---------------|-----------|
| **Left-to-Right** | `+`, `-`, `*`, `/`, `//`, `%`, `<<`, `>>`, `&`, `^`, `\|` |
| **Right-to-Left** | `**`, `=` (assignment), `:=` (walrus) |

#### Left-to-Right Associativity
```python
result = 100 / 10 / 2
print(result)  # Output: 5.0
# Evaluated as: (100 / 10) / 2 = 10.0 / 2 = 5.0

result = 10 - 5 - 2
print(result)  # Output: 3
# Evaluated as: (10 - 5) - 2 = 5 - 2 = 3
```

#### Right-to-Left Associativity (Exponentiation)
```python
result = 2 ** 3 ** 2
print(result)  # Output: 512
# Evaluated as: 2 ** (3 ** 2) = 2 ** 9 = 512
# NOT (2 ** 3) ** 2 = 8 ** 2 = 64

# Multiple assignments
a = b = c = 10
print(a, b, c)  # Output: 10 10 10
# Evaluated right-to-left: c = 10, then b = c, then a = b
```

---

## 2. Operations on Strings

Strings in Python are **immutable** sequences of characters. Once created, they cannot be changed in place.

### String Creation
```python
single = 'Hello'
double = "World"
multi_line = """This is a
multi-line string"""
raw = r"C:\\Users\\name"  # Raw string (backslashes are literal)
```

### Concatenation & Repetition
```python
# Using + operator
first = "Hello"
last = "World"
full = first + " " + last
print(full)  # Output: Hello World

# Using += (creates new string each time)
greeting = "Hi"
greeting += " there"
print(greeting)  # Output: Hi there

# Using join() (more efficient for multiple strings)
words = ["Python", "is", "awesome"]
sentence = " ".join(words)
print(sentence)  # Output: Python is awesome

# Using f-strings (Python 3.6+)
name = "Alice"
age = 25
info = f"My name is {name} and I am {age} years old"
print(info)  # Output: My name is Alice and I am 25 years old

# Repetition
line = "-" * 30
print(line)  # Output: ------------------------------

pattern = "Na" * 4 + " Batman!"
print(pattern)  # Output: NaNaNaNa Batman!
```

### Indexing & Slicing
```python
text = "Python"

# Indexing (0-based)
print(text[0])   # Output: P
print(text[-1])  # Output: n (last character)
print(text[-2])  # Output: o (second from last)

# Slicing [start:stop:step]
print(text[0:3])    # Output: Pyt (indices 0, 1, 2)
print(text[:3])     # Output: Pyt (from start to index 2)
print(text[3:])     # Output: hon (from index 3 to end)
print(text[:])      # Output: Python (full copy)
print(text[::2])    # Output: Pto (every 2nd character)
print(text[::-1])   # Output: nohtyP (reversed string)

# Slicing never raises IndexError
print(text[100:200])  # Output: (empty string, no error)
```

### String Methods
```python
text = "  Hello, Python World!  "

# Case operations
print(text.upper())       # Output:   HELLO, PYTHON WORLD!  
print(text.lower())       # Output:   hello, python world!  
print(text.title())       # Output:   Hello, Python World!  
print(text.capitalize())  # Output:   hello, python world!  
print(text.swapcase())    # Output:   hELLO, pYTHON wORLD!  

# Stripping whitespace
print(text.strip())       # Output: Hello, Python World!
print(text.lstrip())      # Output: Hello, Python World!  
print(text.rstrip())      # Output:   Hello, Python World!

# Finding and replacing
print(text.find("Python"))     # Output: 10 (index of first occurrence)
print(text.find("Java"))       # Output: -1 (not found)
print(text.index("Python"))    # Output: 10 (raises ValueError if not found)
print(text.count("o"))         # Output: 3
print(text.replace("Python", "Java"))  # Output:   Hello, Java World!  

# Checking content
print("123".isdigit())       # Output: True
print("abc".isalpha())       # Output: True
print("abc123".isalnum())    # Output: True
print("   ".isspace())       # Output: True
print("Hello".startswith("He"))  # Output: True
print("World!".endswith("!"))    # Output: True

# Splitting and joining
csv = "apple,banana,orange"
fruits = csv.split(",")
print(fruits)  # Output: ['apple', 'banana', 'orange']

lines = "line1\nline2\nline3"
print(lines.splitlines())  # Output: ['line1', 'line2', 'line3']

# Partition (splits into 3 parts: before, separator, after)
result = "key=value".partition("=")
print(result)  # Output: ('key', '=', 'value')
```

### String Formatting
```python
# Old style (% formatting)
name = "Alice"
age = 25
print("My name is %s and I am %d years old" % (name, age))

# .format() method
print("My name is {} and I am {} years old".format(name, age))
print("My name is {0} and I am {1} years old".format(name, age))
print("My name is {n} and I am {a} years old".format(n=name, a=age))

# f-strings (recommended)
print(f"My name is {name} and I am {age} years old")
print(f"Pi = {3.14159:.2f}")  # Output: Pi = 3.14
print(f"Binary of 10 = {10:b}")  # Output: Binary of 10 = 1010
print(f"Right aligned: {name:>10}")  # Output: Right aligned:      Alice
print(f"Centered: {name:^10}")       # Output: Centered:   Alice   
```

### Immutability
```python
s = "hello"
# s[0] = "H"  # TypeError: 'str' object does not support item assignment

# To "modify" a string, create a new one
s = "H" + s[1:]
print(s)  # Output: Hello

# Or convert to list, modify, then join back
chars = list(s)
chars[0] = "J"
s = "".join(chars)
print(s)  # Output: Jello
```

---

## 3. Type Casting (Type Conversion)

Type casting is the process of converting a value from one data type to another. Python provides **implicit** (automatic) and **explicit** (manual) type conversion.

### Implicit Conversion
```python
# int + float = float
result = 5 + 3.5
print(result)       # Output: 8.5
print(type(result)) # Output: <class 'float'>

# int + complex = complex
result = 5 + 3j
print(result)       # Output: (5+3j)
print(type(result)) # Output: <class 'complex'>

# bool in arithmetic (True=1, False=0)
result = 10 + True
print(result)  # Output: 11
```

### Explicit Conversion

| Function | Converts To | Example |
|----------|-------------|---------|
| `int()` | Integer | `int("42")` → `42` |
| `float()` | Float | `float("3.14")` → `3.14` |
| `str()` | String | `str(100)` → `"100"` |
| `bool()` | Boolean | `bool(1)` → `True` |
| `list()` | List | `list("abc")` → `['a', 'b', 'c']` |
| `tuple()` | Tuple | `tuple([1, 2, 3])` → `(1, 2, 3)` |
| `set()` | Set | `set([1, 2, 2])` → `{1, 2}` |
| `dict()` | Dictionary | `dict([('a', 1)])` → `{'a': 1}` |

#### int() Conversions
```python
# From string
print(int("42"))        # Output: 42
print(int("  42  "))    # Output: 42 (whitespace is stripped)
print(int("42", 10))    # Output: 42 (base 10, default)
print(int("1010", 2))   # Output: 10 (binary to decimal)
print(int("FF", 16))    # Output: 255 (hex to decimal)
print(int("77", 8))     # Output: 63 (octal to decimal)

# From float (truncates decimal part)
print(int(3.99))        # Output: 3 (not rounded!)
print(int(-3.99))       # Output: -3

# From bool
print(int(True))        # Output: 1
print(int(False))       # Output: 0

# Invalid conversions (will raise ValueError):
# int("42.5")
# int("hello")
```

#### float() Conversions
```python
print(float("3.14"))    # Output: 3.14
print(float("42"))      # Output: 42.0
print(float("  2.5  ")) # Output: 2.5
print(float("inf"))     # Output: inf
print(float("-inf"))    # Output: -inf
print(float("nan"))     # Output: nan

print(float(42))        # Output: 42.0
print(float(True))      # Output: 1.0
```

#### str() Conversions
```python
print(str(42))          # Output: "42"
print(str(3.14159))     # Output: "3.14159"
print(str(True))        # Output: "True"
print(str([1, 2, 3]))   # Output: "[1, 2, 3]"
print(str(None))        # Output: "None"

# Custom object conversion
class Person:
    def __str__(self):
        return "I am a Person"

p = Person()
print(str(p))  # Output: I am a Person
```

#### bool() Conversions
```python
# Falsy values (convert to False)
print(bool(0))          # Output: False
print(bool(0.0))        # Output: False
print(bool(""))         # Output: False
print(bool([]))         # Output: False
print(bool({}))         # Output: False
print(bool(None))       # Output: False
print(bool(set()))      # Output: False

# Truthy values (convert to True)
print(bool(1))          # Output: True
print(bool(-5))         # Output: True (any non-zero number)
print(bool("hello"))    # Output: True
print(bool([0]))        # Output: True (non-empty list)
print(bool("False"))    # Output: True (non-empty string!)
```

#### list(), tuple(), set() Conversions
```python
# String to list
print(list("hello"))    # Output: ['h', 'e', 'l', 'l', 'o']

# Tuple to list
print(list((1, 2, 3)))  # Output: [1, 2, 3]

# List to tuple
print(tuple([1, 2, 3])) # Output: (1, 2, 3)

# List to set (removes duplicates)
print(set([1, 2, 2, 3, 3, 3]))  # Output: {1, 2, 3}

# Dictionary to list (keys only)
print(list({"a": 1, "b": 2}))   # Output: ['a', 'b']
```

### Practical Scenarios
```python
# Reading user input (always returns string)
age_str = input("Enter your age: ")  # User enters: 25
age = int(age_str)
print(f"In 5 years, you will be {age + 5}")

# Safe conversion with error handling
def safe_int(value):
    try:
        return int(value)
    except ValueError:
        return None

print(safe_int("42"))     # Output: 42
print(safe_int("abc"))    # Output: None

# Converting a list of strings to integers
str_numbers = ["1", "2", "3", "4", "5"]
int_numbers = [int(x) for x in str_numbers]
print(int_numbers)  # Output: [1, 2, 3, 4, 5]

# Parsing data from a file
data = "10,20,30,40"
numbers = [int(x) for x in data.split(",")]
print(sum(numbers))  # Output: 100
```

---

## 4. Indentation in Python

Unlike many programming languages that use braces `{}` or keywords to define code blocks, Python uses **indentation** (whitespace at the beginning of a line) to determine the grouping of statements.

### Rules

| Rule | Description |
|------|-------------|
| **Consistency** | Use either spaces or tabs, never mix them in the same file |
| **PEP 8 Standard** | Use **4 spaces** per indentation level |
| **Mandatory** | Indentation is not optional — it defines code structure |
| **Same Level** | Statements at the same indentation level belong to the same block |

### Examples

#### if-else Statement
```python
age = 18

if age >= 18:
    print("You are an adult")      # Indented 4 spaces
    print("You can vote")          # Same block
else:
    print("You are a minor")       # Indented 4 spaces
    print("You cannot vote yet")   # Same block

print("This runs regardless")      # No indentation = outside if-else
```

#### Nested if Statements
```python
score = 85

if score >= 60:
    print("You passed")            # Level 1: 4 spaces
    if score >= 90:
        print("Excellent! A grade")  # Level 2: 8 spaces
    elif score >= 80:
        print("Good job! B grade")   # Level 2: 8 spaces
    else:
        print("Keep improving")      # Level 2: 8 spaces
else:
    print("You failed")            # Level 1: 4 spaces
    print("Please retake the exam") # Level 1: 4 spaces
```

#### for Loop
```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(f"I like {fruit}")       # Loop body: 4 spaces
    print(f"  {fruit} is tasty")   # Still in loop: 8 spaces

print("Done with fruits")          # Outside loop: 0 spaces
```

#### while Loop
```python
count = 0

while count < 5:
    print(f"Count: {count}")       # Loop body
    count += 1                     # Still in loop
else:
    print("Loop completed")        # else block (runs if no break)

print("After loop")                # Outside loop
```

#### Function Definition
```python
def greet(name):
    """This function greets a person."""  # Docstring
    message = f"Hello, {name}!"           # Function body: 4 spaces
    print(message)                        # Still in function
    return message                        # Still in function

# Calling the function (no indentation)
result = greet("Alice")
```

#### Class Definition
```python
class Dog:
    species = "Canis familiaris"      # Class variable: 4 spaces

    def __init__(self, name):         # Method: 4 spaces
        self.name = name              # Method body: 8 spaces

    def bark(self):                   # Method: 4 spaces
        print(f"{self.name} says woof!")  # Method body: 8 spaces

# Creating an object (no indentation)
my_dog = Dog("Buddy")
my_dog.bark()  # Output: Buddy says woof!
```

### Common Errors

```python
# ❌ IndentationError: unexpected indent
    print("Hello")  # Indented without a reason

# ❌ IndentationError: expected an indented block
if True:
# Error: expected indented block after if statement
print("Hello")

# ❌ TabError: inconsistent use of tabs and spaces
if True:
    print("Line 1")  # 4 spaces
    print("Line 2")  # Tab character

# ❌ Unindent does not match any outer indentation level
if True:
    if True:
        print("Inner")
      print("This doesn't match any level")  # Error
```

### Best Practices

```python
# ✅ Good: Consistent 4 spaces
def calculate_area(radius):
    pi = 3.14159
    area = pi * radius ** 2
    return area

# ✅ Good: Clear visual structure
def process_data(data):
    result = []
    for item in data:
        if item > 0:
            processed = item * 2
            result.append(processed)
        else:
            result.append(0)
    return result

# ✅ Good: Multi-line statements
result = some_function(
    arg1, arg2, arg3,
    arg4, arg5
)

# ❌ Bad: Inconsistent spacing
def bad_function():
   x = 1      # 3 spaces
     y = 2    # 5 spaces
  z = 3       # 2 spaces
```

---

## Summary

| Topic | Key Takeaway |
|-------|-------------|
| **Precedence** | `()` > `**` > `* / // %` > `+ -` > comparisons > `not` > `and` > `or` |
| **Associativity** | Most operators are left-to-right; `**` and `=` are right-to-left |
| **Strings** | Immutable; rich set of methods; use f-strings for formatting |
| **Type Casting** | `int()`, `float()`, `str()`, `bool()`; handle errors with try-except |
| **Indentation** | 4 spaces per level; defines code blocks; consistency is mandatory |

---

## Contributing

Feel free to submit issues or pull requests if you find any errors or want to add more examples!

## License

This guide is released under the MIT License.
