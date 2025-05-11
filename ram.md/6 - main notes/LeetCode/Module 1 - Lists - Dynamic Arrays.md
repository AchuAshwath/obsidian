07-05-2025 08:50:05

Status : #child 

Tags : [[LeetCode]] [[Arrays]] 

This module dives into Python's built-in `list` type, which functions as a dynamic array, and the `str` type for strings. We'll cover their core operations, performance characteristics, and common use cases in LeetCode.
# Lists

**Concept:**
- An ordered, mutable (changeable) sequence of items.
- Items can be of different data types (heterogeneous).
- Implemented as a dynamic array in Python, meaning it can grow or shrink in size as needed. While it provides array-like indexed access, its size is not fixed at creation.

**Python Implementation:** The built-in `list` type.

```python
my_list = [1, "hello", 3.14, True, [10, 20]]
empty_list = []
another_list = list(range(5)) # [0, 1, 2, 3, 4]
```

**Core Operations (with Time/Space Complexity):**

- **Access an item by index:** my_list[i]
    - Syntax: element = my_list[index]
    - Description: Retrieves the element at the specified zero-based index. Negative indexing is allowed (-1 is the last element).
    - Time Complexity: **O(1)** (Constant time) - Direct memory access.
    - Space Complexity: O(1)

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[0])    # Output: 10
print(numbers[2])    # Output: 30
print(numbers[-1])   # Output: 50
```   

- **Update an item by index:** my_list[i] = new_value
    - Syntax: my_list[index] = new_value
    - Description: Changes the element at the specified index to new_value.
    - Time Complexity: **O(1)**
    - Space Complexity: O(1)

```python
numbers = [10, 20, 30]
numbers[1] = 200
print(numbers)  # Output: [10, 200, 30]
```

- **Append an item to the end:** my_list.append(item)
    - Syntax: my_list.append(item)
    - Description: Adds item to the very end of the list.
    - Time Complexity: **O(1) amortized**.
        - Amortized Explanation: Most of the time, it's O(1) because Python lists often have extra allocated space. When that space runs out, the list needs to be resized (a new, larger block of memory is allocated, and all existing elements are copied over), which is an O(k) operation where k is the current size. However, these resizes happen infrequently enough that the average cost over many appends is O(1).
    - Space Complexity: O(1) for the operation itself (plus space for the new item).
   
```python
letters = ['a', 'b']
letters.append('c')
print(letters)  # Output: ['a', 'b', 'c']
```
   
-  **Insert an item at a specific index:** my_list.insert(index, item)
    - Syntax: my_list.insert(index, item)
    - Description: Inserts item at the given index, shifting all subsequent elements to the right.
    - Time Complexity: **O(n)**, where n is the number of elements in the list. In the worst case (inserting at index 0), all elements need to be shifted.
    - Space Complexity: O(1) (or O(n) if a resize is triggered, but typically focused on element shifting cost).
   
```python
letters = ['a', 'c', 'd']
letters.insert(1, 'b')  # Insert 'b' at index 1
print(letters)  # Output: ['a', 'b', 'c', 'd']

letters.insert(0, 'Z')  # Insert at the beginning
print(letters)  # Output: ['Z', 'a', 'b', 'c', 'd']
```
   
- **Remove an item from the end (Pop last):** my_list.pop()
    - Syntax: removed_item = my_list.pop()
    - Description: Removes and returns the last item from the list.
    - Time Complexity: **O(1) amortized** (similar reasoning to append).
    - Space Complexity: O(1)

```python
stack = [1, 2, 3, 4]
last_item = stack.pop()
print(last_item)  # Output: 4
print(stack)       # Output: [1, 2, 3]
```

- **Remove an item at a specific index (Pop intermediate/first):** my_list.pop(index)
    - Syntax: removed_item = my_list.pop(index)
    - Description: Removes and returns the item at the given index. Subsequent items are shifted left.
    - Time Complexity: **O(n)**, where n is the number of elements. Worst case is pop(0).
    - Space Complexity: O(1)
    
```python
queue_like = ['a', 'b', 'c', 'd']
first_item = queue_like.pop(0)  # Inefficient for queue behavior
print(first_item)  # Output: 'a'
print(queue_like)   # Output: ['b', 'c', 'd']

item_at_1 = queue_like.pop(1)
print(item_at_1)    # Output: 'c'
print(queue_like)   # Output: ['b', 'd']
```
    
-  **Remove the first occurrence of an item by value:** my_list.remove(value)
    - Syntax: my_list.remove(value)
    - Description: Removes the first item from the list whose value is equal to value. Raises a ValueError if value is not present.
    - Time Complexity: **O(n)** (it has to search for the item first, then potentially shift elements).
    - Space Complexity: O(1)

```python
data = [10, 20, 30, 20, 40]
data.remove(20)  # Removes the first 20
print(data)      # Output: [10, 30, 20, 40]

