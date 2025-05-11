07-05-2025 08:44:16

Status : #child

Tags : [[LeetCode]] [[Data Types]] [[Arrays]] [[Strings]]

This module covers foundational Python knowledge critical for writing clean, efficient, and correct Data Structures and Algorithms (DSA) code, particularly for platforms like LeetCode.
## 1. Variables & Data Types 

In Python, you don't need to declare a variable's type explicitly. The type is inferred at runtime.

*   **`int`**: Whole numbers (e.g., `10`, `-3`, `0`).
*   **`float`**: Numbers with a decimal point (e.g., `3.14`, `-0.001`, `2.0`).
*   **`str`**: Sequences of characters (e.g., `"hello"`, `'world'`).
*   **`bool`**: Truth values, either `True` or `False`.

```python
# Examples
age = 30                     # int
price = 19.99                # float
name = "Alice"               # str
is_student = True            # bool

print(type(age), type(price), type(name), type(is_student))
# Output: <class 'int'> <class 'float'> <class 'str'> <class 'bool'>
```

## 2. Mutability vs. Immutability

This is a crucial concept in Python.

- **Mutable Objects:** Their state or content can be changed after creation.
    - Examples: list, dict, set.
- **Immutable Objects:** Their state or content cannot be changed after creation. Any operation that appears to modify an immutable object actually creates a new object.    
    - Examples: int, float, str, tuple, bool, frozenset.

```python
# Mutable example: list
my_list = [1, 2, 3]
print(f"Original list: {my_list}, id: {id(my_list)}")
my_list.append(4) # Modifies the original list object
print(f"Modified list: {my_list}, id: {id(my_list)}") # id remains the same

# Immutable example: string
my_string = "hello"
print(f"Original string: {my_string}, id: {id(my_string)}")
my_string = my_string + " world" # Creates a NEW string object
print(f"New string: {my_string}, id: {id(my_string)}") # id changes

# Immutable example: tuple
my_tuple = (1, 2, 3)
# my_tuple[0] = 5  # This would raise a TypeError: 'tuple' object does not support item assignment
```

> -  Understanding mutability helps predict behavior, especially when passing objects to functions or when multiple variables reference the same mutable object. 
> - Immutable objects (like tuples or strings) can be used as keys in dictionaries or elements in sets, while mutable objects (like lists) generally cannot directly.

## 3. Object References & Copying

When you assign a variable to an object, you are essentially creating a reference (or a name/label) pointing to that object in memory.

**a) Assignment (Reference):**  
Assigning one variable to another (for mutable types) makes both variables point to the same object. Modifying the object through one variable affects the other.

```python
list_a = [1, 2, 3]
list_b = list_a       # list_b now refers to the SAME object as list_a

print(f"list_a: {list_a}, id: {id(list_a)}")
print(f"list_b: {list_b}, id: {id(list_b)}")

list_b.append(4)
print(f"After list_b.append(4):")
print(f"list_a: {list_a}") # Output: [1, 2, 3, 4] (list_a is also changed)
print(f"list_b: {list_b}") # Output: [1, 2, 3, 4]
```

**b) Shallow Copy:**  

Creates a new object, but if the object contains other objects (like a list of lists), it copies references to those inner objects.
Methods for shallow copy:
- object.copy() (for list, dict, set)
- Slicing [:] (for list)
- list(original_list)
- dict(original_dict)
- set(original_set)
- copy.copy() from the copy module.

```python
import copy

original_list = [1, [10, 20], 3]
shallow_copied_list = original_list.copy()
# or shallow_copied_list = original_list[:]
# or shallow_copied_list = copy.copy(original_list)

print(f"Original: {original_list}, id: {id(original_list)}")
print(f"Shallow Copy: {shallow_copied_list}, id: {id(shallow_copied_list)}")
print(f"Inner list (Original): id: {id(original_list[1])}")
print(f"Inner list (Shallow):  id: {id(shallow_copied_list[1])}") # Same id for inner list

shallow_copied_list.append(4)          # Does not affect original_list
shallow_copied_list[1].append(30)      # AFFECTS original_list's inner list

print(f"Original after modifications: {original_list}")
# Output: [1, [10, 20, 30], 3]
print(f"Shallow copy after modifications: {shallow_copied_list}")
# Output: [1, [10, 20, 30], 3, 4]
```

