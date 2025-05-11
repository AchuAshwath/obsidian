09-05-2025 07:45:35

Status : #child 

Tags : [[LeetCode]] 

# Sets

**Concept:**
- An unordered collection of unique, hashable items.
- Similar to the mathematical concept of a set.
- Optimized for fast membership testing (in operator), insertion, and deletion.
- Also provides standard set operations like union, intersection, difference.

**Python Implementation**: The built-in set type.

```python
# Creating sets
empty_set = set() # Note: {} creates an empty dictionary, not an empty set
fruits = {"apple", "banana", "cherry"} # Using curly braces with elements
numbers = set([1, 2, 2, 3, 4, 4, 4]) # From a list, duplicates are removed
print(numbers) # Output: {1, 2, 3, 4} (order may vary)
```

- **Core Operations (Average Time / Worst-Case Time Complexity)**:
	
	Similar to dictionaries, sets rely on hash tables internally, so average time complexities are O(1), but worst-case (due to hash collisions) can be O(n).
	
	- **Add an item: my_set.add(item)**
		- Syntax: my_set.add(item)
		- Description: Adds item to the set. If item is already present, the set remains unchanged (as sets only store unique items).
		- Time Complexity: Average: O(1) / Worst-Case: O(n)
		- Space Complexity: O(1) (plus space for the item if new).

```python
colors = {"red", "green"}
colors.add("blue")
print(colors)         # Output: {'red', 'green', 'blue'} (order may vary)
colors.add("red")     # Adding an existing item
print(colors)         # Output: {'red', 'green', 'blue'}
```

