03-04-2025 18:30:42

Status : #child 

Tags : [[LeetCode]]

# Pre-requisite for LeetCode

This document details the pre-requisite knowledge for tackling Data Structures and Algorithms (DSA) problems on LeetCode using Python. It focuses on Python's built-in data structures, relevant standard library modules, their operations, complexities, and common LeetCode use cases, drawing inspiration from effective learning roadmaps like NeetCode and AlgoMap.io.

---

# Module 0: Python Essentials for DSA & LeetCode

This module covers foundational Python knowledge critical for writing clean, efficient, and correct DSA code.

## 1. Variables & Data Types (Brief Review)
*(No significant changes from previous version, basics are covered)*
*   `int`, `float`, `str`, `bool`.
*   **Addition:** Python integers have arbitrary precision, meaning they can grow as large as memory allows. You generally don't need to worry about integer overflow like in C++/Java for standard integer types. This is a significant advantage for certain problems involving large numbers.

**a) What it means:** *(as before)*
**b) Common Complexities (from best to worst):** *(as before)*
**c) How to do a basic analysis (Rule of Thumb):** *(as before)*

**d) Big O in the Context of LeetCode Constraints:**
LeetCode problems usually have time limits (e.g., 1-2 seconds) and memory limits. The maximum input size (`N`) often dictates the acceptable Big O complexity:
*   **`N` up to ~10<sup>6</sup> - 10<sup>7</sup>:** Your solution likely needs to be **O(N)** or **O(N log N)**. Sometimes O(N * small_constant) might pass.
*   **`N` up to ~10<sup>5</sup> - 10<sup>6</sup>:** **O(N log N)** is often fine, O(N) is better.
*   **`N` up to ~2000 - 5000:** **O(N²)** might be acceptable.
*   **`N` up to ~500 - 1000:** **O(N³) ** might pass, but it's pushing it.
*   **`N` up to ~20 - 25:** **O(2<sup>N</sup>)** or **O(N * 2<sup>N</sup>)** (often from backtracking/recursion with exponential branches) might be acceptable.
*   **`N` up to ~10 - 12:** **O(N!)** or **O(N² * 2<sup>N</sup>)** (e.g., permutations, some complex bitmask DP) might pass.
*   **`O(log N)` or `O(1)`** solutions are almost always fast enough.

Always consider the worst-case complexity. Understanding these general guidelines helps you quickly assess if a potential approach is viable before coding it.

## 9. Basic Recursion
*(No significant changes, concept well covered)*

---

# Module 1: Lists (Dynamic Arrays) & Strings

This module dives into Python's built-in `list` type and the `str` type.

## A) `list` (Dynamic Array)

*(Previous content on core operations and complexities is good. Enhancing "Key LeetCode Use Cases".)*

**Key LeetCode Use Cases for `list`:**
*   Storing sequences of data where order matters.
*   Implementing other data structures like stacks (using `append` and `pop`).
*   **Two-Pointer Technique:** A very common algorithmic pattern using lists (or arrays/strings).
    *   **Opposite Ends:** Pointers start at `left=0` and `right=len(list)-1` and move towards each other (e.g., checking for palindromes, finding pairs that sum to a target in a *sorted* list).
    *   **Same Direction (Fast/Slow or Fixed Gap):** Both pointers start at or near the beginning. One might move faster than the other, or they maintain a fixed-size "window" between them. (e.g., detecting cycles in linked lists (adapted here), finding longest substring without repeating characters).
*   **Sliding Window Technique:** Another common pattern where a "window" of a certain size (fixed or variable) slides over the list/array. Often used with dictionaries or sets to track contents within the window efficiently. (e.g., finding max sum subarray of size k, min window substring).
*   Dynamic Programming (often storing intermediate results in a 1D or 2D list/array).
*   Representing grids or matrices (list of lists).

*(Other list operations and Pythonic Tips remain as before)*

## B) `str` (Strings)

*(Previous content is comprehensive. Highlighting pattern connections.)*

