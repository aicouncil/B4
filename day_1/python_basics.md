### 1\. Variables and Data Types

In Python, variables are used to store data in memory. This section of the notebook explains the fundamental data types and how to work with them.

  * **Variables**: A variable is a name given to a memory location. The assignment operator (`=`) is used to store a value in a variable.
    ```python
    x = 10
    ```
  * **Data Types**: Python is a dynamically typed language, meaning you don't need to declare the variable type explicitly. The type is inferred from the value.
      * **Integer (`int`)**: Represents whole numbers, positive or negative.
        ```python
        age = 25
        ```
      * **Float (`float`)**: Represents real numbers with decimal points.
        ```python
        price = 19.99
        ```
      * **String (`str`)**: Represents a sequence of characters enclosed in single or double quotes.
        ```python
        name = "John Doe"
        ```
      * **Boolean (`bool`)**: Represents truth values, either `True` or `False`.
        ```python
        is_active = True
        ```
  * **Type Conversion (Casting)**: You can convert a variable from one data type to another using built-in functions.
    ```python
    number_str = "123"
    number_int = int(number_str)

    decimal_num = 5
    float_num = float(decimal_num)

    int_val = 100
    str_val = str(int_val)
    ```

-----

### 2\. Operators

Operators are special symbols used to perform operations on variables and values.

  * **Arithmetic Operators**: Used for mathematical calculations.
      * `+` (Addition), `-` (Subtraction), `*` (Multiplication), `/` (Division)
      * `**` (Exponentiation): Raises a number to the power of another.
      * `//` (Floor Division): Divides and returns the integer part of the quotient.
      * `%` (Modulus): Divides and returns the remainder.
  * **Comparison Operators**: Used to compare two values and return a boolean result (`True` or `False`).
      * `==` (Equal to), `!=` (Not equal to)
      * `>` (Greater than), `<` (Less than)
      * `>=` (Greater than or equal to), `<=` (Less than or equal to)
  * **Logical Operators**: Used to combine conditional statements.
      * `and`: Returns `True` if both statements are true.
      * `or`: Returns `True` if at least one statement is true.
      * `not`: Reverses the logical state of its operand.

-----

### 3\. Data Structures

Python offers several built-in data structures to organize and store collections of data.

  * **Lists**:
      * **Definition**: A list is an ordered, mutable (changeable) collection of items. It is created using square brackets `[]`.
      * **Indexing and Slicing**: Elements can be accessed by their index, which starts at `0`. Slicing extracts a sub-list.
        ```python
        my_list = [1, 'apple', 3.14, True]
        print(my_list[1])    # Output: 'apple'
        print(my_list[1:3])  # Output: ['apple', 3.14]
        ```
      * **Methods**: Lists have various methods for manipulation, such as `append()` (adds an element to the end), `insert()` (adds an element at a specific index), `remove()` (removes the first occurrence of a value), and `pop()` (removes and returns an element at a given index).
  * **Tuples**:
      * **Definition**: A tuple is an ordered, **immutable** (unchangeable) collection of items. It is created using parentheses `()`.
      * **Key Feature**: Once a tuple is created, its elements cannot be modified, which makes them useful for data that should not change.
  * **Dictionaries**:
      * **Definition**: A dictionary is an unordered, mutable collection of **key-value pairs**. It is created using curly braces `{}`.
      * **Accessing Values**: Values are accessed using their unique keys, not an index.
        ```python
        my_dict = {'name': 'John', 'age': 30, 'city': 'New York'}
        print(my_dict['name']) # Output: 'John'
        ```
      * **Methods**: Dictionaries have methods like `keys()` (returns all keys), `values()` (returns all values), and `items()` (returns all key-value pairs).
  * **Sets**:
      * **Definition**: A set is an unordered, mutable collection of **unique** elements. It is created using curly braces `{}` or the `set()` constructor.
      * **Key Feature**: Duplicates are automatically removed. This is its primary use case.
      * **Set Operations**: Sets support mathematical operations like `union()` (combines sets), `intersection()` (finds common elements), and `difference()` (finds elements in one set but not the other).

-----

### 4\. Control Flow and Loops

Control flow statements determine the order in which a program's code is executed.

  * **Conditional Statements (`if-elif-else`)**: These statements allow a program to make decisions based on whether a condition is true or false.
    ```python
    x = 10
    if x > 10:
      print("x is greater than 10")
    elif x == 10:
      print("x is equal to 10")
    else:
      print("x is less than 10")
    ```
  * **For Loops**: Used to iterate over a sequence (like a list, tuple, or string).
    ```python
    for item in ['a', 'b', 'c']:
      print(item)
    ```
  * **While Loops**: Repeatedly executes a block of code as long as a condition is true.
    ```python
    count = 0
    while count < 3:
      print(count)
      count += 1
    ```
  * **`break` and `continue`**: These keywords are used to alter the flow of a loop. `break` immediately exits the loop, while `continue` skips the current iteration and moves to the next.

-----

### 5\. Functions

**Definition**: A function is a named, reusable block of code that performs a specific task. It helps in organizing code, improving readability, and reducing redundancy.

  * **Syntax**: Functions are defined using the `def` keyword, followed by the function name, parameters in parentheses, and a colon. The `return` statement is used to send a value back to the caller.
    ```python
    def add_numbers(a, b):
      return a + b
    result = add_numbers(5, 3)
    print(result) # Output: 8
    ```
  * **Lambda Functions**:
      * **Definition**: A lambda function is a small, anonymous function defined with the `lambda` keyword. It can take any number of arguments but can only have one expression.
      * **Example**: A lambda function to multiply two numbers.
        ```python
        multiply = lambda x, y: x * y
        print(multiply(4, 5)) # Output: 20
        ```
      * **Use Cases**: Lambda functions are often used for short, single-line operations, particularly as arguments to higher-order functions like `map()`, `filter()`, and `sorted()`.

-----

### 6\. File Handling

This section covers how to read from and write to files using Python.

  * **Opening and Closing Files**: The `open()` function is used to open a file. It takes the file path and a mode (`'r'` for read, `'w'` for write, `'a'` for append) as arguments. The `close()` method must be called to properly close the file and release system resources.
  * **The `with` Statement**: The `with` statement is the recommended way to handle files. It automatically closes the file, even if errors occur, making the code safer and cleaner.
    ```python
    # Writing to a file
    with open('example.txt', 'w') as file:
      file.write('Hello, World!')

    # Reading from a file
    with open('example.txt', 'r') as file:
      content = file.read()
      print(content) # Output: Hello, World!
    ```