try:
  data.remove(100)  # Would raise ValueError
except ValueError:
  print("Value was not found in the array")
```
   
 > **del my_list[index]**: Can also remove an item (or slice) by index. del my_list[i] is O(n) for intermediate, O(1) for last if no resize. del my_list[i:j] is O(n).

- **Find an item (check membership):** value in my_list
    - Syntax: is_present = value in my_list
    - Description: Returns True if value is found in the list, False otherwise.
    - Time Complexity: **O(n)** (linear search).
    - Space Complexity: O(1)
        
```python
numbers = [1, 2, 3, 4, 5]
print(3 in numbers)     # Output: True
print(10 in numbers)    # Output: False
```  
   
- **Find the index of the first occurrence of an item:** my_list.index(value, start, end)
    - Syntax: idx = my_list.index(value)
    - Description: Returns the zero-based index in the list of the first item whose value is equal to value. Raises a ValueError if value is not present. Optional start and end arguments can limit the search to a sub-section of the list.
    - Time Complexity: **O(n)** (linear search).
    - Space Complexity: O(1)
    
```python
numbers = [10, 20, 30, 20, 40]
print(numbers.index(30))  # Output: 2
print(numbers.index(20))  # Output: 1 (index of the first 20)

try:
  print(numbers.index(10, 1, 3))
except ValueError:
  print("Value was not found in the array")

# print(numbers.index(100))  # Would raise ValueError
```

- **Get the length of the list:** len(my_list)
    - Syntax: length = len(my_list)
    - Description: Returns the number of items in the list.
    - Time Complexity: **O(1)** (the list object keeps track of its size).
    - Space Complexity: O(1)

```python
print(len([1, 2, 3]))  # Output: 3
print(len([]))         # Output: 0
```

- **Slicing (Copy part of an array or create sublists):** my_list[start:end:step]
    - Syntax: sub_list = my_list[start:end:step]
        - start: starting index (inclusive, defaults to 0).
        - end: ending index (exclusive, defaults to length of list).
        - step: step value (defaults to 1).
    - Description: Creates a new list containing a portion of the original list.
    - Time Complexity: **O(k)**, where k is the number of elements in the slice.
    - Space Complexity: **O(k)** (to store the new slice).

```python
numbers = [0, 1, 2, 3, 4, 5, 6]

print(numbers[1:4])   # Output: [1, 2, 3] (elements at index 1, 2, 3)
print(numbers[:3])    # Output: [0, 1, 2] (from beginning up to index 3 (exclusive))
print(numbers[3:])    # Output: [3, 4, 5, 6] (from index 3 to end)
print(numbers[::2])   # Output: [0, 2, 4, 6] (every second element)
print(numbers[::-1])  # Output: [6, 5, 4, 3, 2, 1, 0] (reverses the list - common trick)
```

- **Copy an array (shallow copy):**
    - Syntax:
        - new_list = my_list.copy()
        - new_list = list(my_list)
        - new_list = my_list[:] (slicing the whole list)
    - Description: Creates a shallow copy of the list.
    - Time Complexity: **O(n)**, where n is the number of elements.
    - Space Complexity: **O(n)** (for the new list).
    
```python
original = [1, 2, [3, 4]]
copied_slice = original[:]        # Creates a shallow copy of the list
copied_copy_method = original.copy()  # Another shallow copy method

copied_slice.append(5)
copied_slice[2].append(50)  # Modifies inner list in original too (shallow copy)

print(f"Original: {original}")  # Output: Original: [1, 2, [3, 4, 50]]
print(f"Copied Slice: {copied_slice}")  # Output: Copied Slice: [1, 2, [3, 4, 50], 5]
```

- **Sort an array:**
    - my_list.sort(key=None, reverse=False): In-place sort.
        - Description: Modifies the list itself. Returns None.
        - Time Complexity: **O(n log n)** (uses Timsort algorithm).
        - Space Complexity: **O(log n)** or **O(n)** depending on data (Timsort can use O(n) space in some cases, O(log n) typically for random data).
    - new_list = sorted(iterable, key=None, reverse=False): Returns a new sorted list.
        - Description: Creates and returns a new list, leaving the original iterable unchanged.
        - Time Complexity: **O(n log n)**.
        - Space Complexity: **O(n)** (for the new list).

```python
numbers = [3, 1, 4, 1, 5, 9, 2]

# Creates a new sorted list
sorted_numbers = sorted(numbers)
print(f"Original numbers: {numbers}")  # Output: [3, 1, 4, 1, 5, 9, 2]
print(f"Sorted numbers: {sorted_numbers}")  # Output: [1, 1, 2, 3, 4, 5, 9]