**c) Deep Copy:**  
Creates a new object and recursively copies all objects found within the original. No shared references to nested objects.
Method for deep copy:
- copy.deepcopy() from the copy module.

```python
import copy

original_list_deep = [1, [10, 20], 3]
deep_copied_list = copy.deepcopy(original_list_deep)

print(f"Original Deep: {original_list_deep}, id: {id(original_list_deep)}")
print(f"Deep Copy: {deep_copied_list}, id: {id(deep_copied_list)}")
print(f"Inner list (Original Deep): id: {id(original_list_deep[1])}")
print(f"Inner list (Deep Copy):     id: {id(deep_copied_list[1])}") # DIFFERENT id for inner list

deep_copied_list.append(4)
deep_copied_list[1].append(30) # Does NOT affect original_list_deep's inner list

print(f"Original Deep after modifications: {original_list_deep}")
# Output: [1, [10, 20], 3]
print(f"Deep copy after modifications: {deep_copied_list}")
# Output: [1, [10, 20, 30], 3, 4]
```

>- When you need to modify a copy of a data structure without affecting the original (e.g., in backtracking, or exploring paths in a graph), you need to decide if a shallow or deep copy is necessary.
>- Passing mutable objects to helper functions can lead to unintended side effects if not handled carefully.

## 4. Control Flow

**a) if/elif/else (Conditional Statements):**  
Executes code blocks based on whether conditions are true or false.

```python
score = 85
if score >= 90:    
    grade = "A"
elif score >= 80:    
    grade = "B"
elif score >= 70:    
    grade = "C"
else:    
    grade = "D"
print(f"Score: {score}, Grade: {grade}") # Output: Score: 85, Grade: B
```

**b) for Loops (Iteration):**  
Iterates over a sequence (like a list, tuple, str, range) or other iterable objects.

```python
# Iterate over a list 
names = ["Alice", "Bob", "Charlie"] 

for name in names:     
  print(f"Hello, {name}!")  
# Iterate using range() 
for i in range(5): # 0, 1, 2, 3, 4     
  print(i, end=" ") # Output: 0 1 2 3 4 print()  
print()

for i in range(1, 6): # 1, 2, 3, 4, 5   
  print(i, end=" ") # Output: 1 2 3 4 5 
print()

for i in range(0, 10, 2): # 0, 2, 4, 6, 8 (start, stop, step)     
  print(i, end=" ") # Output: 0 2 4 6 8  
print()

# Iterate with index and value using enumerate() 
for index, name in enumerate(names):     
  print(f"Index {index}: {name}")
```   

**c) while Loops:**  
Executes a block of code as long as a condition is true.

```python
# Using a while loop
count = 0
while count < 3:
    print(f"Count is {count}")
    count += 1  # Important: update the condition variable to avoid infinite loop

# Output:
# Count is 0
# Count is 1
# Count is 2

# Using a for loop with break and continue
# `break`: exits the current loop
# `continue`: skips the rest of the current iteration and proceeds to the next
for i in range(10):
    if i == 3:
        continue  # Skip printing 3
    if i == 7:
        break     # Stop loop when i is 7
    print(i, end=" ")

print()

# Output: 0 1 2 4 5 6
```
## 5. Functions

Blocks of reusable code that perform a specific task.

**a) Defining and Calling:**

```python
def greet(name):  # "name" is a parameter
    """This function greets the person passed in as a parameter."""  # Docstring
    message = f"Hello, {name}!"
    return message

greeting = greet("David")  # "David" is an argument
print(greeting)            # Output: Hello, David!
```

**b) Arguments:**
- **Positional Arguments:** Order matters.
- **Keyword Arguments:** Order doesn't matter if specified by name.
- **Default Argument Values:**

```python
def power(base, exponent=2):  # exponent has a default value
    return base ** exponent

print(power(3))                    # Output: 9 (3^2)
print(power(3, 3))                 # Output: 27 (3^3)
print(power(base=4, exponent=3))  # Output: 64
```

