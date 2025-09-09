
## 1. If Statements

### Explanation

The **if statement** is a fundamental control structure in Python that allows you to execute a block of code only if a certain condition is true. It's used for decision making.

**Syntax Example:**
```python
if condition:
    # code to execute if condition is True
```

### Example from the Notebook

```python
age = 18

if age < 21:
    print("You can have student discount")
```

**Explanation:**  
- Here, the variable `age` is set to 18.
- The condition checks if `age` is less than 21.
- Since 18 < 21 is `True`, the print statement executes:  
  Output: `You can have student discount`

**Further Example:**
```python
temperature = 30

if temperature > 25:
    print("It's a hot day")
```
- Output: `It's a hot day` (because 30 > 25 is True)

---

## 2. While Loops

### Explanation

A **while loop** repeatedly executes a block of code as long as a condition remains true. It's useful for tasks where you don't know in advance how many times you need to repeat an action.

**Syntax Example:**
```python
while condition:
    # code to repeat while condition is True
```

### Example from the Notebook

#### Problematic Example (Infinite Loop)

```python
age = 18

while age < 21:
    print("You can have student discount")
```

**Explanation:**  
- The variable `age` starts at 18.
- The condition `age < 21` is always true inside the loop, and there's no code that changes `age`.
- This results in an **infinite loop:**  
  - The message `You can have student discount` prints endlessly.
- In practice, infinite loops should be avoided unless intentionally required (for example, in servers that run forever until stopped).

#### Corrected Example

To prevent infinite loops, you should modify the condition variable inside the loop:

```python
age = 18

while age < 21:
    print("You can have student discount")
    age += 1  # increment age to eventually break the loop
```
**Explanation:**  
- Now, each time the loop runs, `age` increases by 1.
- The loop will print the message for ages 18, 19, and 20, then stop when `age` becomes 21.

**Output:**
```
You can have student discount
You can have student discount
You can have student discount
```

---

## 3. How While Loops Work (Markdown Explanation)

The notebook includes a markdown cell explaining how while loops function:
- The loop checks the condition and triggers activity if true.
- It rechecks the condition and repeats the activity.
- The loop continues until the condition becomes false.

**Summary:**  
While loops are useful for repeating actions where the number of repetitions depends on a condition rather than being predetermined.

---

## Additional Examples

### Using While Loop for Counting

```python
counter = 1

while counter <= 5:
    print("Counter is:", counter)
    counter += 1
```
**Output:**
```
Counter is: 1
Counter is: 2
Counter is: 3
Counter is: 4
Counter is: 5
```

### Using If Statement for Conditions

```python
score = 85

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
else:
    print("Grade: C")
```
**Output:**  
`Grade: B` (since 85 >= 80 but < 90)

---

## Summary Table

| Concept      | Purpose                             | Example                                  | Notes                      |
|--------------|-------------------------------------|------------------------------------------|----------------------------|
| If Statement | Decision making                     | `if age < 21: ...`                       | Executes once if true      |
| While Loop   | Repeated execution based on condition| `while age < 21: ...`                    | Infinite if not updated    |

---

## Conclusion

This notebook teaches you:
- How to use **if statements** for making decisions in code.
- How to use **while loops** for repetitive tasks based on a condition.
- The importance of updating loop variables to avoid infinite loops.

If you need further details or want to see more advanced use cases, let me know!
