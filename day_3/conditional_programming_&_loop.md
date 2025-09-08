# Detailed Explanation of `ds_4_pythonbasics_3.ipynb`

This Jupyter notebook covers **basic Python programming concepts**, specifically focused on **conditional programming** and **loops**. Below is a step-by-step, detailed explanation of its contents with examples and thorough explanations.

---

## 1. Conditional Programming

Conditional programming allows programs to make decisions based on certain conditions using statements like `if`, `else`, and `elif`.

### Example 1: Simple Print Statement

```python
print("Hello")
```
**Explanation:**  
Prints `Hello` to the output. This is just a demonstration of the print function.

---

### Example 2: Simple If Statement

```python
age = 21

if age > 18:
  print("You are eligible to vote")
```
**Explanation:**  
- Variable `age` is set to 21.
- The condition checks if `age` is greater than 18.
- Since 21 > 18, it prints "You are eligible to vote".

---

### Example 3: If-Else Statement

```python
age = 17

if age > 18:
  print("You are eligible to vote")
else:
  print("You are not eligible to vote")
```
**Explanation:**  
- `age` is set to 17.
- Checks if `age` is greater than 18.
- Condition is false, so it executes the `else` block and prints "You are not eligible to vote".

---

### Example 4: User Input and Typecasting

```python
marks = int(input("Enter Your Marks "))   # User input is typecast to integer
print(marks)
print(marks > 80)
```
**Explanation:**  
- Prompts the user to enter marks. `input()` returns a string so it is converted to an integer using `int()`.
- Prints the entered marks.
- Checks if marks are greater than 80 and prints the Boolean result (`True` or `False`).

---

### Example 5: Pass/Fail Based on Marks

```python
marks = int(input("Enter your marks"))

if marks > 40:
  print("Pass")
else:
  print("Fail")
```
**Explanation:**  
- User enters their marks.
- If marks are greater than 40, prints "Pass".
- Otherwise, prints "Fail".

---

### Example 6: Assign Grades Based on Marks (Incorrect Implementation)

```python
marks = int(input("Enter your marks"))

if marks > 90:
  print("Grade A+")
if marks > 80:
  print("Grade A")
if marks > 70:
  print("Grade B+")
if marks > 60:
  print("Grade B")
if marks > 50:
  print("Grade C+")
if marks > 40:
  print("Grade C")
else:
  print("Fail")
```
**Explanation:**
- This implementation uses multiple `if` statements instead of `elif`.  
- If marks are 93, all conditions above 40 will be true, so it prints **all grades** above "Fail".
- This is **not the correct way** to assign exclusive grades.

**Example Output for marks = 93:**
```
Grade A+
Grade A
Grade B+
Grade B
Grade C+
Grade C
```
**Correct approach is shown below.**

---

### Example 7: Assign Grades Based on Marks (Correct Implementation)

```python
marks = int(input("Enter your marks"))

if marks > 90:
  print("Grade A+")
elif marks > 80:
  print("Grade A")
elif marks > 70:
  print("Grade B+")
elif marks > 60:
  print("Grade B")
elif marks > 50:
  print("Grade C+")
elif marks > 40:
  print("Grade C")
else:
  print("Fail")
```
**Explanation:**  
- Uses `elif` to ensure only one grade is assigned.
- Once a condition is true, subsequent conditions are not checked.

**Example Output for marks = 75:**  
```
Grade B+
```

---

### Example 8: Simulate Login Activity

```python
userid = input("Enter your user id ")
userpass = input("Enter the password ")

if userid == 'admin' and userpass == 'password':
  print("You are logged in")
else:
  print("Incorrrect credentials")
```
**Explanation:**  
- Prompts user for a user id and password.
- Checks if both match the required values.
- If both are correct, prints "You are logged in", else "Incorrrect credentials".

---

## 2. Loops in Python

Loops are used to execute a block of code multiple times.

### For Loop

#### Example 1: Print Statement Repetition

```python
print("Hello World!!")
print("Hello World!!")
# ... repeated 5 times
```
This is a manual repetition, not efficient for many repetitions.

#### Example 2: Using For Loop for Repetition

```python
for i in range(0,5):
  print(i , "Hello World")
```
**Explanation:**
- Loops from 0 to 4 (5 iterations).
- Prints the loop index and the string "Hello World".

**Output:**
```
0 Hello World
1 Hello World
2 Hello World
3 Hello World
4 Hello World
```

---

#### Example 3: List Iteration

```python
cities = ["Mumbai", "Delhi", "Bengaluru", "Hyderabad", "Chennai"]

print(cities[0] , len(cities[0]))
# ... prints for each index
```
Manual way to print each item.

**Using a For Loop:**

```python
for i in range(0,5):
  print(cities[i] , len(cities[i]))
```
Iterates over the indices, prints city name and its length.

**More Pythonic Way:**

```python
for city in cities:
  print(city, len(city))
```
Iterates directly over the elements.

**Output:**
```
Mumbai 6
Delhi 5
Bengaluru 9
Hyderabad 9
Chennai 7
```

---

### Example: Login Activity with Limited Attempts

```python
for i in range(0,3):
  userid = input("Enter your user id ")
  userpass = input("Enter the password ")

  if userid == 'admin' and userpass == 'password':
    print("You are logged in")
    break
  else:
    print("Incorrrect credentials")
```
**Explanation:**  
- Allows the user to try login up to 3 times.
- On correct credentials, prints success and breaks the loop.
- Otherwise, prints "Incorrrect credentials" each time.

---

### Example: Multiplication Table

```python
number = int(input("Enter a number"))

for i in range(1,11):
  print(f"{i} * {number} = {i * number}" )
```
**Explanation:**  
- Prompts user for a number.
- Loops from 1 to 10.
- Prints multiplication table for the entered number.

**Output for number = 9:**
```
1 * 9 = 9
2 * 9 = 18
...
10 * 9 = 90
```

---

## 3. String Formatting

### Example:

```python
name = "Gagan"

print(f"Hello {name}")
```
**Explanation:**  
- Uses f-string for formatting.
- Prints "Hello Gagan".

---

### Example: String Multiplication

```python
print('7' * 2)
print(7 * 2)
```
**Explanation:**
- `'7' * 2` results in '77' (string repeated).
- `7 * 2` results in 14 (integer multiplication).

**Output:**
```
77
14
```

---

## Summary of Concepts Covered

- **Conditional statements:** `if`, `else`, `elif`
- **User input:** Reading and typecasting inputs
- **Comparison and logical operators:** `>`, `and`
- **Loops:** `for` loop with range and with lists
- **Break statement:** Exit loop on condition
- **String formatting:** f-strings
- **String vs. integer multiplication**

---

## Key Takeaways

- Use `if-elif-else` for mutually exclusive conditions.
- Use loops (`for`) to efficiently repeat actions.
- Always convert user inputs to the intended data type.
- Use list iteration to handle collections.
- Break out of loops using the `break` statement when needed.
- Understand difference between string and numerical operations.

**This notebook provides a fundamental introduction to conditional logic and loops in Python, essential for beginner programmers.**
