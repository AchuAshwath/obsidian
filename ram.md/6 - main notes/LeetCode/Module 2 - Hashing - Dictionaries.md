07-05-2025 08:53:11

Status : #child 

Tags : [[LeetCode]] [[Hashing]]

# Module 2: Hashing - Dictionaries (`dict`) & Sets (`set`)

**Concept of Hashing:**
Hashing is the process of converting an input item (like a key in a dictionary or an element in a set) into a fixed-size value, typically an integer, called a "hash code" or "hash". This hash code is then used to determine the index or "bucket" where the item (or its associated value) should be stored in an underlying array-like structure (often called a hash table).

**Key Properties for Hashing:**
1.  **Deterministic:** The same input must always produce the same hash code.
2.  **Efficiently Computable:** Calculating the hash should be fast.
3.  **Uniform Distribution (Ideal):** Hash codes should be spread out as evenly as possible across the available buckets to minimize "collisions."
    *   **Collision:** When two different input items produce the same hash code. Hash tables have strategies to resolve collisions (e.g., chaining, open addressing).

In Python, objects that are "hashable" can be used as dictionary keys or set elements.
*   **Hashable Objects:** An object is hashable if it has a hash value that never changes during its lifetime (it needs a `__hash__()` method) and can be compared to other objects (it needs an `__eq__()` method).
*   **Immutable built-in types** like `int`, `float`, `str`, `tuple` (if all its elements are hashable), and `bool` are hashable.
*   **Mutable built-in types** like `list`, `dict`, and `set` are *not* hashable because their contents (and thus their hash value if they had one) could change.

## Hash Map `dict` 

**Concept:**
*   A `dict` (dictionary) in Python is an implementation of a hash map (or hash table).
*   It's an unordered (prior to Python 3.7; since 3.7, insertion order is preserved, but this is an implementation detail and shouldn't be relied upon for algorithmic correctness that requires ordering across different Python versions or contexts unless explicitly stated by the problem).
*   It stores a collection of **key-value pairs**.
*   Keys must be unique and hashable. Values can be of any type and can be duplicated.
*   Optimized for fast lookups, insertions, and deletions of items based on their keys.

> If we are going to append new key : value pairs to dictionaries we should always check for duplicate keys, before blindly trying to insert it.

**Python Implementation:** The built-in `dict` type.

```python
# Creating dictionaries
empty_dict = {}
student_grades = {"Alice": 85, "Bob": 92, "Charlie": 78}
another_dict = dict(name="David", age=30, city="New York") # Using dict() constructor
```

**Core Operations (with Average Time / Worst-Case Time Complexity)**:

The worst-case O(n) complexities occur when there are many hash collisions, forcing the underlying hash table to degrade to something like a linked list search. However, with good hash functions and resizing strategies, Python's dict implementation makes this rare in practice, achieving average O(1).

- **Insert / Update a key-value pair: my_dict[key] = value**
	- Syntax: `my_dict[key] = value`
	- Description: If key is already in the dictionary, its associated value is updated. If key is not present, a new key-value pair is inserted.
	- Time Complexity: Average: O(1) / Worst-Case: O(n)
	- Space Complexity: O(1) (for the operation itself, plus space for key/value if new).

```python
person = {"name": "Alice"}
person["age"] = 30         # Insert
print(person)              # Output: {'name': 'Alice', 'age': 30}
person["name"] = "Alicia"  # Update
print(person)              # Output: {'name': 'Alicia', 'age': 30}
```

- **Access / Find the value for a key: 
	- **my_dict[key]**:
		- Syntax: `value = my_dict[key]`
		- Description: Retrieves the value associated with key. Raises a KeyError if key is not found.
		- Time Complexity: Average: O(1) / Worst-Case: O(n)
		- Space Complexity: O(1)
	- **my_dict.get(key, default=None)**:
		- Syntax: `value = my_dict.get(key, default_value)`
		- Description: Retrieves the value associated with key. If key is not found, returns default_value (which is None if not specified) instead of raising a KeyError.
		- Time Complexity: Average: O(1) / Worst-Case: O(n)
		- Space Complexity: O(1)

```python
grades = {"math": 90, "science": 85}
print(grades["math"])             # Output: 90
# print(grades["history"])        # Raises KeyError

print(grades.get("science"))      # Output: 85
print(grades.get("history"))      # Output: None
print(grades.get("history", "N/A")) # Output: N/A
```

- **Delete a key-value pair:**
	- **del my_dict[key]** :
		- Syntax: `del my_dict[key]`
		- Description: Removes the key-value pair specified by key. Raises a KeyError if key is not found.
		- Time Complexity: Average: O(1) / Worst-Case: O(n)
		- Space Complexity: O(1)
	- **my_dict.pop(key, default=None)**:
		- Syntax: `value = my_dict.pop(key, default_value)`
		- Description: Removes the key-value pair specified by key and returns its associated value. If key is not found, it returns default_value if provided, otherwise raises KeyError.
		- Time Complexity: Average: O(1) / Worst-Case: O(n)
		- Space Complexity: O(1)

