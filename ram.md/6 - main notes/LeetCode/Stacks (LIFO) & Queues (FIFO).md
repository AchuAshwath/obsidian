07-05-2025 08:54:02

Status : #child 

Tags : [[LeetCode]]

# Stack (LIFO - Last-In, First-Out)

**Concept:**
*   A linear data structure that follows the **Last-In, First-Out (LIFO)** principle.
*   The last element added to the stack is the first one to be removed.
*   Think of a stack of plates: you add (push) a plate to the top, and you remove (pop) a plate from the top.
*   Main operations:
    *   **Push:** Add an item to the top of the stack.
    *   **Pop:** Remove an item from the top of the stack.
    *   **Peek (or Top):** View the item at the top of the stack without removing it.
    *   **isEmpty:** Check if the stack is empty.
    *   **Size:** Get the number of items in the stack.

**Python Implementation:**

Python doesn't have a separate built-in stack type. Stacks are commonly implemented using:

1.  **Python `list`:**
    *   `append()` for `push` operation (adds to the end, which acts as the "top").
    *   `pop()` (without an index) for `pop` operation (removes from the end).
    *   This is often sufficient and very straightforward for most LeetCode problems.

2.  **`collections.deque` (Double-Ended Queue):**
    *   `append()` for `push`.
    *   `pop()` for `pop`.
    *   `deque` can be slightly more efficient for very high-frequency push/pop operations if you're strictly using it as a stack, as its appends/pops from either end are O(1) non-amortized (lists are O(1) *amortized* for `append`/`pop` from end). However, for typical LeetCode scenarios, `list` is usually fine and simpler. `deque` is more often chosen for its O(1) `popleft()` when implementing queues.

**Core Operations (using `list` as a stack, Time Complexity):**

Let `my_stack` be a Python list used as a stack.

1.  **Push an item to a stack:** `my_stack.append(item)`
    *   Syntax: `my_stack.append(item)`
    *   Description: Adds `item` to the top (end) of the stack.
    *   Time Complexity: **O(1) amortized**

    ```python
stack = []
stack.append(10)
stack.append(20)
stack.append(30)
print(stack)  # Output: [10, 20, 30] (30 is at the top)
```

2.  **Pop an item from a stack:** `item = my_stack.pop()`
    *   Syntax: `top_item = my_stack.pop()`
    *   Description: Removes and returns the item from the top (end) of the stack. Raises `IndexError` if the stack is empty.
    *   Time Complexity: **O(1) amortized**

    ```python
stack = [10, 20, 30]
top = stack.pop()
print(f"Popped: {top}") # Output: Popped: 30
print(stack)            # Output: [10, 20]
# stack.pop(); stack.pop() # Pop 20, then 10
# stack.pop() # Would raise IndexError if stack is now empty
    ```

3.  **Peek at the top of a stack:** `my_stack[-1]`
    *   Syntax: `top_item = my_stack[-1]` (if stack is not empty)
    *   Description: Returns the item at the top of the stack without removing it. Raises `IndexError` if the stack is empty.
    *   Time Complexity: **O(1)**
   
    ```python
stack = [10, 20, 30]
if stack: # Check if stack is not empty
	print(f"Top item: {stack[-1]}") # Output: Top item: 30
print(stack)                         # Output: [10, 20, 30] (stack unchanged)
    ```

4.  **Check if stack is empty:** `not my_stack` or `len(my_stack) == 0`
    *   Syntax: `is_empty = not my_stack`
    *   Description: Returns `True` if the stack contains no items, `False` otherwise.
    *   Time Complexity: **O(1)**

    ```python
stack = []
print(f"Is stack empty? {not stack}") # Output: Is stack empty? True
stack.append(5)
print(f"Is stack empty? {not stack}") # Output: Is stack empty? False
```

5.  **Get size of stack:** `len(my_stack)`
    *   Syntax: `current_size = len(my_stack)`
    *   Time Complexity: **O(1)**

    ```python
stack = [1, 2, 3]
print(f"Size of stack: {len(stack)}") # Output: Size of stack: 3
    ```

6.  **Loop over a stack (less common for typical stack processing):**
    *   You can iterate through a list-based stack, but typically stacks are processed by pushing and popping elements. Iteration usually means you're just inspecting it or using the list for other purposes.

    ```python
stack = [10, 20, 30] # Top is 30
for item in reversed(stack): # To see items from top to bottom
		print(item)
# Output:
# 30
# 20
# 10
 ```

7.  **Reverse a stack (not a standard stack operation, but possible):**
    *   This usually involves popping all elements into a temporary structure (like another stack or a list) and then pushing them back.
    *   Using list's `reverse()` method if it's a list-based stack: `my_stack.reverse()`. This is O(n).

    ```python
stack_list = [1, 2, 3, 4] # Top is 4
# To conceptually reverse the stack order (what was bottom is now top)
# 1. Pop all to a temp list
temp_list = []
while stack_list:
	temp_list.append(stack_list.pop())
# temp_list is now [4, 3, 2, 1]
# 2. This temp_list itself now acts as the "reversed" stack if used directly,
# or push back to original if needed.
stack_list = temp_list # stack_list is now [4, 3, 2, 1], top is 1
print(stack_list)
```

