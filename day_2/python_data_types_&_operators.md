# Python Basics: Lists, Tuples, Dictionaries, Sets, Booleans, and Operators

This notebook covers the foundational Python data structures and operators. Here's a detailed explanation of each concept, with examples and explanations for every topic covered.

---

## 1. **List**

**Definition:**  
A `list` in Python is a sequential, mutable, inbuilt data structure used to store multiple values in a single variable.

**Key Points:**
- Lists are ordered (sequence matters).
- They can store elements of different data types (e.g., int, float, string).
- Lists are mutable (you can change their content).

**Example:**
```python
cities = ["Mumbai", "Delhi", "Bengaluru", "Hyderabad", "Chennai"]
print(cities)
# Output: ['Mumbai', 'Delhi', 'Bengaluru', 'Hyderabad', 'Chennai']
```

**Accessing Elements:**
Use indices (starting from 0) to access elements.
```python
print(cities[0]) # Mumbai
print(cities[1]) # Delhi
print(cities[2]) # Bengaluru
```

---

### **List Operations**

#### - Modifying Elements
```python
cities[2] = "Mysore"
print(cities)
# Output: ['Mumbai', 'Delhi', 'Mysore', 'Hyderabad', 'Chennai']
```
Lists are mutable, so you can change their content.

#### - Checking the Type
```python
print(type(cities))
# Output: <class 'list'>
```

---

### **Common List Functions**

#### - `append()`: Add an element at the end
```python
cities.append('Indore')
print(cities)
# Output: ['Mumbai', 'Delhi', 'Mysore', 'Hyderabad', 'Chennai', 'Indore']
```

#### - `insert(index, value)`: Insert at a specific index
```python
cities.insert(2, 'Jaipur')
print(cities)
# Output: ['Mumbai', 'Delhi', 'Jaipur', 'Mysore', 'Hyderabad', 'Chennai', 'Indore']
```

#### - `remove(value)`: Remove the first occurrence of a value
```python
cities.remove('Mysore')
print(cities)
# Output: ['Mumbai', 'Delhi', 'Jaipur', 'Hyderabad', 'Chennai', 'Indore']
```

#### - `pop(index)`: Remove and return item at index (default is last)
```python
cities.pop(2)
print(cities)
# Output: ['Mumbai', 'Delhi', 'Hyderabad', 'Chennai', 'Indore']
```

#### - `index(value)`: Get the index of a value
```python
print(cities.index('Chennai'))
# Output: 3
```

#### - `len(list)`: Get the number of items
```python
print(len(cities))
# Output: 5
```

---

## 2. **Tuple**

**Definition:**  
A `tuple` is a sequential, inbuilt Python data structure used to store multiple values in a single variable. Unlike lists, tuples are immutable.

**Key Points:**
- Tuples are ordered.
- Immutable (cannot change elements after creation).

**Example:**
```python
colors = ("blue", "green", "pink", "red", "yellow")
print(colors)
# Output: ('blue', 'green', 'pink', 'red', 'yellow')
print(type(colors))
# Output: <class 'tuple'>
```

**Immutability Example:**
```python
colors[1] = 'purple'
# TypeError: 'tuple' object does not support item assignment
```

**Finding Index:**
```python
print(colors.index("pink"))
# Output: 2
```

---

## 3. **Dictionary**

**Definition:**  
A `dict` (dictionary) is a mutable, sequential collection of key-value pairs.

**Key Points:**
- Keys must be unique and immutable (e.g., strings, numbers).
- Values can be of any type.

**Example:**
```python
emp_details = {'name': 'Jai', 'city': 'Delhi', 'age': 22}
print(emp_details)
# Output: {'name': 'Jai', 'city': 'Delhi', 'age': 22}
print(type(emp_details))
# Output: <class 'dict'>
```

**Accessing Values:**
```python
print(emp_details['name']) # Jai
print(emp_details['city']) # Delhi
print(emp_details['age'])  # 22
```

**Dictionary Methods:**
- `keys()`: returns all keys
- `values()`: returns all values

```python
print(emp_details.keys())   # dict_keys(['name', 'city', 'age'])
print(emp_details.values()) # dict_values(['Jai', 'Delhi', 22])
```

**Modifying Dictionary:**
- Change a value:
    ```python
    emp_details['name'] = 'pavan'
    print(emp_details)
    # Output: {'name': 'pavan', 'city': 'Delhi', 'age': 22}
    ```

- Add a new key-value pair:
    ```python
    emp_details['salary'] = 34000.50
    print(emp_details)
    # Output: {'name': 'pavan', 'city': 'Delhi', 'age': 22, 'salary': 34000.5}
    ```

- Remove a key:
    ```python
    del(emp_details['age'])
    print(emp_details)
    # Output: {'name': 'pavan', 'city': 'Delhi', 'salary': 34000.5}
    ```

---

## 4. **Set**

**Definition:**  
A `set` is a non-sequential, mutable Python data structure that stores unique values.