```python
config = {"host": "localhost", "port": 8080, "debug": True}
del config["debug"]
print(config)                 # Output: {'host': 'localhost', 'port': 8080}

port_val = config.pop("port")
print(port_val)               # Output: 8080
print(config)                 # Output: {'host': 'localhost'}

# non_existent = config.pop("timeout") # Raises KeyError
non_existent = config.pop("timeout", -1)
print(non_existent)           # Output: -1
```

- **Check if a key has been used (Membership): key in my_dict**
	- Syntax: is_present = key in my_dict
	- Description: Returns True if key is in the dictionary, False otherwise.
	- Time Complexity: Average: O(1) / Worst-Case: O(n)
	- Space Complexity: O(1)

```python
counts = {"apple": 5, "banana": 3}
print("apple" in counts)  # Output: True
print("orange" in counts) # Output: False
print("orange" not in counts) # Output: True
```

- **Get the length (number of key-value pairs): len(my_dict)**
	- Syntax: size = len(my_dict)
	- Time Complexity: O(1)
	- Space Complexity: O(1)

```python
print(len({"a": 1, "b": 2})) # Output: 2
```

- **Loop / Iterate over key-value pairs, keys, or values:**
	- for key in my_dict: (Iterates over keys by default)
	- **my_dict.keys()**: Returns a view object displaying a list of all keys.
	- **my_dict.values()**: Returns a view object displaying a list of all values.
	- **my_dict.items()**: Returns a view object displaying a list of key-value tuple pairs.
	- Time Complexity: O(n) for full iteration, where n is the number of items. Each step of iteration is O(1) on average.
	- Space Complexity: O(1) for iteration itself (view objects are memory-efficient, not full copies).

```python
stats = {"mean": 75.5, "median": 78.0, "mode": 80.0}

print("Keys:")
for k in stats: # same as `for k in stats.keys():`
    print(k)
# Output: mean, median, mode (order preserved from Python 3.7+)

print("\nValues:")
for v in stats.values():
    print(v)
# Output: 75.5, 78.0, 80.0

print("\nItems (key-value pairs):")
for key, value in stats.items():
    print(f"{key}: {value}")
# Output: mean: 75.5, median: 78.0, mode: 80.0
```

- **Search for a value:**
	- Description: There's no direct method to search for a value and get its key efficiently (like my_dict.find_key_by_value(val)). You generally have to iterate.
	- Time Complexity: O(n) (you need to iterate through values or items).
	- Space Complexity: O(1)

```python
ages = {"Alice": 30, "Bob": 25, "Charlie": 30}
target_age = 25
found_key = None
for name, age in ages.items():
    if age == target_age:
        found_key = name
        break
print(f"Person with age {target_age}: {found_key}") # Output: Bob
```