**Key LeetCode Use Cases for Stacks:**
*   **Reversing things:** Reversing a string, reversing a linked list (part of the process).
*   **Parsing Expressions:**
    *   **Balanced Parentheses/Brackets:** Checking if an expression like `"{[()]}"` is valid. (e.g., LeetCode #20. Valid Parentheses)
    *   Evaluating postfix or infix expressions.
*   **Depth-First Search (DFS) for Graphs/Trees (Iterative approach):** An explicit stack is used to manage nodes to visit.
*   **Backtracking Algorithms:** The call stack in recursion implicitly acts as a stack. Sometimes an explicit stack is used for an iterative backtracking approach.
*   **Monotonic Stack Problems:** Problems where you need to find the next greater/smaller element, largest rectangle in histogram, etc. A stack is used to maintain elements in an increasing or decreasing order.
*   **Simulating Recursion:** Any recursive algorithm can be converted to an iterative one using an explicit stack.
*   Function call stacks (how programs manage function calls).

---

## B) Queue (FIFO - First-In, First-Out)

**Concept:**
*   A linear data structure that follows the **First-In, First-Out (FIFO)** principle.
*   The first element added to the queue is the first one to be removed.
*   Think of a checkout line at a store: the first person to join the line (enqueue) is the first person to be served (dequeue).
*   Main operations:
    *   **Enqueue:** Add an item to the rear (back) of the queue.
    *   **Dequeue:** Remove an item from the front of the queue.
    *   **Peek (or Front):** View the item at the front of the queue without removing it.
    *   **isEmpty:** Check if the queue is empty.
    *   **Size:** Get the number of items in the queue.

**Python Implementation:**

*   **`collections.deque` (Double-Ended Queue) is the **highly recommended** and standard way to implement a queue in Python.**
    *   `append()` for `enqueue` (adds to the right end, which acts as the "rear").
    *   `popleft()` for `dequeue` (removes from the left end, which acts as the "front").
    *   Both `append()` and `popleft()` are **O(1)** operations on a `deque`.

*   **Using a `list` for a queue is INEFFICIENT:**
    *   If you use `list.append()` for enqueue and `list.pop(0)` for dequeue, `list.pop(0)` is an **O(n)** operation because all subsequent elements must be shifted left. This makes list-based queues slow for many operations. **Avoid this for LeetCode problems requiring efficient queues.**

**Core Operations (using `collections.deque` as a queue, Time Complexity):**

```python
from collections import deque

my_queue = deque()
````

1. **Enqueue an item:** my_queue.append(item)
    - Syntax: my_queue.append(item)
    - Description: Adds item to the rear (right end) of the queue.
    - Time Complexity: **O(1)**

```python
queue = deque() 
queue.append(10) # Enqueue 10 
queue.append(20) # Enqueue 20 
queue.append(30) # Enqueue 30 
print(queue)     # Output: deque([10, 20, 30]) (10 is at the front, 30 at the rear)`
```

- **Dequeue an item:** item = my_queue.popleft()
    - Syntax: front_item = my_queue.popleft()
    - Description: Removes and returns the item from the front (left end) of the queue. Raises IndexError if the queue is empty.
    - Time Complexity: **O(1)**
   
```python
queue = deque([10, 20, 30]) 
front = queue.popleft() 
print(f"Dequeued: {front}") # Output: Dequeued: 10 
print(queue)                # Output: deque([20, 30])
```       

- **Peek at the front of a queue:** my_queue[0]
    - Syntax: front_item = my_queue[0] (if queue is not empty)
    - Description: Returns the item at the front of the queue without removing it. Raises IndexError if the queue is empty.
    - Time Complexity: **O(1)**

```python
queue = deque([10, 20, 30]) 
if queue: # Check if queue is not empty     
	print(f"Front item: {queue[0]}") # Output: Front item: 10 

print(queue)                         # Output: deque([10, 20, 30])
```
   
- **Check if queue is empty:** not my_queue or len(my_queue) == 0
    - Syntax: is_empty = not my_queue
    - Description: Returns True if the queue contains no items, False otherwise.
    - Time Complexity: **O(1)**

```python
queue = deque() 
print(f"Is queue empty? {not queue}") # Output: Is queue empty? True 
queue.append(5) 
print(f"Is queue empty? {not queue}") # Output: Is queue empty? False
```
   
- **Get size of queue:** len(my_queue)
    - Syntax: current_size = len(my_queue)
    - Time Complexity: **O(1)**

```python
queue = deque([1, 2, 3, 4]) 
print(f"Size of queue: {len(queue)}") # Output: Size of queue: 4
```
   
- **Loop over a queue (less common for typical queue processing):**
    - deque objects are iterable.
   
```python
queue = deque([10, 20, 30]) # Front is 10 
for item in queue:     
	print(item) # Output: # 10 # 20 # 30
```
   
**Key LeetCode Use Cases for Queues:**
- **Breadth-First Search (BFS) for Graphs/Trees:** A queue is essential to manage nodes to visit level by level. This is one of the most common uses.
- **Level-Order Traversal of Trees:** A specific application of BFS.
- **Managing Tasks in Order:** Simulating systems where tasks are processed in the order they arrive.
- **Sliding Window Minimum/Maximum (Advanced):** A deque can be used cleverly to maintain candidates for the minimum/maximum in a sliding window efficiently (often called a monotonic queue).
- Shortest path in unweighted graphs.
- Implementing a message queue or task scheduler (conceptual).

**Pythonic Tips & Common Pitfalls for Stacks & Queues:**
- **Always use collections.deque for efficient queues.** Using list.pop(0) for dequeueing is a common mistake leading to TLE (Time Limit Exceeded) on LeetCode.
- For stacks, list.append() and list.pop() are generally fine and often more convenient than importing deque if you don't need deque's other features.
- Remember to handle empty stack/queue conditions to avoid IndexError when calling pop(), popleft(), or accessing stack[-1] / queue[0]. Always check if the structure is non-empty first.

```python
if my_stack:     
	top_element = my_stack.pop() # or 
try:     
	top_element = my_stack.pop() 
except IndexError:     # Handle empty stack     
	pass
```
## References