**Key LeetCode Use Cases for `str`:**
*   String manipulation problems (parsing, formatting, validating).
*   Palindrome checks (often uses **Two-Pointer Technique**).
*   Anagram checks (often combined with hashmaps/`Counter` or sorting).
*   Substring search (can involve algorithms like KMP, but often simpler methods or built-ins are sufficient for typical LC).
*   Longest common prefix/substring problems.
*   Many string problems can also be solved using **Sliding Window** or **Dynamic Programming**.


---

# Module 3: Stacks (LIFO) & Queues (FIFO)
*(No significant changes from previous version, `deque` emphasis is good)*
*   **Monotonic Stack:** Already mentioned as a use case for Stacks. This is a specific and powerful pattern that comes up in problems like "Next Greater Element," "Largest Rectangle in Histogram," "Sum of Subarray Minimums." Recognizing when a monotonic stack can be applied is key.

---

# Module 6: Trees (Conceptual & Basic Traversal)

*(Previous content on BT, BST, and traversals is good. Adding Trie and reinforcing visualization.)*

**Types of Trees (Common in LeetCode):**
*   Binary Tree (BT)
*   Binary Search Tree (BST)
*   N-ary Tree
*   *(Other types as before)*

**Specialized Tree Type: Trie (Prefix Tree)**
*   **Concept:** A tree-like data structure that stores a dynamic set of strings, typically used for efficient prefix searches. Each node usually represents a character, and paths from the root to a node represent a prefix. A special marker in a node (e.g., `isEndOfWord` boolean) can indicate that the path to this node forms a complete word.
*   **Python Implementation:**
    *   Custom `TrieNode` class.
    *   Each `TrieNode` often contains:
        *   `children`: A dictionary mapping characters to child `TrieNode`s (e.g., `self.children = {}` or `self.children = defaultdict(TrieNode)`).
        *   `isEndOfWord`: A boolean flag, `False` by default.
    ```python
    # Example TrieNode structure
    # class TrieNode:
    #     def __init__(self):
    #         self.children = {} # char -> TrieNode
    #         self.isEndOfWord = False

    # class Trie:
    #     def __init__(self):
    #         self.root = TrieNode()

    #     def insert(self, word: str) -> None:
    #         curr = self.root
    #         for char in word:
    #             if char not in curr.children:
    #                 curr.children[char] = TrieNode()
    #             curr = curr.children[char]
    #         curr.isEndOfWord = True

    #     def search(self, word: str) -> bool:
    #         curr = self.root
    #         for char in word:
    #             if char not in curr.children:
    #                 return False
    #             curr = curr.children[char]
    #         return curr.isEndOfWord

    #     def startsWith(self, prefix: str) -> bool:
    #         curr = self.root
    #         for char in prefix:
    #             if char not in curr.children:
    #                 return False
    #             curr = curr.children[char]
    #         return True
    ```