- clear(): Removes all items from the dictionary.
	- Syntax: my_dict.clear()
	- Time Complexity: O(1) on average (doesn't iterate, just resets internal pointers).
	- Space Complexity: O(1)

```python 
# Example for clear()
my_data = {"name": "Gadget", "type": "Electronics", "stock": 75}
print(f"Dictionary before clear(): {my_data}")
print(f"ID of dictionary before clear(): {id(my_data)}")

my_data.clear() # Clears the dictionary in-place

print(f"Dictionary after clear(): {my_data}")
print(f"ID of dictionary after clear(): {id(my_data)}") # Note: The dictionary object itself is the same
```

- **copy(): Returns a shallow copy of the dictionary.** (Refer to Module 0 for shallow vs. deep copy).
	- Syntax: new_dict = my_dict.copy()
	- Time Complexity: O(n)
	- Space Complexity: O(n)

```python
# Example for copy()
original_dict = {
    "id": 101,
    "name": "Alice",
    "hobbies": ["reading", "hiking"],
    "details": {"city": "New York"}
}
print(f"Original dictionary: {original_dict}, ID: {id(original_dict)}")

# Create a shallow copy
copied_dict = original_dict.copy()
print(f"Copied dictionary:   {copied_dict}, ID: {id(copied_dict)}")

# 1. Verify they are different objects
print(f"\nAre original and copied the same object? {original_dict is copied_dict}") # Output: False

# 2. Modifying an immutable value in the copy
copied_dict["id"] = 102
copied_dict["name"] = "Alicia" # Strings are immutable, so this assigns a new string
print(f"\nAfter modifying immutable value ('id', 'name') in copy:")
print(f"Original: {original_dict}")
print(f"Copied:   {copied_dict}")
# Original is unaffected because 'id' (int) and 'name' (str) are immutable.
# When 'copied_dict["id"] = 102' happens, 'copied_dict' points 'id' to a new integer object.

# 3. Modifying a mutable value (list) *inside* the copied dictionary
# Since it's a shallow copy, 'hobbies' list is shared
copied_dict["hobbies"].append("coding")
print(f"\nAfter appending to 'hobbies' list via copied_dict:")
print(f"Original: {original_dict}")
print(f"Copied:   {copied_dict}")
# Both dictionaries reflect the change because they share the same list object for 'hobbies'.
print(f"ID of original_dict['hobbies']: {id(original_dict['hobbies'])}")
print(f"ID of copied_dict['hobbies']:   {id(copied_dict['hobbies'])}") # Will be the same ID

# 4. Modifying a mutable value (dict) *inside* the original dictionary
original_dict["details"]["zip"] = "10001"
print(f"\nAfter adding 'zip' to 'details' dict via original_dict:")
print(f"Original: {original_dict}")
print(f"Copied:   {copied_dict}")
# Both dictionaries reflect the change because they share the same dict object for 'details'.
print(f"ID of original_dict['details']: {id(original_dict['details'])}")
print(f"ID of copied_dict['details']:   {id(copied_dict['details'])}") # Will be the same ID
```

- **Specialized Dictionary Types from collections module (Very useful for LeetCode!):**
	- **collections.defaultdict**:
		- A subclass of dict that calls a factory function to supply missing values. If you try to access a key that doesn't exist, it automatically creates that key with a default value provided by the factory function (e.g., int -> 0, list -> [], set -> set()
  
```python
from collections import defaultdict

# Counting frequency of characters
s = "abracadabra"
char_counts = defaultdict(int) # Default value for a new key will be int(), which is 0
for char in s:
		char_counts[char] += 1
print(char_counts)
# Output: defaultdict(<class 'int'>, {'a': 5, 'b': 2, 'r': 2, 'c': 1, 'd': 1})
print(char_counts['z']) # Accessing a missing key
print(char_counts)      # 'z' is now in char_counts with value 0

# Grouping items
pairs = [('a', 1), ('b', 2), ('a', 3), ('c', 4), ('b', 5)]
grouped = defaultdict(list) # Default value for a new key will be list(), which is []
for key, value in pairs:
		grouped[key].append(value)
print(grouped)
# Output: defaultdict(<class 'list'>, {'a': [1, 3], 'b': [2, 5], 'c': [4]})
```

- **collections.Counter**:
	- A dict subclass for counting hashable objects. Elements are stored as dictionary keys and their counts are stored as dictionary values.

```python
from collections import Counter

s = "mississippi"
counts = Counter(s)
print(counts)
# Output: Counter({'i': 4, 's': 4, 'p': 2, 'm': 1})
print(counts['s']) # Output: 4
print(counts['z']) # Output: 0 (doesn't add 'z' to Counter if it's not there)

words = ["apple", "banana", "apple", "orange", "banana", "apple"]
word_counts = Counter(words)
print(word_counts)
# Output: Counter({'apple': 3, 'banana': 2, 'orange': 1})

# Get most common elements
print(word_counts.most_common(2)) # Output: [('apple', 3), ('banana', 2)]

# Counter objects also support arithmetic operations
c1 = Counter(a=3, b=1)
c2 = Counter(a=1, b=2)
print(c1 + c2) # Counter({'a': 4, 'b': 3})
print(c1 - c2) # Counter({'a': 2}) (keeps only positive counts)
```

- **Key LeetCode Use Cases for dict:**
	- Frequency Counting: Extremely common (e.g., count character occurrences, number occurrences). Counter is perfect for this.
	- Mapping: Storing associations between items (e.g., mapping a node to its neighbors in a graph adjacency list, mapping values to their indices).
	- Caching/Memoization: In dynamic programming or recursive solutions, store results of subproblems to avoid re-computation.
	- Checking for Duplicates: Iterate through a list and use a dictionary (or set) to track seen elements.
	- Problems involving "Two Sum" and its variations often use dictionaries for O(n) solutions.

- **Pythonic Tips & Common Pitfalls for dict:**
	- Use my_dict.get(key, default_val) to safely access keys that might not exist, preventing KeyError.
	- collections.defaultdict is your friend for simplifying code where you need default values for new keys (e.g., building frequency maps, adjacency lists).
	- collections.Counter is highly optimized for counting tasks.
	- Remember keys must be hashable. You cannot use a list as a key directly. If you need to, convert the list to a tuple (if its elements are hashable): my_dict[tuple(my_list_key)] = value.
	- While Python 3.7+ preserves insertion order, don't rely on this if the problem's logic requires specific ordering unless that ordering is explicitly guaranteed by problem constraints or you are using collections.OrderedDict (though OrderedDict is less critical now that standard dict maintains order).


## References


