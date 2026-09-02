# 🐍 Operators in Python

> ** Operators in Python**  
> A stylish and beginner-friendly GitHub Markdown version of the provided study material, with an example for each concept.

---

## 📌 4.1 Operators in Python

Operators in Python are symbols or special characters that are used to perform specific operations on variables and values.

Python provides various types of operators to manipulate, and work with different data types.

### 🔹 Important Categories of Operators in Python

| No. | Category |
|---:|---|
| 1 | ➕ Arithmetic Operators |
| 2 | ⚖️ Comparison Operators |
| 3 | 📝 Assignment Operators |
| 4 | 🧠 Logical Operators |
| 5 | 🔢 Bitwise Operators |
| 6 | 🔎 Membership Operators |
| 7 | 🆔 Identity Operators |

---

# ➕ Arithmetic Operators

Arithmetic operators in Python are used to perform mathematical calculations.

## The basic arithmetic operators include:

| Operator | Operation | Description | Example |
|:---:|---|---|---|
| `+` | Addition | Adds two operands together. | `20 + 10 = 30` |
| `-` | Subtraction | Subtracts the second operand from the first. | `20 - 10 = 10` |
| `/` | Division | Divides the first operand by the second and returns the quotient. | `20 / 10 = 2.0` |
| `*` | Multiplication | Multiplies one operand by the other. | `20 * 4 = 80` |
| `%` | Modulus | Returns the remainder after division. | `20 % 3 = 2` |
| `//` | Floor Division | Provides the floor value of the quotient obtained by dividing two operands. | `20 // 3 = 6` |
| `**` | Exponentiation | Raises the first operand to the power of the second operand. | `2 ** 3 = 8` |

---

## 1️⃣ Addition (`+`)

Adds two operands together.

### Example

```python
a = 10
b = 20

print(a + b)
```

### Output

```text
30
```

---

## 2️⃣ Subtraction (`-`)

Subtracts the second operand from the first operand.

### Example

```python
a = 20
b = 10

print(a - b)
```

### Output

```text
10
```

---

## 3️⃣ Division (`/`)

Divides the first operand by the second and returns the quotient.

### Example

```python
a = 20
b = 10

print(a / b)
```

### Output

```text
2.0
```

> 💡 The `/` operator normally returns a floating-point result.

---

## 4️⃣ Multiplication (`*`)

Multiplies one operand by the other.

### Example

```python
a = 20
b = 4

print(a * b)
```

### Output

```text
80
```

---

## 5️⃣ Modulus (`%`)

Returns the remainder after dividing the first operand by the second.

### Example

```python
a = 20
b = 3

print(a % b)
```

### Output

```text
2
```

---

## 6️⃣ Floor Division (`//`)

Provides the floor value of the quotient obtained by dividing two operands. It returns the largest integer that is less than or equal to the result.

### Example

```python
a = 20
b = 3

print(a // b)
```

### Output

```text
6
```

---

## 7️⃣ Exponentiation (`**`)

Raises the first operand to the power of the second operand.

### Example

```python
a = 2
b = 3

print(a ** b)
```

### Output

```text
8
```

---

# ⚖️ Comparison Operators

Comparison operators in Python are used to compare two values and return a Boolean value (`True` or `False`) based on the comparison.

### Common comparison operators include:

| Operator | Meaning | Example |
|:---:|---|---|
| `==` | Equal to | `10 == 10` → `True` |
| `!=` | Not equal to | `10 != 5` → `True` |
| `<` | Less than | `5 < 10` → `True` |
| `>` | Greater than | `10 > 5` → `True` |
| `<=` | Less than or equal to | `10 <= 10` → `True` |
| `>=` | Greater than or equal to | `10 >= 5` → `True` |

---

## 1️⃣ Equal to (`==`)

Checks if two operands are equal.

### Example

```python
a = 10
b = 10

print(a == b)
```

### Output

```text
True
```

---

## 2️⃣ Not Equal to (`!=`)

Checks if two operands are not equal.

### Example

```python
a = 10
b = 5

print(a != b)
```

