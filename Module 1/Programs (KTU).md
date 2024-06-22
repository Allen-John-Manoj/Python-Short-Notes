### 1. Write a python program to input a time in seconds and print the time in HH:MM:SS format.

**Answer:**

```python
# program to convert time in sec to HH:MM:SS format
time = input("Enter time in seconds")
time = int(time)
timeinmin = time // 60
timeinsec = time % 60
timeinhr = timeinmin // 60
timeinmin = timeinmin % 60
print("HH:MM:SS ---- {}:{}:{}".format(timeinhr, timeinmin, timeinsec))
```

### 2. Program to find Area and Circumference of a Circle.

**Answer:**

```python
# Python Program to find Area and Circumference of a Circle
# Standard formula to calculate the Area of a circle is: a = π r².
# Circumference c = 2 π r.
import math

r = input("Enter radius :")
r = int(r)
a = math.pi * r * r
c = 2 * math.pi * r
print("Area of the circle", a)
print("Circumference of the circle", c)
```

### 3. Write a python program to check whether a number is even or odd.

**Answer:**

```python
x = int(input("Enter a number...:"))
if x % 2 == 0:
    print("number is even")
else:
    print("number is odd")
```

### 4. Program to compare two numbers.

**Answer:**

```python
x = int(input("Enter first number.."))
y = int(input("Enter second number.."))
if x > y:
    print("x is greater than y")
elif x < y:
    print("x is smaller than y")
else:
    print("x and y are equal")
```

### 5. Program to find the roots of a quadratic equation.

**Answer:**

```python
import math

print("enter a b and c the coefficients line by line")
a = int(input())
b = int(input())
c = int(input())
if a == 0:
    print("Not a quadratic equation..root is ", -c / b)
else:
    d = b * b - 4 * a * c
    if d == 0:
        print("only one root", -b / (2 * a))
    elif d > 0:
        print("roots are real")
        print("root1", -b + math.sqrt(d) / (2 * a))
        print("root2", -b - math.sqrt(d) / (2 * a))
    else:
        print("roots are imaginary")
```

### 6. Program that accepts the length of three sides of a triangle as input and determine whether or not the triangle is a right angled triangle.

**Answer:**

```python
a = int(input("enter side a..:"))
b = int(input("enter side b..:"))
c = int(input("enter side c..:"))
if a + b > c and a + c > b and b + c > a:
    if a ** 2 + b ** 2 == c ** 2:
        print("Right angled triangle")
    else:
        print("Not a right angled triangle")
else:
    print("given sides do not form a triangle")
```

### 7. Program to input a point and find the quadrant.

**Answer:**

```python
x = int(input("Enter x:"))
y = int(input("enter y:"))
if x > 0 and y > 0:
    print("first quadrant")
elif x < 0 and y > 0:
    print("second quadrant")
elif x < 0 and y < 0:
    print("third quadrant")
elif x > 0 and y < 0:
    print("fourth quadrant")
else:
    print("point at origin")
```

### 8. Program to find the Sum of the digits of a number.

**Answer:**

```python
sum = 0
n = int(input("Enter a number.."))
while n != 0:
    sum = sum + n % 10
    n = n // 10
print("Sum of the digits =", sum)
```

### 9. Program to check whether the given number is prime or not.

**Answer:**

```python
n = int(input("Enter a number.."))
i = 2
prime = True
while i <= n // 2:
    if n % i == 0:
        prime = False
        break
    i = i + 1
if prime:
    print('Prime number')
else:
    print('Not a prime number')
```

### 10. Python program to find the sum of even numbers from N given numbers.

**Answer:**

```python
sum = 0
N = int(input("enter the number of numbers (N).."))
print("Enter the Numbers")
for i in range(N):
    num = int(input())
    if num % 2 == 0:
        sum = sum + num
print("Sum of even numbers..", sum)
```

### 11. Write a Python program which takes a positive integer n as input and finds the sum of cubes of all positive even numbers less than or equal to the number.

**Answer:**

```python
sum = 0
N = int(input("enter the number"))
for num in range(1, N + 1):
    if num % 2 == 0:
        sum = sum + num ** 3
print("Sum of cubes of even numbers..", sum)
```

### 12. Input 4 integers (+ve and −ve). Write a Python code to find the sum of negative numbers, positive numbers, and print them. Also, find the averages of these two groups of numbers and print.

**Answer:**

```python
psum = 0
nsum = 0
pc = 0
nc = 0
print("Enter the 4 Numbers +ve and -ve")
for i in range(4):
    num = int(input())
    if num > 0:
        psum = psum + num
        pc = pc + 1
    else:
        nsum = nsum + num
        nc = nc + 1
print("Sum of +ve numbers..", psum)
if pc != 0:
    print("Avg of +ve numbers..", psum / pc)
print("Sum of -ve numbers..", nsum)
if nc != 0:
    print("Avg of -ve numbers..", nsum / nc)
```

### 13. Write a Python program to reverse a number. Prompt the user for input.

**Answer:**

```python
rev = 0
print("Enter a number")
num = int(input())
while num != 0:
    d = num % 10
    rev = rev * 10 + d
    num = num // 10
print("Reverse of the number =", rev)
```

### 14. Generate first 10 Fibonacci numbers.

**Answer:**

```python
a = 0
b = 1
for i in range(10):
    c = a + b
    a = b
    b = c
    print(c)
```

### 15. Print Prime numbers less than 1000.

**Answer:**

```python
print("Prime numbers less than 1000")
for n in range(2, 1000):
    i = 2
    while i <= n / 2:
        if n % i == 0:
            break
        i = i + 1
    else:
        print(n, end=' ')
```

### 16. Write a Nested loop to print the following pattern.

```
5 4 3 2 1
4 3 2 1
3 2 1
2 1
1
```

**Answer:**

```python
n = int(input("Enter a number::"))
for i in range(n, 0, -1):
    for j in range(i, 0, -1):
        print(j, end=' ')
    print()
```

### 17. Print Multiplication table of 1-n numbers.

**Answer:**

```python
n = int(input("Enter n::"))
for k in range(1, n + 1):
    for i in range(1, 11):
        print(k, "X", i, "=", k * i)
    print()
```

### 18. Write a python program to check Armstrong number of n digits.

**Answer:**

```python
# Python program to check if the given 3 digit number is an Armstrong number or not
# take input from the user
num = int(input("Enter a number: "))

# initialize sum
sum = 0

# find the sum of the cube of each digit
temp = num
while temp > 0:
    digit = temp % 10
    sum += digit ** 3
    temp //= 10

# display the result
if num == sum:
    print(num, "is an Armstrong number")
else:
    print(num, "is not an Armstrong number")
```

**Output:**

```
Enter a number: 663
663 is not an Armstrong number

Enter a number: 407
407 is an Armstrong number
```

### 19. Check Armstrong number of n digits. Example: 1634 = 1^4 + 6^4 + 3^4 + 4^4 = 1634

**Answer:**

```python
num = int(input("Enter a number..."))

# Changed num variable to string, and calculated the length (number of digits)
order = len(str(num))

# initialize sum
sum = 0

# find the sum of the cube of each digit
temp = num
while temp > 0:
    digit = temp % 10
    sum += digit ** order
    temp //= 10

# display the result
if num == sum:
    print(num, "is an Armstrong number")
else:
    print(num, "is not an Armstrong number")
```

**Output:**

```
Enter a number...1634
1634 is an Armstrong number
```
