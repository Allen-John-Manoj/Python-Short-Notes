### Selection Structures in Python

#### If-Else Statement

The `if-else` statement in Python allows you to execute a block of code if a condition is true and another block if it is false.

**Syntax:**
```python
if condition:
    # code block executed if condition is true
else:
    # code block executed if condition is false
```

**Example:**
```python
x = 10
if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
```

#### Elif Statement

The `elif` statement is used to check multiple conditions sequentially.

**Syntax:**
```python
if condition1:
    # code block executed if condition1 is true
elif condition2:
    # code block executed if condition2 is true
else:
    # code block executed if none of the conditions are true
```

**Example:**
```python
x = 10
if x > 15:
    print("x is greater than 15")
elif x > 5:
    print("x is greater than 5 but less than or equal to 15")
else:
    print("x is 5 or less")
```

#### Switch-Case Equivalent in Python

Python does not have a built-in `switch-case` construct like other languages (e.g., C, Java). However, you can use dictionaries to mimic a `switch-case` statement.

**Example:**
```python
def switch_case_example(value):
    switcher = {
        1: "One",
        2: "Two",
        3: "Three",
    }
    return switcher.get(value, "Invalid value")

print(switch_case_example(1))  # Output: One
print(switch_case_example(4))  # Output: Invalid value
```

### Conditional Iteration with While

The `while` loop in Python allows you to execute a block of code repeatedly as long as a condition is true.

**Syntax:**
```python
while condition:
    # code block executed repeatedly as long as condition is true
```

**Example:**
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### Case Study: Number Guessing Game

Let's create a simple number guessing game to demonstrate selection structures, conditional iteration, and lazy evaluation.

#### Step-by-Step Implementation

1. **Define the Game Logic:**

```python
import random

def guess_number_game():
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guess = None

    while guess != number_to_guess:
        guess = int(input("Enter your guess (between 1 and 100): "))
        attempts += 1

        if guess < number_to_guess:
            print("Too low!")
        elif guess > number_to_guess:
            print("Too high!")

    print(f"Congratulations! You guessed the number in {attempts} attempts.")
```

2. **Start the Game:**

```python
if __name__ == "__main__":
    guess_number_game()
```

#### Example Output:

```
Enter your guess (between 1 and 100): 50
Too low!
Enter your guess (between 1 and 100): 75
Too high!
Enter your guess (between 1 and 100): 60
Too low!
Enter your guess (between 1 and 100): 70
Congratulations! You guessed the number in 4 attempts.
```

### Testing Control Statements

Testing control statements involves checking different paths in your code to ensure all conditions are handled correctly. You can use various test cases to verify your program's behavior.

**Example Tests for the Number Guessing Game:**

- Guess a number lower than the target number.
- Guess a number higher than the target number.
- Guess the exact target number.
- Verify that the program counts the number of attempts correctly.

### Lazy Evaluation

Lazy evaluation is an evaluation strategy where an expression is not evaluated until its value is needed. This can be beneficial for performance optimization.

**Example of Lazy Evaluation:**

Python's `and` and `or` operators use lazy evaluation. They short-circuit, meaning they stop evaluating as soon as the result is determined.

**Example:**

```python
def lazy_evaluation_example(x):
    return x == 10 or expensive_function()

def expensive_function():
    print("Expensive function called")
    return True

print(lazy_evaluation_example(10))  # Output: True (expensive_function is not called)
print(lazy_evaluation_example(5))   # Output: Expensive function called
                                    #         True
```

In the first call, `expensive_function` is not called because `x == 10` evaluates to `True`. In the second call, `expensive_function` is called because `x == 5` evaluates to `False`.

### Summary

This guide covers selection structures (if-else, switch-case equivalent), conditional iteration with `while`, a case study of a number guessing game, testing control statements, and lazy evaluation in Python. By understanding these concepts, you'll be able to write more complex and efficient programs.