### Output

```text
True
```

---

## 3️⃣ Less Than (`<`)

Checks if the left operand is less than the right operand.

### Example

```python
a = 5
b = 10

print(a < b)
```

### Output

```text
True
```

---

## 4️⃣ Greater Than (`>`)

Checks if the left operand is greater than the right operand.

### Example

```python
a = 10
b = 5

print(a > b)
```

### Output

```text
True
```

---

## 5️⃣ Less Than or Equal to (`<=`)

Checks if the left operand is less than or equal to the right operand.

### Example

```python
a = 10
b = 10

print(a <= b)
```

### Output

```text
True
```

---

## 6️⃣ Greater Than or Equal to (`>=`)

Checks if the left operand is greater than or equal to the right operand.

### Example

```python
a = 10
b = 5

print(a >= b)
```

### Output

```text
True
```

---

# 📝 Assignment Operators

Assignment operators are used to assign values to variables.

They include:

## 1️⃣ Equal to (`=`)

Assigns the value on the right to the variable on the left.

### Example

```python
x = 10

print(x)
```

### Output

```text
10
```

---

## 2️⃣ Compound Assignment Operators

Compound assignment operators perform the specified arithmetic operation and assign the result to the variable.

Common compound assignment operators include:

| Operator | Meaning | Example |
|:---:|---|---|
| `+=` | Add and assign | `x += 5` |
| `-=` | Subtract and assign | `x -= 5` |
| `*=` | Multiply and assign | `x *= 5` |
| `/=` | Divide and assign | `x /= 5` |

### Example

```python
x = 10

x += 5
print(x)

x -= 3
print(x)

x *= 2
print(x)

x /= 4
print(x)
```

### Output

```text
15
12
24
6.0
```

---

# 🧠 Logical Operators

Logical operators in Python are used to perform logical operations on Boolean values.

The main logical operators are:

| Operator | Description |
|:---:|---|
| `and` | Returns `True` if both operands are `True`, otherwise `False`. |
| `or` | Returns `True` if at least one of the operands is `True`, otherwise `False`. |
| `not` | Returns the opposite Boolean value of the operand. |

---

## 1️⃣ Logical AND (`and`)

Returns `True` if both operands are `True`; otherwise, `False`.

### Example

```python
age = 20

print(age >= 18 and age <= 60)
```

### Output

```text
True
```

---

## 2️⃣ Logical OR (`or`)

Returns `True` if at least one operand is `True`; otherwise, `False`.

### Example

```python
age = 16

print(age < 18 or age > 60)
```

### Output

```text
True
```

---

## 3️⃣ Logical NOT (`not`)

Returns the opposite Boolean value of the operand.

### Example

```python
is_student = True

print(not is_student)
```

### Output

```text
False
```

---

# 🔢 Bitwise Operators

Bitwise operators perform operations on individual bits of binary numbers.

Common bitwise operators in Python are:

| Operator | Operation | Description |
|:---:|---|---|
| `&` | Bitwise AND | Performs a bitwise AND operation. |
| `\|` | Bitwise OR | Performs a bitwise OR operation. |
| `^` | Bitwise XOR | Performs a bitwise exclusive OR operation. |
| `~` | Bitwise Complement | Inverts the bits of the operand. |
| `<<` | Left Shift | Shifts the bits of the left operand to the left by the specified number of positions. |
| `>>` | Right Shift | Shifts the bits of the left operand to the right by the specified number of positions. |

---

## 1️⃣ Bitwise AND (`&`)

Performs a bitwise AND operation on the binary representations of the operands.

### Example

```python
a = 5
b = 3

print(a & b)
```

### Output

```text
1
```

Binary representation:

```text
5 = 101
3 = 011
    ---
    001 = 1
```

---

## 2️⃣ Bitwise OR (`|`)

Performs a bitwise OR operation on the binary representations of the operands.

### Example

```python
a = 5
b = 3

print(a | b)
```

### Output

```text
7
```

---

## 3️⃣ Bitwise XOR (`^`)

Performs a bitwise exclusive OR operation on the binary representations of the operands.