*   **Key LeetCode Use Cases:** Autocomplete systems, spell checkers, dictionary lookups, word search in a grid (if words are from a dictionary), problems involving matching string prefixes. (e.g., LeetCode #208 Implement Trie, #211 Design Add and Search Words Data Structure, #677 Map Sum Pairs).
*   **Time Complexity:**
    *   Insert word of length `L`: O(L)
    *   Search for word of length `L`: O(L)
    *   Search for prefix of length `P`: O(P)
*   **Space Complexity:** O(N*M) in worst case where N is number of words and M is average length, if all words are distinct. More precisely, O(total number of characters in all words if no sharing, or O(number of nodes in Trie)).

*(Tree Traversal Algorithms and other tree content remain as before)*

**Pythonic Tips & Common Pitfalls for Trees:**
*   *(Previous tips are good)*
*   **Visualization:** Similar to linked lists, drawing trees (especially for traversals, LCA, path problems) is immensely helpful for understanding the flow of recursion or iteration.

______________

- before updating any datatype always check if it's empty.
- 
### Array - mutable
1. access - `array[index]`
2. update - `array[index]`
3. append - `array.append(item)`
4. insert - `array.insert(index, item)`
5. remove - `arrary.pop(index)`
6. remove first occurrence - `array.remove(item)`
7. find item - `value in array` 
8. find first occurrence - `array.index(value, start, end)`
9. slicing - `array[start : end : steps]`
10. copy - `array.copy` or `list(array)` or `array[:]`
11. sort - `array.sort()`
12. reverse - `array.reverse()`
13. concatenation - `array1 + array2` or `array1.extend(array2)`
14. filter array - `[list comprehension]`

### String - immutable
1. access - `string[index]`
2. slicing = `string[start : end : steps]`
3. concatenation - `string1 + string2` - O(n+m)
4. join - `string.join(list)`
5. find substring - `substring in string`
6. find index of substring - `string.find(substring`
7. count occurrences of substring - `string.count(substring)`
8. check prefix & suffix - `string.startswith(substring)` and `string.endswith(substring)`
9. replace substring - `string.replace(substring)`
10. string split - `string.split(separator, maxsplit)`
11. case conversion - `.upper()` `.lower()` `.capitalize()` `.title()` `.swapcase()`
12. strip whitespace - `.strip()` `.lstrip()` `.rstrip()`
13. Character type checks - `isdigit()` `isalpha()` `isalnum()` `islower()` `isupper()` `isspace()`

### Dictionary
1. insert/ update - `dict["key"] = value`
2. find value of key - `dict["key"]` or `dict.get(key, defult = None)`
3. delete - `del dict["key]` or `dict.pop(key, default_value)`
4. membership - `key in dict` 
5. loop - primarily its `dict.keys` and `dict.values`
6. search for value - iterate
7. remove all - `dict.clear()`
8. shallow copy - `dict.copy()`
9. `collections.defaltdict` - building frequency maps, adjacency lists
10. `collections.counter` - highly optimised for counting tasks

### Sets
1. add item - `set.add(item)`
2. remove item - `set.remove()` or or `set.pop()` and `set.discard()` doesn't throw error
3. membership - `item in set`
4. union - `set1 | set2` or `set1.union(set2)`
5. intersection - `set1 & set2` or `set1.intersection(set2)`
6. difference - `set1 - set2` or `set1.difference(set2)`
7. symmetric difference - `set1 ^ set2` or `set1.symmetric_difference(set2)`
8. subset - `set1.issubset(set2)` or `set1<=set2`
9. superset - `set1.issuperset(set2)` or `set1 >= set2`
10. proper subset and superset - `set1 < set2` and `set1 > set2`

### Stack 
1. push - `stack.append(item)`
2. pop - `stack.pop()`
3. peek - `stack[-1]`
4. Is stack empty - `not stack`
5. loop - array
6. reverse - array or pop and push every iteration

### Queue `collections.deque`
1. enqueue - `deque.append(item)`
2. dequeue - `deque.popleft()`
3. peek at the front of queue - `deque[0]`
4. Is queue empty - `not deque`
5. loop - `for item in deque`

### Priority Queue `heapq`
1. insert an item - `heapq.heappush(heaplist, item)`
2. pop - `heapq.heappop(heaplist)`
3. peek - `heaplist[0]`
4. heapify - `heapq.heapify(list)`
5. push and pop (efficient) - `heapq.heappushpop(heap, item)`
6. pop then push - `heapq.heaprepalace(heap, item)`
7. Get K smallest and largest - `heapq.nsmallest(k-value, heaplist)` and `heapq.nlargest(k-value, heaplist)`
8. 



| Data Type                       | Operation / Method                 | Time Complexity (Avg)            | Time Complexity (Worst)         | Space Complexity (Auxiliary) | Common LeetCode Use Case / Notes                                                                 |
|---------------------------------|------------------------------------|----------------------------------|---------------------------------|------------------------------|-------------------------------------------------------------------------------------------------|
| **`list`**                      | `append(x)`                        | O(1) Amortized                   | O(N) (resize)                   | O(1)                         | Adding to end of a dynamic array, stack implementation.                                         |
|                                 | `pop()` (from end)                 | O(1) Amortized                   | O(N) (resize)                   | O(1)                         | Removing from end, stack implementation.                                                        |
|                                 | `insert(i, x)`                     | O(N)                             | O(N)                            | O(1)                         | Inserting at specific index (shifts elements). Less common if performance critical.             |
|                                 | `pop(i)` (from index `i`)          | O(N)                             | O(N)                            | O(1)                         | Removing from specific index (shifts elements).                                                 |
|                                 | `remove(x)` (first occurrence)     | O(N)                             | O(N)                            | O(1)                         | Searching and removing.                                                                         |
|                                 | `l[i]` (access)                    | O(1)                             | O(1)                            | O(1)                         | Direct access by index.                                                                         |
|                                 | `l[i] = x` (update)                | O(1)                             | O(1)                            | O(1)                         | Direct update by index.                                                                         |
|                                 | `len(l)`                           | O(1)                             | O(1)                            | O(1)                         | Getting size.                                                                                   |
|                                 | `x in l` (membership)              | O(N)                             | O(N)                            | O(1)                         | Checking if element exists (linear scan).                                                       |
|                                 | `l.sort()` (in-place)              | O(N log N)                       | O(N log N)                      | O(log N) or O(N) (Timsort)   | Sorting the list.                                                                               |
|                                 | `sorted(l)` (returns new)          | O(N log N)                       | O(N log N)                      | O(N)                         | Getting a sorted copy.                                                                          |
|                                 | `l.reverse()` (in-place)           | O(N)                             | O(N)                            | O(1)                         | Reversing the list.                                                                             |
|                                 | `l[:]` or `l.copy()` (shallow)     | O(N)                             | O(N)                            | O(N)                         | Creating a shallow copy.                                                                        |
|                                 | Slicing `l[a:b]`                   | O(k) (k = b-a)                   | O(k) (k = b-a)                  | O(k)                         | Creating sublists.                                                                              |
| **`str`**                       | `s[i]` (access)                    | O(1)                             | O(1)                            | O(1)                         | Accessing characters.                                                                           |
|                                 | `len(s)`                           | O(1)                             | O(1)                            | O(1)                         | Getting length.                                                                                 |
|                                 | `s1 + s2` (concatenation)          | O(N+M)                           | O(N+M)                          | O(N+M)                       | Creates a new string. Inefficient in loops; use `"".join()`.                                    |
|                                 | `"".join(iterable)`                | O(L) (L=total length)            | O(L) (L=total length)           | O(L)                         | Efficiently concatenating multiple strings.                                                     |
|                                 | Slicing `s[a:b]`                   | O(k) (k = b-a)                   | O(k) (k = b-a)                  | O(k)                         | Creating substrings.                                                                            |
|                                 | `char in s` (membership)           | O(N)                             | O(N)                            | O(1)                         | Checking if character/substring exists (can be faster with advanced algorithms).                |
|                                 | `s.find(sub)` / `s.index(sub)`     | O(N*M) (naive), O(N+M) (actual)  | O(N*M)                          | O(1) or O(M)                 | Finding substring. `index` raises ValueError if not found.                                      |
|                                 | `s.replace(old, new)`              | O(N)                             | O(N)                            | O(N)                         | Returns new string with replacements.                                                           |
|                                 | `s.split(sep)`                     | O(N)                             | O(N)                            | O(N)                         | Splitting string into a list of substrings.                                                     |
| **`dict`**                      | `d[key]` (access)              | O(1)                             | O(N) (hash collisions)          | O(1)                         | Getting value by key. Raises KeyError if not found.                                             |
|                                 | `d.get(key, default)`            | O(1)                             | O(N) (hash collisions)          | O(1)                         | Safe access by key.                                                                             |
|                                 | `d[key] = value` (insert/update) | O(1)                             | O(N) (hash collisions)          | O(1)                         | Storing key-value pairs. Crucial for frequency counts, memoization.                             |
|                                 | `del d[key]` / `d.pop(key)`        | O(1)                             | O(N) (hash collisions)          | O(1)                         | Removing items.                                                                                 |
|                                 | `key in d` (membership)            | O(1)                             | O(N) (hash collisions)          | O(1)                         | Checking if key exists.                                                                         |
|                                 | `len(d)`                           | O(1)                             | O(1)                            | O(1)                         | Getting number of key-value pairs.                                                              |
|                                 | `d.keys()`, `d.values()`, `d.items()` | O(1) for view obj, O(N) to iterate | O(1) for view obj, O(N) to iterate | O(1) (view obj)            | Iterating over keys, values, or items. Iteration is O(N).                                       |
| **`set`**                       | `add(x)`                           | O(1)                             | O(N) (hash collisions)          | O(1)                         | Adding unique elements.                                                                         |
|                                 | `remove(x)`                        | O(1)                             | O(N) (hash collisions)          | O(1)                         | Removing element. Raises KeyError if not found.                                                 |
|                                 | `discard(x)`                       | O(1)                             | O(N) (hash collisions)          | O(1)                         | Safe removal of element.                                                                        |
|                                 | `pop()` (arbitrary element)        | O(1)                             | O(N) (hash collisions)          | O(1)                         | Remove and return an arbitrary element.                                                         |
|                                 | `x in s` (membership)              | O(1)                             | O(N) (hash collisions)          | O(1)                         | Fast check for element existence. Great for finding duplicates, visited tracking.               |
|                                 | `len(s)`                           | O(1)                             | O(1)                            | O(1)                         | Getting number of unique elements.                                                              |
|                                 | Set operations (`&`, `\|`, `-`, `^`) | O(len(s1)+len(s2)) (approx)      | O(len(s1)*len(s2)) (worst case) | O(len(s1)+len(s2)) (new set) | Union, intersection, difference, symmetric difference.                                          |
| **`collections.deque`**         | `append(x)`                        | O(1)                             | O(1)                            | O(1)                         | Adding to right end.                                                                            |
|                                 | `appendleft(x)`                    | O(1)                             | O(1)                            | O(1)                         | Adding to left end. Core for BFS queues.                                                        |
|                                 | `pop()` (from right)               | O(1)                             | O(1)                            | O(1)                         | Removing from right end.                                                                        |
|                                 | `popleft()` (from left)            | O(1)                             | O(1)                            | O(1)                         | Removing from left end. Core for BFS queues.                                                    |
|                                 | `d[i]` (access, not recommended)   | O(N)                             | O(N)                            | O(1)                         | Possible but slow, deques are not for random access.                                            |
|                                 | `rotate(n)`                        | O(N) (Python's C impl is O(k) for rotate(k) but O(N) if k approx N/2) | O(N)                       | O(1)                         | Rotating elements.                                                                              |
| **`collections.Counter`**       | (Inherits from `dict`)             | (Like dict)                      | (Like dict)                     | (Like dict)                  | Specialized dictionary for counting hashable objects.                                           |
|                                 | `c[key] += 1`                      | O(1)                             | O(N) (hash collisions)          | O(1)                         | Incrementing counts.                                                                            |
|                                 | `most_common(n)`                   | O(K log k_mc) (K items, k_mc=n)  | O(K log k_mc)                   | O(k_mc)                      | Getting n most common elements and their counts. (If n is None, sorts all K items: O(K log K)) |
| **`collections.defaultdict`**   | (Inherits from `dict`)             | (Like dict)                      | (Like dict)                     | (Like dict)                  | Dictionary that provides a default value for a nonexistent key. Useful for grouping items.      |
|                                 | `d[non_existent_key]`              | O(1) (for factory call)          | O(N) (hash collisions)          | O(1) (+ space for new value) | Accessing a key calls default_factory if key missing.                                           |
| **`heapq` module**              | `heapq.heappush(heap, item)`       | O(log N)                         | O(log N)                        | O(1)                         | Adding item to heap. For min-heaps by default. For max-heap, store `-item`.                     |
| (operates on lists)             | `heapq.heappop(heap)`              | O(log N)                         | O(log N)                        | O(1)                         | Removing smallest item from heap.                                                               |
|                                 | `heapq.heapify(list)`              | O(N)                             | O(N)                            | O(1) (in-place)              | Transforming a list into a heap in-place.                                                       |
|                                 | `heap[0]` (access min/max)         | O(1)                             | O(1)                            | O(1)                         | Accessing smallest element (for min-heap).                                                      |
|                                 | `heapq.nlargest(k, iter)`          | O(N log k)                       | O(N log k)                      | O(k)                         | Get k largest elements.                                                                         |
|                                 | `heapq.nsmallest(k, iter)`         | O(N log k)                       | O(N log k)                      | O(k)                         | Get k smallest elements.                                                                        |
| **`tuple`**                     | `t[i]` (access)                    | O(1)                             | O(1)                            | O(1)                         | Immutable sequence, fast access.                                                                |
|                                 | `len(t)`                           | O(1)                             | O(1)                            | O(1)                         | Getting size.                                                                                   |
|                                 | `x in t` (membership)              | O(N)                             | O(N)                            | O(1)                         | Checking if element exists (linear scan).                                                       |
|                                 | Slicing `t[a:b]`                   | O(k) (k = b-a)                   | O(k) (k = b-a)                  | O(k)                         | Creating subtuples. Used as dict keys if elements are hashable.                                 |	
**The Core Concepts & How Data Types Fit In**

We can think of data structures along a few axes:

1. **Collection Type:**
    
    - **Sequence:** Ordered collection of items. Access by numerical index.
        
    - **Mapping:** Collection of key-value pairs. Access by key.
        
    - **Set-like:** Unordered collection of unique items. Fast membership testing.
        
2. **Mutability:** Can it be changed after creation?
    
3. **Specialization:** Is it a general-purpose tool or optimized for a specific task?
    

**Visualizing the Relationships (Conceptual Hierarchy/Grouping)**

Instead of one giant flat table, let's think in groups. You can still have your detailed table as a reference, but this conceptual grouping helps with understanding.

**Group 1: The Sequences - "Things in a Row"**

- **Core Idea:** Ordered items, accessible by an integer index (0-based).
    
- **Most Basic (Conceptual):** An array (though Python's list is more dynamic).
    
    - **list (Mutable Sequence)**
        
        - **Foundation:** The workhorse. A dynamic array that can grow or shrink.
            
        - **Key Operations Reflecting "Sequence":**
            
            - l[i] (access): O(1)
                
            - l[i] = x (update): O(1)
                
            - append(x): O(1) amortized (at the end)
                
            - pop(): O(1) amortized (from the end)
                
            - insert(i, x), pop(i): O(N) (because items need to shift)
                
            - Slicing l[a:b]: O(k) where k is slice length
                
            - len(l): O(1)
                
        - **Similarity:** Think of it as a flexible, numbered shelf.
            
    - **tuple (Immutable Sequence)**
        
        - **Builds on:** The concept of a sequence, but immutable.
            
        - **Differences from list:** Cannot be changed after creation (no append, insert, pop that modifies in-place, no l[i]=x).
            
        - **Key Operations (similar to list for read-only):**
            
            - t[i] (access): O(1)
                
            - Slicing t[a:b]: O(k)
                
            - len(t): O(1)
                
            - x in t: O(N)
                
        - **Why use it?** When you need a guarantee that the sequence won't change. Often used as keys in dictionaries (since lists are mutable and unhashable).
            
        - **Similarity:** A fixed, numbered shelf.
            
    - **str (Immutable Sequence of Characters)**
        
        - **Specialization of:** An immutable sequence, specifically for characters.
            
        - **Key Operations (similar to tuple, but with string-specific methods):**
            
            - s[i] (access): O(1)
                
            - Slicing s[a:b]: O(k)
                
            - len(s): O(1)
                
            - char in s: O(N) (can be faster with more complex algorithms like KMP for substring search, but conceptually a scan)
                
            - Concatenation s1 + s2: O(N+M) (creates a new string)
                
            - "".join(iterable_of_strings): O(Total Length) - efficient concatenation.
                
        - **Similarity:** A fixed sequence of letters/symbols.
            
    - **collections.deque (Double-Ended Queue - Mutable Sequence Optimized for Ends)**
        
        - **Builds on:** The concept of a sequence, but with highly efficient additions/removals from both ends. Implemented as a doubly-linked list (or similar).
            
        - **Key Operations (Key Differentiators from list):**
            
            - append(x) (right): O(1)
                
            - appendleft(x) (left): O(1)
                
            - pop() (right): O(1)
                
            - popleft() (left): O(1)
                
        - **Operations that are worse than list:**
            
            - d[i] (access by index): O(N) - because it might have to traverse from an end.
                
        - **Why use it?** BFS algorithms (queue), sliding window problems where you add/remove from both ends.
            
        - **Similarity:** A flexible line (queue) where people can efficiently join/leave from the front or back, but finding someone in the middle is slow.
            

**Group 2: The Mappings - "Lookup by Label"**

- **Core Idea:** Store key-value pairs. Fast lookup, insertion, deletion based on the key. Typically implemented with hash tables.
    
- **Most Basic:** A hash table.
    
    - **dict (Mutable Mapping)**
        
        - **Foundation:** The primary mapping type.
            
        - **Key Operations Reflecting "Mapping":**
            
            - d[key] (access): O(1) average, O(N) worst (hash collisions)
                
            - d[key] = value (insert/update): O(1) average, O(N) worst
                
            - del d[key]: O(1) average, O(N) worst
                
            - key in d: O(1) average, O(N) worst
                
            - len(d): O(1)
                
        - **Similarity:** A filing cabinet where each folder has a unique label (key) and contains information (value).
            
    - **collections.defaultdict (Mutable Mapping with Default Values)**
        
        - **Specialization of dict:** Inherits from dict.
            
        - **Key Enhancement:** If you try to access a key that doesn't exist, instead of raising a KeyError, it automatically creates that key with a default value provided by a "default factory" (e.g., int for 0, list for an empty list).
            
        - **Operations:** Same complexities as dict for standard operations. The default factory call is typically O(1).
            
        - **Why use it?** Simplifying code when grouping items or counting, as you don't need to check if a key exists before appending to its list or incrementing its count.
            
        - **Similarity:** A filing cabinet that automatically creates an empty folder (of a pre-defined type) if you ask for a label that doesn't exist.
            
    - **collections.Counter (Mutable Mapping for Counting Hashables)**
        
        - **Specialization of dict:** Inherits from dict.
            
        - **Key Enhancement:** Values are integers representing counts. Provides convenient methods for counting. Keys that don't exist are treated as having a count of 0.
            
        - **Operations:**
            
            - Standard dict operations apply with same complexities.
                
            - c[key] += 1: Still O(1) average.
                
            - most_common(n): O(K log N) or O(K + N log K) depending on implementation details (K total unique items).
                
        - **Why use it?** Frequency counting (e.g., character counts in a string for anagrams).
            
        - **Similarity:** A filing cabinet specifically for tallying how many times you've seen each label.
            

**Group 3: The Sets - "Unique Items, Fast Checks"**

- **Core Idea:** Unordered collection of unique, hashable items. Extremely fast membership testing, insertion, and deletion. Also implemented with hash tables.
    
    - **set (Mutable Set)**
        
        - **Foundation:** The primary set type.
            
        - **Key Operations Reflecting "Set":**
            
            - add(x): O(1) average, O(N) worst
                
            - remove(x) (raises KeyError if not found): O(1) average, O(N) worst
                
            - discard(x) (no error if not found): O(1) average, O(N) worst
                
            - x in s: O(1) average, O(N) worst
                
            - len(s): O(1)
                
            - Set operations (union |, intersection &, difference -): Generally O(len(s1) + len(s2)).
                
        - **Similarity:** A bag where you can quickly check if an item is inside, add new items (duplicates are ignored), and remove items. The order doesn't matter.
            
    - **frozenset (Immutable Set)**
        
        - **Builds on:** The concept of a set, but immutable.
            
        - **Differences from set:** Cannot be changed after creation (no add, remove, discard).
            
        - **Key Operations (similar to set for read-only and creation):**
            
            - x in fs: O(1) average, O(N) worst
                
            - len(fs): O(1)
                
            - Set operations create new frozensets.
                
        - **Why use it?** When you need an immutable set, e.g., as a key in a dictionary or an element in another set.
            
        - **Similarity:** A sealed bag of unique items.
            

**Group 4: The Adapters/Algorithms (Operate on other types)**

- **heapq module (Priority Queue Algorithms)**
    
    - **Not a data type itself, but a collection of algorithms that operate on a standard Python list to maintain heap invariant.**
        
    - **Core Idea:** Keeps the smallest (min-heap, default) or largest (max-heap, by storing negative numbers) element at index 0, allowing for O(log N) insertion and removal of this extremal element.
        
    - **Key Operations:**
        
        - heapq.heappush(heap_list, item): O(log N)
            
        - heapq.heappop(heap_list): O(log N)
            
        - heap_list[0] (access min/max): O(1)
            
        - heapq.heapify(list) (transform list into heap in-place): O(N)
            
    - **Why use it?** Dijkstra's, Prim's, Kth largest/smallest element, any problem needing efficient access to the min/max element while dynamically adding/removing.
        
    - **Relationship:** It adapts a list to behave like a priority queue. You're still working with a list under the hood.
        

**How This Helps Memorization:**

1. **Anchor to Core Concepts:**
    
    - Need order and indexing? Think **Sequences**. Then decide: mutable (list), immutable (tuple), text (str), or fast end-ops (deque).
        
    - Need key-value lookup? Think **Mappings**. Then decide: basic (dict), with defaults (defaultdict), or for counting (Counter).
        
    - Need unique items and fast "is it there?" checks? Think **Sets**. Then decide: mutable (set) or immutable (frozenset).
        
    - Need efficient min/max access? Think heapq (acting on a list).
        
2. **Understand Specializations:**
    
    - defaultdict and Counter are just dicts with extra convenience. Their core performance for get/set/delete is the same as dict.
        
    - tuple and frozenset are the immutable twins of list and set. Operations that don't modify are similar.
        
3. **Focus on Key Differentiators:**
    
    - Why deque over list? O(1) appendleft/popleft.
        
    - Why set over list for membership? O(1) vs O(N) for in.
        
    - Why dict over list for lookups? O(1) key-based vs O(N) value-based search.
        
4. **Common Operations & Their General Complexities:**
    
    - len(): Almost always O(1).
        
    - Indexed access [i] for sequences: O(1).
        
    - Key access [key] for mappings/sets: O(1) average.
        
    - in operator: O(1) average for mappings/sets, O(N) for sequences (lists, tuples, strings).
        
    - Operations that shift elements in a list/array-based structure (insert, pop(i)): O(N).
        

**Visualizing this for your Table:**

You could augment your big table with:

- **A "Group" column:** (Sequence, Mapping, Set, Adapter)
    
- **A "Base Concept/Builds On" column:** (e.g., for defaultdict, "dict"; for deque, "sequence, linked-list like ends")
    
- **Use indentation or sub-headings** in your documentation to visually represent these groups.
    
- **Start with an introductory section** explaining these core concepts before diving into the detailed table.
    

This way, when you look at defaultdict.get(), you immediately think "it's a dict, so get() is O(1) average," rather than memorizing it in isolation. You're building a mental model, not just a fact list.



___________________

You have to be familiar with the data structures that are available in the language of your choice. Here's a list

- Lists/Dynamic arrays
- Stacks
- Queues
- HashMaps/Dictionary
- Sets
- Heaps

A data structure that can maintain sorted order and you make queries such as check if a value less than x exist, check if a value greater than x exists. In Python you can use bisect_left and bisect_right, in Java there is TreeMap/TreeSets.

Array
- Insert an item
- Remove an item
- Update an item
- Find an item
- Loop over array
- Copy an array
- Copy part of an array
- Sort an array
- Reverse an array
- Swap two items
- Filter an array

Linked List
- Insert a node
- Remove a node
- Update a node
- Find a node
- Loop over linked list
- Reverse a linked list
- Swap two nodes

Stack and Queue
- Enqueue an item
- Dequeue an item
- Push an item to a stack
- Pop an item from a stack
- Loop over a stack or queue
- Peek at the top of a stack
- Reverse a stack
- Get size of stack or queue

Hash Table
- Insert a key-value pair
- Find the value for a key
- Update the value for a key
- Check if a key has been used
- Loop over key-value pairs
- Delete a key-value pair
- Search for a value

Graph
- Insert a node into a graph
- Remove a node from a graph
- Add an edge between two nodes
- Find the neighbors of a node
- Find a path between two nodes

Heap
- Insert an item
- Pop the top item
- Peek the top item
- Remove an item
- Update an item

_________________


# References