- **Remove an item:**
	- **my_set.remove(item):**
		- Syntax: my_set.remove(item)
		- Description: Removes item from the set. Raises a KeyError if item is not found.
		- Time Complexity: Average: O(1) / Worst-Case: O(n)
		- Space Complexity: O(1)
	- **my_set.discard(item):**
		- Syntax: my_set.discard(item)
		- Description: Removes item from the set if it is present. Does not raise an error if item is not found.
		- Time Complexity: Average: O(1) / Worst-Case: O(n)
		- Space Complexity: O(1)
	- **my_set.pop():**
		- Syntax: removed_item = my_set.pop()
		- Description: Removes and returns an arbitrary item from the set. Raises KeyError if the set is empty. (Useful if you just need to get an element out and don't care which one).
		- Time Complexity: Average: O(1) / Worst-Case: O(n)

```python
permissions = {"read", "write", "execute"}
permissions.remove("execute")
print(permissions) # Output: {'read', 'write'} (order may vary)
# permissions.remove("admin") # Raises KeyError

permissions.discard("write")
print(permissions) # Output: {'read'}
permissions.discard("admin") # No error
print(permissions) # Output: {'read'}

if permissions: # check if set is not empty
  item = permissions.pop()
  print(f"Popped: {item}, Remaining: {permissions}") # Example: Popped: read, Remaining: set()
```

- **Check if an item exists (Membership): item in my_set**
	- Syntax: is_present = item in my_set
	- Description: Returns True if item is in the set, False otherwise. This is a primary strength of sets.
	- Time Complexity: Average: O(1) / Worst-Case: O(n)
	- Space Complexity: O(1)

```python
visited_nodes = {10, 20, 30}
print(20 in visited_nodes)    # Output: True
print(40 in visited_nodes)    # Output: False
```

- **Get the length (number of unique items): len(my_set)**
	- Syntax: size = len(my_set)
	- Time Complexity: O(1)
	- Space Complexity: O(1)

```python
print(len({"a", "b", "c"})) # Output: 3
```


- **Loop / Iterate over items: for item in my_set:**
	- Description: Iterates through each unique item in the set. The order of iteration is arbitrary.
	- Time Complexity: O(n) for full iteration.
	- Space Complexity: O(1).

```python
for fruit in {"apple", "banana", "cherry"}:
    print(fruit) # Order not guaranteed
```

- **Set Operations:**
	- Union: set1 | set2 or set1.union(set2, ...)
        - Returns a new set containing all items from both sets.
        - Time: O(len(s1) + len(s2))
    - Intersection: set1 & set2 or set1.intersection(set2, ...)
        - Returns a new set containing only items common to both sets.
        - Time: O(min(len(s1), len(s2))) on average (iterates through smaller set, checks membership in larger).
    - Difference: set1 - set2 or set1.difference(set2, ...)
        - Returns a new set containing items from set1 that are not in set2.
        - Time: O(len(s1)) on average (iterates through s1, checks membership in s2).
    - Symmetric Difference: set1 ^ set2 or set1.symmetric_difference(set2)
        - Returns a new set containing items in either set1 or set2 but not both.
        - Time: O(len(s1) + len(s2))

```python
s1 = {1, 2, 3, 4}
s2 = {3, 4, 5, 6}

print(f"Union: {s1 | s2}")                 # Output: {1, 2, 3, 4, 5, 6}
print(f"Intersection: {s1 & s2}")          # Output: {3, 4}
print(f"Difference (s1-s2): {s1 - s2}")    # Output: {1, 2}
print(f"Difference (s2-s1): {s2 - s1}")    # Output: {5, 6}
print(f"Symmetric Diff: {s1 ^ s2}")        # Output: {1, 2, 5, 6}
```

> There are also in-place update versions: |= (update), &= (intersection_update), -= (difference_update), ^= (symmetric_difference_update).

- Subset/Superset Checks:
	- set1.issubset(set2) or set1 <= set2: Is set1 a subset of set2?
	- set1.issuperset(set2) or set1 >= set2: Is set1 a superset of set2?
	- set1 < set2: Proper subset. set1 > set2: Proper superset.
	- Time Complexity: Generally O(len(set1)) for issubset (iterates through set1 checking membership in set2).

```python
# Define some sets for demonstration
set_a = {1, 2, 3}
set_b = {1, 2, 3, 4, 5}
set_c = {1, 2}
set_d = {3, 2, 1} # Same as set_a, but different order for definition
set_e = {6, 7}
set_f = {1, 2, 3, 4, 5} # Same as set_b

print("Set A:", set_a)
print("Set B:", set_b)
print("Set C:", set_c)
print("Set D:", set_d)
print("Set E:", set_e)
print("Set F:", set_f)
print("-" * 30)

# 1. issubset() or <=
print("\n--- issubset() or <= ---")
# Is set_a a subset of set_b? (Are all elements of set_a in set_b?)
print(f"set_a.issubset(set_b): {set_a.issubset(set_b)}") # Output: True
print(f"set_a <= set_b: {set_a <= set_b}")             # Output: True

# Is set_c a subset of set_a?
print(f"set_c.issubset(set_a): {set_c.issubset(set_a)}") # Output: True
print(f"set_c <= set_a: {set_c <= set_a}")             # Output: True

# Is set_a a subset of set_d? (Equality also means subset)
print(f"set_a.issubset(set_d): {set_a.issubset(set_d)}") # Output: True
print(f"set_a <= set_d: {set_a <= set_d}")             # Output: True

# Is set_a a subset of set_e?
print(f"set_a.issubset(set_e): {set_a.issubset(set_e)}") # Output: False
print(f"set_a <= set_e: {set_a <= set_e}")             # Output: False

# Is set_b a subset of set_a?
print(f"set_b.issubset(set_a): {set_b.issubset(set_a)}") # Output: False
print(f"set_b <= set_a: {set_b <= set_a}")             # Output: False

print("-" * 30)

# 2. issuperset() or >=
print("\n--- issuperset() or >= ---")
# Is set_b a superset of set_a? (Does set_b contain all elements of set_a?)
print(f"set_b.issuperset(set_a): {set_b.issuperset(set_a)}") # Output: True
print(f"set_b >= set_a: {set_b >= set_a}")             # Output: True

# Is set_a a superset of set_c?
print(f"set_a.issuperset(set_c): {set_a.issuperset(set_c)}") # Output: True
print(f"set_a >= set_c: {set_a >= set_c}")             # Output: True

# Is set_a a superset of set_d? (Equality also means superset)
print(f"set_a.issuperset(set_d): {set_a.issuperset(set_d)}") # Output: True
print(f"set_a >= set_d: {set_a >= set_d}")             # Output: True

# Is set_e a superset of set_a?
print(f"set_e.issuperset(set_a): {set_e.issuperset(set_a)}") # Output: False
print(f"set_e >= set_a: {set_e >= set_a}")             # Output: False

# Is set_a a superset of set_b?
print(f"set_a.issuperset(set_b): {set_a.issuperset(set_b)}") # Output: False
print(f"set_a >= set_b: {set_a >= set_b}")             # Output: False
print("-" * 30)

# 3. < (Proper subset)
# set1 < set2 means set1 is a subset of set2 AND set1 != set2
print("\n--- < (Proper subset) ---")
# Is set_a a proper subset of set_b?
print(f"set_a < set_b: {set_a < set_b}") # Output: True (set_a is subset, and set_b has more elements)

# Is set_c a proper subset of set_a?
print(f"set_c < set_a: {set_c < set_a}") # Output: True (set_c is subset, and set_a has more elements)

# Is set_a a proper subset of set_d? (set_a and set_d are equal)
print(f"set_a < set_d: {set_a < set_d}") # Output: False (they are equal, so not a *proper* subset)

# Is set_b a proper subset of set_f? (set_b and set_f are equal)
print(f"set_b < set_f: {set_b < set_f}") # Output: False (they are equal)

# Is set_b a proper subset of set_a?
print(f"set_b < set_a: {set_b < set_a}") # Output: False (set_b is not even a subset of set_a)
print("-" * 30)

# 4. > (Proper superset)
# set1 > set2 means set1 is a superset of set2 AND set1 != set2
print("\n--- > (Proper superset) ---")
# Is set_b a proper superset of set_a?
print(f"set_b > set_a: {set_b > set_a}") # Output: True (set_b is superset, and set_b has more elements)

# Is set_a a proper superset of set_c?
print(f"set_a > set_c: {set_a > set_c}") # Output: True (set_a is superset, and set_a has more elements)

# Is set_a a proper superset of set_d? (set_a and set_d are equal)
print(f"set_a > set_d: {set_a > set_d}") # Output: False (they are equal, so not a *proper* superset)

# Is set_b a proper superset of set_f? (set_b and set_f are equal)
print(f"set_b > set_f: {set_b > set_f}") # Output: False (they are equal)

# Is set_a a proper superset of set_b?
print(f"set_a > set_b: {set_a > set_b}") # Output: False (set_a is not even a superset of set_b)
print("-" * 30)

# Time Complexity Reminder:
# For s1.issubset(s2) or s1 <= s2:
# The check iterates through elements of s1 and for each element,
# checks if it's present in s2. Hash lookups in s2 are O(1) on average.
# So, overall complexity is generally O(len(s1)).
# The same logic applies to s1.issuperset(s2) or s1 >= s2, but it's O(len(s2)).
# For < and >, it's effectively the same as <= or >= plus a length check.
```

**Key LeetCode Use Cases for set:**
- Tracking Visited Elements: Essential in graph traversals (DFS/BFS) or any algorithm where you need to avoid reprocessing items (e.g., finding cycles, exploring paths).
- Finding Unique Elements / Removing Duplicates: unique_list = list(set(original_list)).
- Fast Membership Testing: When you frequently need to check if an item has been seen before or exists in a collection.
- Problems involving finding common elements or differences between collections.
- Checking for missing numbers in a range.

**Pythonic Tips & Common Pitfalls for set:**
- Use set() to create an empty set. {} creates an empty dictionary.
- Items in a set must be hashable (e.g., list cannot be an element of a set directly; use tuple(my_list) if its contents are hashable).
- my_set.remove(item) will raise a KeyError if the item is not present; my_set.discard(item) will not. Choose based on whether a missing item is an exceptional condition or expected.
- Sets are unordered. If you need to preserve order while ensuring uniqueness, you might need a combination of data structures or a more complex approach (e.g., iterate through a list, add to a set to check for uniqueness, and if unique, add to a new result list).

Dictionaries and sets are workhorses in LeetCode due to their average O(1) performance for key operations. Mastering their usage, including the specialized types from collections, will significantly boost your problem-solving capabilities

## References