**Key Points:**
- Unordered collection (no indexing).
- No duplicate values.

**Example:**
```python
ids = {10, 12, 15, 17, 19, 20, 10, 15, 17}
print(ids)
# Output: {10, 12, 15, 17, 19, 20}
print(type(ids))
# Output: <class 'set'>
```

---

## 5. **Boolean**

**Definition:**  
A `bool` is a data type with only two possible values: `True` or `False`.

**Example:**
```python
status = True
print(status)
# Output: True
print(type(status))
# Output: <class 'bool'>
```

---

## 6. **Operators & Operands**

Python supports various operators for performing operations on variables and values.

### - **Arithmetic Operators**
Perform mathematical operations.

| Operator | Description         | Example                | Output  |
|----------|---------------------|------------------------|---------|
| `+`      | Addition           | `17 + 5`               | `22`    |
| `-`      | Subtraction        | `17 - 5`               | `12`    |
| `*`      | Multiplication     | `17 * 5`               | `85`    |
| `/`      | Division           | `17 / 5`               | `3.4`   |
| `**`     | Exponentiation     | `17 ** 5`              | `1419857` |
| `//`     | Floor Division     | `17 // 5`              | `3`     |
| `%`      | Modulus            | `17 % 5`               | `2`     |

**Example:**
```python
a = 17
b = 5
print(a + b)  # 22
print(a - b)  # 12
print(a * b)  # 85
print(a / b)  # 3.4
print(a ** b) # 1419857
print(a // b) # 3
print(a % b)  # 2
```

---

### - **Assignment Operators**
Assign values to variables.

| Operator | Example   | Equivalent to     |
|----------|-----------|------------------|
| `=`      | `x = 21`  |                  |
| `+=`     | `x += 2`  | `x = x + 2`      |
| `-=`     | `x -= 3`  | `x = x - 3`      |
| `*=`     | `x *= 2`  | `x = x * 2`      |
| `/=`     | `x /= 6`  | `x = x / 6`      |
| `**=`    | `x **= 2` | `x = x ** 2`     |
| `//=`    | `x //= 3` | `x = x // 3`     |
| `%=`     | `x %= 5`  | `x = x % 5`      |

**Example:**
```python
x = 21
x += 2
print(x)  # 23
x -= 3
print(x)  # 20
x *= 2
print(x)  # 40
x /= 6
print(x)  # 6.666...
x **= 2
print(x)  # 44.444...
x //= 3
print(x)  # 14.0
x %= 5
print(x)  # 4.0
```

---

### - **Comparison Operators**
Compare two values and return a boolean result.

| Operator | Description         | Example         | Output   |
|----------|---------------------|-----------------|----------|
| `==`     | Equal to            | `a == 12`       | `True`   |
| `!=`     | Not equal to        | `a != b`        | `True`   |
| `>`      | Greater than        | `a > b`         | `True`   |
| `<`      | Less than           | `a < b`         | `False`  |
| `>=`     | Greater or equal    | `a >= b`        | `True`   |
| `<=`     | Less or equal       | `a <= b`        | `False`  |

**Example:**
```python
a = 12
b = 7
print(a == 12) # True
print(b == 7)  # True
print(a == b)  # False
print(a != b)  # True
print(a > b)   # True
print(a < b)   # False
print(a >= b)  # True
print(a <= b)  # False
```

---

### - **Logical Operators**
Combine conditional statements.

| Operator | Description | Example               | Output   |
|----------|-------------|-----------------------|----------|
| `and`    | Logical AND | `True and False`      | `False`  |
| `or`     | Logical OR  | `True or False`       | `True`   |

**Example:**
```python
print(True and True)   # True
print(True and False)  # False
print(False or True)   # True
print(False or False)  # False
```

**With variables:**
```python
age = 21
weight = 65
print(age > 18 and weight > 50)  # True
print(age < 18 or weight > 50)   # True
```

---

### - **Membership Operators**
Test membership in a sequence (like string, list, tuple).

| Operator | Description             | Example                 | Output   |
|----------|-------------------------|-------------------------|----------|
| `in`     | Value exists            | `'P' in name`           | `True`   |
| `not in` | Value does not exist    | `'Q' not in name`       | `True`   |

**Example:**
```python
name = "Pavan Singh Negi"
print('P' in name)    # True
print('Q' in name)    # False
print('P' not in name) # False
print('Q' not in name) # True
```

---

## **Summary Table**

| Data Structure | Ordered? | Mutable? | Syntax Example             |
|----------------|----------|----------|----------------------------|
| List           | Yes      | Yes      | `[1, 2, 3]`                |
| Tuple          | Yes      | No       | `(1, 2, 3)`                |
| Dictionary     | Yes      | Yes      | `{'a': 1, 'b': 2}`         |
| Set            | No       | Yes      | `{1, 2, 3}`                |
| Boolean        | N/A      | N/A      | `True`, `False`            |

---

This notebook provides a solid foundation for working with Python's basic data structures and operators. Practice each concept to deepen your understanding!