- ***args (Arbitrary Positional Arguments):** Collects extra positional arguments into a tuple.

```python
def sum_all(*numbers):  # numbers will be a tuple
    total = 0
    for num in numbers:
        total += num
    return total

print(sum_all(1, 2, 3))           # Output: 6
print(sum_all(10, 20, 30, 40))    # Output: 100
```

- ****kwargs (Arbitrary Keyword Arguments):** Collects extra keyword arguments into a dictionary.

```python
def print_info(**details):  # details will be a dictionary
    for key, value in details.items():
        print(f"{key}: {value}")

print_info(name="Eve", age=25, city="Wonderland")

# Output:
# name: Eve
# age: 25
# city: Wonderland
```

**c) Return Values:**

- A function can return one value, multiple values (as a tuple), or no value (implicitly returns None).

```python
def get_coordinates():
    return 10, 20  # Returns a tuple (10, 20)

x, y = get_coordinates()  # Tuple unpacking
print(f"x: {x}, y: {y}")   # Output: x: 10, y: 20


def no_return_func():
    print("Doing something.")

result = no_return_func()  # Output: Doing something.
print(result)              # Output: None

```
## 6. List Comprehensions

A concise way to create lists. Often more readable and efficient than using explicit for loops to build lists.

**Syntax:** [expression for item in iterable if condition]

```python
# Example 1: Squares of numbers
squares = []
for i in range(5):
    squares.append(i * i)
print(squares)  # Output: [0, 1, 4, 9, 16]

squares_comp = [i * i for i in range(5)]
print(squares_comp)  # Output: [0, 1, 4, 9, 16]

# Example 2: Squares of even numbers
even_squares = [i * i for i in range(10) if i % 2 == 0]
print(even_squares)  # Output: [0, 4, 16, 36, 64]

# Can also be used for dictionaries and sets
# {key_expr: value_expr for item in iterable if condition}
# {expr for item in iterable if condition}
```

**Why it matters for LeetCode:**

- Very common in Python solutions for conciseness.
- Often used for transforming or filtering data quickly.
## 7. Lambda Functions, map(), filter()

**a) Lambda Functions (Anonymous Functions):**  
Small, single-expression functions defined inline.  
**Syntax:** lambda arguments: expression

```python
# Using a lambda function to add two numbers
add = lambda x, y: x + y
print(add(5, 3))  # Output: 8

# Often used where a small function is needed for a short period
points = [(1, 2), (3, 1), (5, -4), (2, 3)]
# Sort points based on the second element of each tuple
points.sort(key=lambda point: point[1])
print(points)  # Output: [(5, -4), (3, 1), (1, 2), (2, 3)]
```

**b) map(function, iterable, ...):**  
Applies a given function to each item of an iterable (or iterables) and returns a map object (which is an iterator).

```python
# Squaring numbers using map and lambda
numbers = [1, 2, 3, 4]
squared_numbers_map = map(lambda x: x * x, numbers)
print(list(squared_numbers_map))  # Output: [1, 4, 9, 16]

# Using map with multiple iterables
list1 = [1, 2, 3]
list2 = [4, 5, 6]
sums_map = map(lambda x, y: x + y, list1, list2)
print(list(sums_map))  # Output: [5, 7, 9]
```

**c) filter(function, iterable):**  
Constructs an iterator from elements of an iterable for which a function returns true.

```python
# Filtering even numbers using filter and lambda
numbers = [1, 2, 3, 4, 5, 6]
even_numbers_filter = filter(lambda x: x % 2 == 0, numbers)
print(list(even_numbers_filter))  # Output: [2, 4, 6]
```

**Why it matters for LeetCode:**

- lambda is great for short, throwaway functions (e.g., custom sort keys).
- map and filter can provide concise ways to transform/filter data, though list comprehensions are often preferred for readability in simpler cases.
## 8. Introduction to Big O Notation

Big O notation is used to describe the **performance** or **complexity** of an algorithm. It specifically describes the **worst-case scenario** and focuses on how the algorithm's runtime or space usage scales as the **input size (n) grows**.

**a) What it means:**