# Sorts in-place
numbers.sort()
print(f"Numbers sorted in-place: {numbers}")  # Output: [1, 1, 2, 3, 4, 5, 9]

# Sorts in descending order
numbers.sort(reverse=True)
print(f"Numbers sorted descending: {numbers}")  # Output: [9, 5, 4, 3, 2, 1, 1]
```
    
- **Reverse an array:**
    - my_list.reverse(): In-place reversal.
        - Description: Modifies the list itself. Returns None.
        - Time Complexity: **O(n)**.
        - Space Complexity: **O(1)**.
    - Slicing [::-1]: Returns a new reversed list.
        - Description: Creates and returns a new list that is the reverse of the original.
        - Time Complexity: **O(n)**.
        - Space Complexity: **O(n)**.
            
```python
data = [1, 2, 3, 4]

# Creates a new reversed list using slicing
reversed_data_new = data[::-1]
print(f"Original data: {data}")              # Output: [1, 2, 3, 4]
print(f"New reversed list: {reversed_data_new}") # Output: [4, 3, 2, 1]

# Reverses the list in-place
data.reverse()
print(f"Data reversed in-place: {data}")     # Output: [4, 3, 2, 1]
```
    
- **Concatenation:** list1 + list2
    - Syntax: combined_list = list1 + list2
    - Description: Creates a new list by appending all items from list2 to list1.
    - Time Complexity: **O(n + m)**, where n and m are lengths of list1 and list2.
    - Space Complexity: **O(n + m)** (for the new list).
    - my_list.extend(iterable): Appends all items from an iterable to my_list (in-place). More efficient than repeated + or append in a loop if you have many items to add from another iterable. Time: O(k) where k is length of iterable.
    
```python
l1 = [1, 2]
l2 = [3, 4]

# Concatenates the two lists and creates a new list
l3 = l1 + l2
print(l3)  # Output: [1, 2, 3, 4]

# Extends l1 by appending elements of l2 to it in-place
l1.extend(l2)
print(l1)  # Output: [1, 2, 3, 4]
```
   
- **Iteration (Loop over array):** for item in my_list:
    - Syntax: for item in my_list: # do something with item
    - Description: Iterates through each item in the list.
    - Time Complexity: **O(n)**.
    - Space Complexity: O(1) (for the loop itself).
    
```python
for num in [10, 20, 30]:
    print(num)
```
    
- **Swap two items:**
    - Syntax: my_list[i], my_list[j] = my_list[j], my_list[i]
    - Description: Pythonic way to swap two elements in a list using tuple packing/unpacking.
    - Time Complexity: **O(1)**
    - Space Complexity: O(1)
        
```python
items = ['A', 'B', 'C', 'D']

# Swap elements at index 0 and 2
items[0], items[2] = items[2], items[0]

print(items)  # Output: ['C', 'B', 'A', 'D']
```

- **Filter an array (using List Comprehension):**
    - Syntax: filtered_list = [item for item in my_list if condition(item)]
    - Description: Creates a new list containing only items that satisfy the condition.
    - Time Complexity: **O(n)** (iterates through the list once).
    - Space Complexity: **O(k)** where k is the number of items satisfying the condition (for the new list).
    
```python
numbers = [1, 2, 3, 4, 5, 6]

# List comprehension to filter even numbers
even_numbers = [num for num in numbers if num % 2 == 0]

print(even_numbers)  # Output: [2, 4, 6]
```

**Key LeetCode Use Cases for list:**

- Storing sequences of data where order matters.
- Implementing other data structures like stacks (using append and pop).
- Two-pointer techniques (e.g., left, right pointers moving through a list).
- Sliding window problems.
- Dynamic Programming (often storing intermediate results in a list/array).
- Representing grids or matrices (list of lists).

**Pythonic Tips & Common Pitfalls for list:**

- **Be mindful of O(n) operations in loops:** Operations like list.insert(0, val), list.pop(0), val in list, list.remove(val) are O(n). If you perform these repeatedly inside another loop, your complexity can quickly become O(n^2) or worse.
- **Shallow vs. Deep Copy:** If your list contains mutable objects (like other lists), understand when you need copy.deepcopy() versus a shallow copy (.copy() or [:]).
- **List comprehensions** are often more readable and efficient than manual for loops for creating or transforming lists.
- When initializing a list of lists (e.g., a 2D grid), be careful:
    - **Incorrect:** grid = [[]] * rows (This creates rows references to the same inner list object!)
    - **Correct:** grid = [[] for _ in range(rows)] (This creates distinct inner lists)
    - **Correct for fixed value:** grid = [[0 for _ in range(cols)] for _ in range(rows)]

## References


