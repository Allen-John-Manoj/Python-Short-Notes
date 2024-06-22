### Basic Coding Skills in Python

#### Strings

Strings in Python are sequences of characters enclosed in single, double, or triple quotes. They are immutable, meaning once created, they cannot be changed.

- **Creating Strings:**
  ```python
  single_quote = 'Hello'
  double_quote = "World"
  triple_quote = '''This is a multi-line
  string'''
  ```

- **Common String Operations:**
  ```python
  # Concatenation
  hello_world = single_quote + ' ' + double_quote
  print(hello_world)  # Output: Hello World

  # Repetition
  repeated = single_quote * 3
  print(repeated)  # Output: HelloHelloHello

  # Slicing
  slice_example = hello_world[0:5]
  print(slice_example)  # Output: Hello

  # Length
  length = len(hello_world)
  print(length)  # Output: 11

  # Methods
  upper = hello_world.upper()
  print(upper)  # Output: HELLO WORLD

  lower = hello_world.lower()
  print(lower)  # Output: hello world
  ```

#### Numeric Data Types

Python supports various numeric data types, including integers, floating-point numbers, and complex numbers.

- **Integers:**
  ```python
  int_num = 10
  ```

- **Floating-Point Numbers:**
  ```python
  float_num = 10.5
  ```

- **Complex Numbers:**
  ```python
  complex_num = 1 + 2j
  ```

- **Basic Operations:**
  ```python
  # Addition
  add = int_num + float_num
  print(add)  # Output: 20.5

  # Subtraction
  sub = int_num - float_num
  print(sub)  # Output: -0.5

  # Multiplication
  mul = int_num * float_num
  print(mul)  # Output: 105.0

  # Division
  div = int_num / float_num
  print(div)  # Output: 0.9523809523809523

  # Floor Division
  floor_div = int_num // 3
  print(floor_div)  # Output: 3

  # Modulus
  mod = int_num % 3
  print(mod)  # Output: 1

  # Exponentiation
  exp = int_num ** 2
  print(exp)  # Output: 100
  ```

#### Character Sets

Character sets define the valid characters that can be used in strings and their encoding schemes.

- **ASCII:**
  - 7-bit encoding scheme for characters.
  - Supports 128 characters.

- **Unicode:**
  - Supports characters from all languages.
  - UTF-8 and UTF-16 are common Unicode encodings.

- **Example:**
  ```python
  # ASCII value
  ascii_value = ord('A')
  print(ascii_value)  # Output: 65

  # Character from ASCII value
  char = chr(65)
  print(char)  # Output: A
  ```

#### Expressions

Expressions are combinations of values, variables, operators, and function calls that are evaluated to produce a result.

- **Examples of Expressions:**
  ```python
  x = 10
  y = 5

  # Arithmetic Expression
  result = x + y * 2
  print(result)  # Output: 20

  # Boolean Expression
  is_greater = x > y
  print(is_greater)  # Output: True

  # String Expression
  full_name = "John" + " " + "Doe"
  print(full_name)  # Output: John Doe
  ```

#### Using Inbuilt Functions and Modules

Python provides a rich set of inbuilt functions and modules to perform various tasks.

- **Inbuilt Functions:**
  ```python
  # Absolute Value
  abs_value = abs(-5)
  print(abs_value)  # Output: 5

  # Minimum and Maximum
  minimum = min(1, 2, 3)
  print(minimum)  # Output: 1

  maximum = max(1, 2, 3)
  print(maximum)  # Output: 3

  # Sum
  total = sum([1, 2, 3])
  print(total)  # Output: 6

  # Round
  rounded = round(3.456, 2)
  print(rounded)  # Output: 3.46
  ```

- **Importing and Using Modules:**
  ```python
  # Importing the math module
  import math

  # Using functions from the math module
  sqrt_value = math.sqrt(16)
  print(sqrt_value)  # Output: 4.0

  pi_value = math.pi
  print(pi_value)  # Output: 3.141592653589793

  # Importing specific functions from a module
  from math import factorial, gcd

  fact = factorial(5)
  print(fact)  # Output: 120

  gcd_value = gcd(24, 36)
  print(gcd_value)  # Output: 12
  ```

### Example Programs

1. **String Manipulation Program:**
  ```python
  def reverse_string(s):
      return s[::-1]

  def is_palindrome(s):
      return s == s[::-1]

  input_string = "madam"
  print("Reversed String:", reverse_string(input_string))
  print("Is Palindrome:", is_palindrome(input_string))
  ```

2. **Numeric Operations Program:**
  ```python
  def calculate_area(radius):
      import math
      return math.pi * radius ** 2

  radius = 5
  print("Area of Circle:", calculate_area(radius))
  ```

3. **Character Set Program:**
  ```python
  def ascii_table():
      for i in range(32, 128):
          print(chr(i), end=" ")

  ascii_table()
  ```

4. **Using Inbuilt Functions and Modules:**
  ```python
  import random

  def generate_random_numbers(count):
      return [random.randint(1, 100) for _ in range(count)]

  random_numbers = generate_random_numbers(10)
  print("Random Numbers:", random_numbers)
  print("Minimum:", min(random_numbers))
  print("Maximum:", max(random_numbers))
  print("Sum:", sum(random_numbers))
  ```

By mastering these basic concepts, you'll be well-equipped to tackle more advanced topics in Python programming.
