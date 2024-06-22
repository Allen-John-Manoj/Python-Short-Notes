### Program Questions

#### 1. Palindrome Checker
Write a program to check if a given string is a palindrome. A string is a palindrome if it reads the same forward and backward.

**Example:**
```python
def is_palindrome(s):
    return s == s[::-1]

# Test Cases
print(is_palindrome("madam"))  # Output: True
print(is_palindrome("hello"))  # Output: False
```

#### 2. Reverse a String
Write a program to reverse a given string.

**Example:**
```python
def reverse_string(s):
    return s[::-1]

# Test Cases
print(reverse_string("hello"))  # Output: "olleh"
print(reverse_string("Python"))  # Output: "nohtyP"
```

#### 3. Count Vowels and Consonants
Write a program to count the number of vowels and consonants in a given string.

**Example:**
```python
def count_vowels_and_consonants(s):
    vowels = "aeiouAEIOU"
    v_count = 0
    c_count = 0
    for char in s:
        if char in vowels:
            v_count += 1
        elif char.isalpha():
            c_count += 1
    return v_count, c_count

# Test Cases
print(count_vowels_and_consonants("hello"))  # Output: (2, 3)
print(count_vowels_and_consonants("Python"))  # Output: (1, 5)
```

#### 4. Check if Two Strings are Anagrams
Write a program to check if two strings are anagrams of each other. Two strings are anagrams if they contain the same characters with the same frequencies.

**Example:**
```python
def are_anagrams(str1, str2):
    return sorted(str1) == sorted(str2)

# Test Cases
print(are_anagrams("listen", "silent"))  # Output: True
print(are_anagrams("hello", "world"))    # Output: False
```

#### 5. Generate Fibonacci Sequence
Write a program to generate the first N numbers in the Fibonacci sequence.

**Example:**
```python
def fibonacci(n):
    sequence = [0, 1]
    while len(sequence) < n:
        sequence.append(sequence[-1] + sequence[-2])
    return sequence[:n]

# Test Cases
print(fibonacci(5))  # Output: [0, 1, 1, 2, 3]
print(fibonacci(10)) # Output: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```

#### 6. Factorial of a Number
Write a program to compute the factorial of a number.

**Example:**
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

# Test Cases
print(factorial(5))  # Output: 120
print(factorial(0))  # Output: 1
```

#### 7. Find the Maximum and Minimum in a List
Write a program to find the maximum and minimum values in a list without using inbuilt functions like `max()` and `min()`.

**Example:**
```python
def find_max_min(lst):
    max_val = lst[0]
    min_val = lst[0]
    for num in lst:
        if num > max_val:
            max_val = num
        if num < min_val:
            min_val = num
    return max_val, min_val

# Test Cases
print(find_max_min([3, 5, 7, 2, 8]))  # Output: (8, 2)
print(find_max_min([1, -1, 0, 4, -5]))  # Output: (4, -5)
```

#### 8. Count Words in a String
Write a program to count the number of words in a given string.

**Example:**
```python
def count_words(s):
    words = s.split()
    return len(words)

# Test Cases
print(count_words("Hello world"))  # Output: 2
print(count_words("This is a test string"))  # Output: 5
```

#### 9. Sum of Digits
Write a program to calculate the sum of the digits of a given number.

**Example:**
```python
def sum_of_digits(n):
    return sum(int(digit) for digit in str(n))

# Test Cases
print(sum_of_digits(12345))  # Output: 15
print(sum_of_digits(9876))   # Output: 30
```

#### 10. Find Prime Numbers up to N
Write a program to find all prime numbers up to a given number N.

**Example:**
```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def prime_numbers_up_to(n):
    return [num for num in range(2, n + 1) if is_prime(num)]

# Test Cases
print(prime_numbers_up_to(10))  # Output: [2, 3, 5, 7]
print(prime_numbers_up_to(20))  # Output: [2, 3, 5, 7, 11, 13, 17, 19]
```

#### 11. Find the Longest Word in a String
Write a program to find the longest word in a given string.

**Example:**
```python
def longest_word(s):
    words = s.split()
    longest = max(words, key=len)
    return longest

# Test Cases
print(longest_word("Hello world this is a test string"))  # Output: "string"
print(longest_word("Find the longest word"))  # Output: "longest"
```

#### 12. Sort Words in Alphabetical Order
Write a program to sort the words in a string in alphabetical order.

**Example:**
```python
def sort_words(s):
    words = s.split()
    words.sort()
    return ' '.join(words)

# Test Cases
print(sort_words("banana apple cherry"))  # Output: "apple banana cherry"
print(sort_words("sort these words alphabetically"))  # Output: "alphabetically sort these words"
```

#### 13. Convert Decimal to Binary
Write a program to convert a given decimal number to its binary representation.

**Example:**
```python
def decimal_to_binary(n):
    return bin(n).replace("0b", "")