### Example

```python
a = 5
b = 3

print(a ^ b)
```

### Output

```text
6
```

---

## 4️⃣ Bitwise Complement (`~`)

Inverts the bits of the operand.

### Example

```python
a = 5

print(~a)
```

### Output

```text
-6
```

---

## 5️⃣ Left Shift (`<<`)

Shifts the bits of the left operand to the left by the number of positions specified by the right operand.

### Example

```python
a = 5

print(a << 1)
```

### Output

```text
10
```

---

## 6️⃣ Right Shift (`>>`)

Shifts the bits of the left operand to the right by the number of positions specified by the right operand.

### Example

```python
a = 8

print(a >> 1)
```

### Output

```text
4
```

---

# 🔎 Membership Operators

Membership operators are used to test whether a value exists in a sequence.

The common membership operators are:

| Operator | Description |
|:---:|---|
| `in` | Returns `True` if the value is found in the sequence. |
| `not in` | Returns `True` if the value is not found in the sequence. |

### Example: `in`

```python
numbers = [10, 20, 30, 40]

print(20 in numbers)
```

### Output

```text
True
```

### Example: `not in`

```python
numbers = [10, 20, 30, 40]

print(50 not in numbers)
```

### Output

```text
True
```

---

# 🆔 Identity Operators

Identity operators are used to compare the identity of two objects.

They include:

| Operator | Description |
|:---:|---|
| `is` | Returns `True` if both operands refer to the same object. |
| `is not` | Returns `True` if both operands do not refer to the same object. |

### Example: `is`

```python
a = [1, 2, 3]
b = a

print(a is b)
```

### Output

```text
True
```

Here, `a` and `b` refer to the same list object.

### Example: `is not`

```python
a = [1, 2, 3]
b = [1, 2, 3]

print(a is not b)
```

### Output

```text
True
```

> 💡 `is` checks **object identity**, whereas `==` checks **value equality**.

---

# 📚 Quick Revision Table

| Category | Operators |
|---|---|
| ➕ Arithmetic | `+`, `-`, `*`, `/`, `%`, `//`, `**` |
| ⚖️ Comparison | `==`, `!=`, `<`, `>`, `<=`, `>=` |
| 📝 Assignment | `=`, `+=`, `-=`, `*=`, `/=` |
| 🧠 Logical | `and`, `or`, `not` |
| 🔢 Bitwise | `&`, `\|`, `^`, `~`, `<<`, `>>` |
| 🔎 Membership | `in`, `not in` |
| 🆔 Identity | `is`, `is not` |

---

# 🧪 Mini Practice Program

Write a Python program that demonstrates different operators:

```python
a = 20
b = 5

print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Modulus:", a % b)
print("Floor Division:", a // b)
print("Exponentiation:", a ** b)

print("a == b:", a == b)
print("a > b:", a > b)

print("Logical:", a > 10 and b < 10)
```

### Expected Output

```text
Addition: 25
Subtraction: 15
Multiplication: 100
Division: 4.0
Modulus: 0
Floor Division: 4
Exponentiation: 3200000
a == b: False
a > b: True
Logical: True
```

---

# 🎯 Key Takeaways

- Operators are symbols or keywords used to perform operations on values and variables.
- **Arithmetic operators** perform mathematical calculations.
- **Comparison operators** compare values and return Boolean results.
- **Assignment operators** assign or update values in variables.
- **Logical operators** combine or invert Boolean conditions.
- **Bitwise operators** operate on individual bits.
- **Membership operators** check whether a value exists in a sequence.
- **Identity operators** compare whether two operands refer to the same object.

---

## 🚀 Learning Path

```text
Python Variables
      ↓
Data Types
      ↓
Operators
      ↓
Conditional Statements
      ↓
Loops
      ↓
Functions
      ↓
Lists / Tuples / Sets / Dictionaries
      ↓
Object-Oriented Programming
```

---

> **📖 Source note:** The organization and core explanations above follow the provided chapter material. Examples and formatting have been added to make the content easier for undergraduate students to learn and practice.
