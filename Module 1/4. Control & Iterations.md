### Control Statements in Python

Control statements manage the flow of a program by executing different statements based on conditions.

#### If Statement

The `if` statement evaluates a condition and executes a block of code if the condition is `True`.

```python
x = 10
if x > 5:
    print("x is greater than 5")
```

#### If-Else Statement

The `if-else` statement provides an alternative block of code to execute if the condition is `False`.

```python
x = 10
if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
```

#### Elif Statement

The `elif` statement allows for multiple conditions to be checked sequentially.

```python
x = 10
if x > 15:
    print("x is greater than 15")
elif x > 5:
    print("x is greater than 5 but less than or equal to 15")
else:
    print("x is 5 or less")
```

### Iteration with for/while Loop

#### For Loop

The `for` loop iterates over a sequence (such as a list, tuple, or string).

```python
# Iterating over a list
numbers = [1, 2, 3, 4, 5]
for number in numbers:
    print(number)

# Iterating over a string
for char in "Hello":
    print(char)
```

#### While Loop

The `while` loop executes a block of code as long as a condition is `True`.

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### Formatting Text for Output

Python provides several ways to format text for output, such as using the `format()` method, f-strings (formatted string literals), and the `%` operator.

#### Using format() Method

```python
name = "Alice"
age = 25
print("Name: {}, Age: {}".format(name, age))
```

#### Using F-strings

Introduced in Python 3.6, f-strings provide a concise way to include expressions inside string literals.

```python
name = "Alice"
age = 25
print(f"Name: {name}, Age: {age}")
```

#### Using % Operator

```python
name = "Alice"
age = 25
print("Name: %s, Age: %d" % (name, age))
```

### Case Study: Simple Calculator

Let's create a simple calculator program that demonstrates control statements, iteration, and formatted output.

#### Step-by-Step Implementation

1. **Define Functions for Basic Operations:**

```python
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Division by zero error"
```

2. **Display Menu:**

```python
def display_menu():
    print("\nSimple Calculator")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")
    print("5. Exit")
```

3. **Main Program Loop:**

```python
while True:
    display_menu()
    choice = input("Enter your choice (1-5): ")

    if choice == '5':
        print("Exiting the program.")
        break

    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))

    if choice == '1':
        result = add(num1, num2)
        print(f"The result is: {result:.2f}")
    elif choice == '2':
        result = subtract(num1, num2)
        print(f"The result is: {result:.2f}")
    elif choice == '3':
        result = multiply(num1, num2)
        print(f"The result is: {result:.2f}")
    elif choice == '4':
        result = divide(num1, num2)
        print(f"The result is: {result}")
    else:
        print("Invalid choice. Please try again.")
```

#### Example Output:

```
Simple Calculator
1. Add
2. Subtract
3. Multiply
4. Divide
5. Exit
Enter your choice (1-5): 1
Enter first number: 10
Enter second number: 5
The result is: 15.00

Simple Calculator
1. Add
2. Subtract
3. Multiply
4. Divide
5. Exit
Enter your choice (1-5): 4
Enter first number: 10
Enter second number: 0
The result is: Division by zero error

Simple Calculator
1. Add
2. Subtract
3. Multiply
4. Divide
5. Exit
Enter your choice (1-5): 5
Exiting the program.
```

### Summary

This study guide covers the basics of control statements, iteration with loops, text formatting, and a simple calculator case study in Python. By understanding these fundamental concepts, you'll be able to build more complex programs and develop your coding skills further.