# Test Cases
print(decimal_to_binary(10))  # Output: "1010"
print(decimal_to_binary(255))  # Output: "11111111"
```

#### 14. Find the GCD of Two Numbers
Write a program to find the greatest common divisor (GCD) of two numbers.

**Example:**
```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

# Test Cases
print(gcd(48, 18))  # Output: 6
print(gcd(100, 25))  # Output: 25
```

#### 15. Generate Pascal's Triangle
Write a program to generate Pascal's Triangle up to a given number of rows.

**Example:**
```python
n = 6

# iterate up to n
for i in range(n):
    # adjust space
    print(' '*(n-i), end='')

    # compute each value in the row
    coef = 1
    for j in range(0, i + 1):
        print(coef, end=' ')
        coef = coef * (i - j) // (j + 1)
    print()

#Output
#      1 
#     1 1 
#    1 2 1 
#   1 3 3 1 
#  1 4 6 4 1 
# 1 5 10 10 5 1 
```

### Indirect and Tough Questions

#### 16. Find the First Non-Repeating Character in a String
Write a program to find the first non-repeating character in a string.

**Example:**
```python
def first_non_repeating_char(s):
    char_count = {}
    for char in s:
        if char in char_count:
            char_count[char] += 1
        else:
            char_count[char] = 1
    for char in s:
        if char_count[char] == 1:
            return char
    return None

# Test Cases
print(first_non_repeating_char("swiss"))  # Output: "w"
print(first_non_repeating_char("repetition"))  # Output: "r"
```

#### 17. Find the Missing Number in an Array
Write a program to find the missing number in an array of integers from 1 to n.

**Example:**
```python
def find_missing_number(arr, n):
    expected_sum = n * (n + 1) // 2
    actual_sum = sum(arr)
    return expected_sum - actual_sum

# Test Cases
print(find_missing_number([1, 2, 4, 5, 6], 6))  # Output: 3
print(find_missing_number([1, 3, 4, 5, 6], 6))  # Output: 2
```

#### 18. Check if a Number is a Perfect Square
Write a program to check if a given number is a perfect square.

**Example:**
```python
def is_perfect_square(n):
    return int(n**0

.5)**2 == n

# Test Cases
print(is_perfect_square(25))  # Output: True
print(is_perfect_square(26))  # Output: False
```

#### 19. Find the Longest Substring Without Repeating Characters
Write a program to find the longest substring without repeating characters.

**Example:**
```python
def longest_unique_substring(s):
    start = 0
    max_length = 0
    used_chars = {}

    for i, char in enumerate(s):
        if char in used_chars and start <= used_chars[char]:
            start = used_chars[char] + 1
        else:
            max_length = max(max_length, i - start + 1)
        used_chars[char] = i

    return max_length

# Test Cases
print(longest_unique_substring("abcabcbb"))  # Output: 3 ("abc")
print(longest_unique_substring("bbbbb"))     # Output: 1 ("b")
```

#### 20. Rotate a Matrix
Write a program to rotate a given NxN matrix 90 degrees clockwise.

**Example:**
```python
def rotate_matrix(matrix):
    n = len(matrix)
    for i in range(n // 2):
        for j in range(i, n - i - 1):
            temp = matrix[i][j]
            matrix[i][j] = matrix[n - j - 1][i]
            matrix[n - j - 1][i] = matrix[n - 1 - i][n - j - 1]
            matrix[n - 1 - i][n - j - 1] = matrix[j][n - 1 - i]
            matrix[j][n - 1 - i] = temp
    return matrix

# Test Cases
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
rotated_matrix = rotate_matrix(matrix)
for row in rotated_matrix:
    print(row)
# Output:
# [7, 4, 1]
# [8, 5, 2]
# [9, 6, 3]
```

#### 21. Check if a String is a Rotation of Another
Write a program to check if one string is a rotation of another.

**Example:**
```python
def is_rotation(s1, s2):
    if len(s1) != len(s2):
        return False
    return s2 in s1 + s1

# Test Cases
print(is_rotation("waterbottle", "erbottlewat"))  # Output: True
print(is_rotation("hello", "lloeh"))              # Output: False
```

#### 22. Find the Majority Element in an Array
Write a program to find the majority element in an array. The majority element is the element that appears more than n/2 times.

**Example:**
```python
def find_majority_element(arr):
    count = 0
    candidate = None

    for num in arr:
        if count == 0:
            candidate = num
        count += (1 if num == candidate else -1)

    return candidate

# Test Cases
print(find_majority_element([3, 3, 4, 2, 4, 4, 2, 4, 4]))  # Output: 4
print(find_majority_element([3, 3, 4, 2, 4, 4, 2, 4]))    # Output: 4
```

These questions are designed to test your understanding of various Python concepts such as strings, control structures, functions, loops, and more. Some questions are straightforward, while others require a deeper understanding and application of multiple concepts.