- It's about the growth rate of resource usage (time or space).
- Ignores constant factors and lower-order terms because as n gets very large, these become insignificant.
    - e.g., O(2n + 100) becomes O(n). O(n^2 + n) becomes O(n^2).

**b) Common Complexities (from best to worst):**
- **O(1) - Constant Time:** Runtime is independent of the input size.
    - Example: Accessing an element in a list by index (my_list[i]), push/pop on a stack (implemented with list append/pop).
- **O(log n) - Logarithmic Time:** Runtime grows logarithmically with input size. Often seen in algorithms that divide the problem in half repeatedly.
    - Example: Binary search in a sorted array.
- **O(n) - Linear Time:** Runtime grows linearly with input size.
    - Example: Iterating through all elements in a list, finding an item in an unsorted list.
- **O(n log n) - Linearithmic Time:** Common in efficient sorting algorithms.
    - Example: Merge Sort, Heap Sort, Python's sort().
- **O(n²) - Quadratic Time:** Runtime grows with the square of the input size. Often involves nested loops over the input.
    - Example: Bubble sort, selection sort, iterating through all pairs in a list.
- **O(2^n) - Exponential Time:** Runtime doubles with each addition to the input. Very slow for even moderately sized n.
    - Example: Recursive calculation of Fibonacci numbers (naive approach), solving some problems by trying every possible subset.
- **O(n!) - Factorial Time:** Runtime grows factorially. Extremely slow.
    - Example: Traveling Salesperson Problem (brute-force), generating all permutations of a list.

**c) How to do a basic analysis (Rule of Thumb):**

- **Sequence of statements:** Sum of their complexities (take the max).

```python
# O(1) + O(n) = O(n)
print("hello")  # O(1)

for i in range(n):  # O(n)
    print(i)
```
   
- **Loops:** Complexity of statements inside loop * number of iterations.

```python
# Outer loop n times, inner loop n times = O(n * n) = O(n^2)
for i in range(n):
    for j in range(n):
        print(i, j)  # O(1) operation inside
```

- **Conditional statements (if/else):** Worst-case complexity of the branches.

**Why it matters for LeetCode:**

- LeetCode problems have time and memory limits. Understanding Big O helps you choose efficient algorithms and data structures.
- You'll need to analyze your solution's complexity to know if it will pass.
## 9. Basic Recursion

Recursion is a programming technique where a function calls itself to solve a smaller instance of the same problem.

**Key Components of a Recursive Function:**

1. **Base Case(s):**
    - The condition(s) under which the function stops calling itself and returns a value directly.
    - Prevents infinite recursion.
2. **Recursive Step (Recursive Call):**
    - The part of the function where it calls itself with a modified argument, moving closer to the base case.

```python
# Example: Factorial (n!)
# n! = n * (n-1) * (n-2) * ... * 1
# 0! = 1 (by definition)

def factorial_recursive(n):
    # Base Case
    if n == 0 or n == 1:
        return 1
    # Recursive Step
    else:
        return n * factorial_recursive(n - 1)

print(f"5! = {factorial_recursive(5)}")  # Output: 5! = 120

# How it works for factorial_recursive(3):
# factorial_recursive(3) returns 3 * factorial_recursive(2)
#   factorial_recursive(2) returns 2 * factorial_recursive(1)
#     factorial_recursive(1) returns 1 (base case)
#   factorial_recursive(2) returns 2 * 1 = 2
# factorial_recursive(3) returns 3 * 2 = 6


# Example: Fibonacci sequence (less efficient recursively without memoization)
# F(n) = F(n-1) + F(n-2)
# F(0) = 0, F(1) = 1

def fibonacci_recursive(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)

# print(f"Fib(6) = {fibonacci_recursive(6)}")  # Output: Fib(6) = 8
```

**Why it matters for LeetCode:**

- Many tree and graph traversal problems are naturally solved using recursion (DFS).
- Divide and conquer algorithms often use recursion.
- Understanding recursion is key to understanding concepts like backtracking.
- Be mindful of stack overflow errors for deep recursion in Python (Python's default recursion limit can be an issue). Iterative solutions are sometimes preferred for this reason.
## References


