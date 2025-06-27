07-05-2025 08:55:15

Status : #child 

Tags : [[LeetCode]]

# Heaps (Priority Queues)

**Concept: What is a Heap?**
*   A heap is a specialized tree-based data structure that satisfies the **heap property**.
*   **Binary Heap:** The most common type, which is a binary tree (each node has at most two children).
*   **Heap Property:**
    *   **Min-Heap:** For every node `N`, the value of `N` is less than or equal to the values of its children. This means the smallest element is always at the root of the tree.
    *   **Max-Heap:** For every node `N`, the value of `N` is greater than or equal to the values of its children. This means the largest element is always at the root.
*   **Complete Binary Tree:** A binary heap is typically implemented as a complete binary tree. This means all levels of the tree are fully filled, except possibly the last level, which is filled from left to right. This property allows heaps to be efficiently represented using an array (or Python list).

**Array Representation of a Binary Heap:**
For a 0-indexed array `arr`:
*   The root is at index `0`.
*   For a node at index `i`:
    *   Its left child is at index `2*i + 1`.
    *   Its right child is at index `2*i + 2`.
    *   Its parent is at index `(i - 1) // 2`.

**Concept: What is a Priority Queue?**
*   A priority queue is an abstract data type (ADT) similar to a regular queue, but each element has an associated "priority."
*   Elements with higher priorities are served before elements with lower priorities.
*   If two elements have the same priority, their order might depend on their insertion order (FIFO) or be undefined.
*   Heaps are a very common and efficient way to implement priority queues.

**Python Implementation: The `heapq` Module**

*   Python's standard library provides the `heapq` module.
*   `heapq` implements a **min-heap** using a standard Python `list`.
*   The list is maintained such that `heap[0]` is always the smallest element.
*   The functions in `heapq` modify the list in-place to maintain the heap property.

**Core Operations (using `heapq` for a min-heap, Time Complexity N = items in heap):**

```python
import heapq

# The "heap" is just a Python list
min_heap = []
```

- **Insert an item (Push): heapq.heappush(heap_list, item)**
	- Syntax: heapq.heappush(heap, item)
	- Description: Adds item to the heap (a Python list) while maintaining the min-heap property.
	- Time Complexity: O(log N) (The item is added to the end, then "sifted up" to its correct position).
	- Space Complexity: O(1) (for the operation itself, list resizing is amortized).

```python
    heapq.heappush(min_heap, 4)
    heapq.heappush(min_heap, 1)
    heapq.heappush(min_heap, 7)
    heapq.heappush(min_heap, 3)
    print(min_heap) # Output might be [1, 3, 7, 4] - internal list order
                    # but heapq.heappop() will always get the smallest (1)
```         

- **Pop the top item (smallest): item = heapq.heappop(heap_list)**
	- Syntax: smallest_item = heapq.heappop(heap)
	- Description: Removes and returns the smallest item (the root, heap[0]) from the heap. Raises IndexError if the heap is empty.
	- Time Complexity: O(log N) (The root is replaced with the last element, then "sifted down" to maintain the heap property).
	- Space Complexity: O(1).

```python
# Assuming min_heap = [1, 3, 7, 4] from previous example
smallest = heapq.heappop(min_heap)
print(f"Popped: {smallest}") # Output: Popped: 1
print(min_heap)              # Output might be [3, 4, 7]

next_smallest = heapq.heappop(min_heap)
print(f"Popped: {next_smallest}") # Output: Popped: 3
print(min_heap)                   # Output might be [4, 7]
```
   
- **Peek the top item (smallest): heap_list[0]**
	- Syntax: smallest_item = heap[0] (if heap is not empty)
	- Description: Returns the smallest item from the heap without removing it. Raises IndexError if the heap is empty.
	- Time Complexity: O(1)
	- Space Complexity: O(1).

```python
min_heap = []
heapq.heappush(min_heap, 5)
heapq.heappush(min_heap, 2)
heapq.heappush(min_heap, 8) # min_heap might be [2, 5, 8] internally
if min_heap:
    print(f"Smallest item: {min_heap[0]}") # Output: Smallest item: 2
```

- **Build a heap from an existing list (Heapify): heapq.heapify(list)**
	- Syntax: heapq.heapify(x)
	- Description: Transforms a list x into a valid min-heap, in-place.
	- Time Complexity: O(N) (This is more efficient than pushing N items one by one, which would be O(N log N)).
	- Space Complexity: O(1) (in-place).

```python
data = [9, 5, 2, 8, 1, 6, 3, 7, 4]
heapq.heapify(data) # data is now a valid min-heap
print(data) # Output might be [1, 4, 2, 7, 5, 6, 3, 8, 9]
            # data[0] is guaranteed to be the smallest (1)
```

- **Push then Pop: item = heapq.heappushpop(heap, item)**
	- Syntax: result = heapq.heappushpop(heap, item)
	- Description: Pushes item onto the heap, then pops and returns the smallest item from the heap. More efficient than separate heappush followed by heappop because it might avoid one sift operation. Useful for maintaining a fixed-size heap of the largest elements (if it's a min-heap).
	- Time Complexity: O(log N)
	- Space Complexity: O(1).

```python
# Example: Keep a heap of the 3 largest numbers seen so far (using a min-heap)
# For this specific problem, we store numbers directly.
# If incoming number is larger than the smallest in heap, replace.
max_k_heap = [] # This will be a min-heap
k = 3
stream = [4, 1, 7, 3, 8, 5, 9, 2, 6]

for num in stream:
    if len(max_k_heap) < k:
        heapq.heappush(max_k_heap, num)
    elif num > max_k_heap[0]: # If current num is larger than smallest of the k largest
        heapq.heappushpop(max_k_heap, num) # Push new, pop smallest

print(f"Top {k} largest numbers (in min-heap form): {max_k_heap}")
# After processing [4,1,7]: max_k_heap = [1,4,7]
# Process 3: no change
# Process 8: heappushpop(max_k_heap, 8) -> pushes 8, pops 1. max_k_heap = [4,7,8] (conceptual)
# Output will be the k largest numbers, with the smallest of them at heap[0].
# Sorted: [7, 8, 9] for this example. Heap will be [7,8,9] or equivalent heap form.
```
   
- **Pop then Push: item = heapq.heapreplace(heap, item)**
	- Syntax: result = heapq.heapreplace(heap, item)
	- Description: Pops and returns the smallest item from the heap, then pushes the new item. heapreplace is equivalent to heappop() followed by heappush(), but can be more efficient. The heap size doesn't change. Raises IndexError if heap is empty.
	- Time Complexity: O(log N)
	- Space Complexity: O(1).

```python
h = [1, 3, 5]
heapq.heapify(h) # Ensure it's a heap: [1, 3, 5]
replaced_item = heapq.heapreplace(h, 0) # Pops 1, pushes 0
print(f"Replaced: {replaced_item}, Heap: {h}") # Replaced: 1, Heap: [0, 3, 5] (or heapified form)
replaced_item = heapq.heapreplace(h, 4) # Pops 0, pushes 4
print(f"Replaced: {replaced_item}, Heap: {h}") # Replaced: 0, Heap: [3, 4, 5] (or heapified form)
```

- **Get K smallest/largest elements:**
	- heapq.nsmallest(k, iterable): Returns a list of the k smallest items from iterable.
	- heapq.nlargest(k, iterable): Returns a list of the k largest items from iterable.
	- Time Complexity: O(N log k) if N is much larger than k. More precisely, O(N + k log N) or O(N log k) depending on implementation details and relative sizes of N and k. For small k, this is efficient.
	- Space Complexity: O(k).

```python
data = [9, 5, 2, 8, 1, 6, 3, 7, 4, 0]
print(f"3 smallest: {heapq.nsmallest(3, data)}") # Output: [0, 1, 2]
print(f"3 largest: {heapq.nlargest(3, data)}")   # Output: [9, 8, 7]
```  

- **Remove an arbitrary item / Update an item:**
	- Not directly supported efficiently by heapq.
	- To remove an arbitrary item, you'd typically have to:
		- Find the item (O(N)).
		- Replace it with the last element in the heap.
		- Remove the last element (shorten the list).
		- Re-heapify by sifting the replaced element up or down (O(log N)).
		- Overall: O(N).
	- To update an item's priority:
		- Remove it (O(N)).
		- Push the item with its new priority (O(log N)).
		- Overall: O(N).
- For LeetCode, if you need efficient updates/removals of arbitrary items, heapq might not be the best choice, or the problem constraints imply N is small enough for O(N) operations, or there's a workaround (e.g., "lazy deletion" - mark items as deleted and ignore them when popped).
- Simulating a Max-Heap with heapq (Min-Heap):
- Since heapq only provides a min-heap, to simulate a max-heap, you can:
	- Store negated values: Push -value into the min-heap. When you pop, negate the result again to get the original maximum value.
	- Store tuples (-priority, item): If you have items with priorities, store (-priority, original_item). The min-heap will sort by the first element of the tuple, effectively giving you max-priority behavior.

```python
# Max-heap simulation using negated values
max_heap_sim = []
heapq.heappush(max_heap_sim, -4) # Store -4 for value 4
heapq.heappush(max_heap_sim, -1) # Store -1 for value 1
heapq.heappush(max_heap_sim, -7) # Store -7 for value 7

print(f"Internal max_heap_sim: {max_heap_sim}") # e.g., [-7, -1, -4]
largest_val = -heapq.heappop(max_heap_sim)
print(f"Largest value popped: {largest_val}") # Output: 7

# Max-heap simulation using tuples (priority, item)
tasks_max_heap = [] # (priority, task_id)
# Store as (-priority, task_id) to make min-heap behave like max-heap on priority
heapq.heappush(tasks_max_heap, (-5, "TaskA")) # Priority 5
heapq.heappush(tasks_max_heap, (-2, "TaskB")) # Priority 2
heapq.heappush(tasks_max_heap, (-8, "TaskC")) # Priority 8

priority, task_id = heapq.heappop(tasks_max_heap)
print(f"Highest priority task: {task_id} with priority {-priority}") # TaskC with priority 8
```

- **Key LeetCode Use Cases for Heaps/Priority Queues:**
    - Finding Kth Smallest/Largest Element: (e.g., LeetCode #215. Kth Largest Element in an Array).
        - For Kth largest: Use a min-heap of size k. Iterate through numbers. If heap size < k, add. Else if num > heap[0], pop smallest and add num.
        - For Kth smallest: Use a max-heap of size k.
    - Top K Frequent Elements: (e.g., LeetCode #347). Use a heap to keep track of the top k frequent elements, often pairing frequency with the element itself in a tuple.
    - Merge K Sorted Lists: (e.g., LeetCode #23). Use a min-heap to store one element from each list, always picking the smallest and adding the next from its list.
    - Dijkstra's Algorithm (Shortest Paths in Weighted Graphs): A min-priority queue is used to efficiently select the unvisited node with the smallest known distance.
    - Prim's Algorithm (Minimum Spanning Tree): Uses a priority queue to select the next edge to add.
    - Event-Driven Simulations / Scheduling: Manage events or tasks by their scheduled time/priority.
    - Problems involving "closest points to origin," "median from a data stream."
- **Pythonic Tips & Common Pitfalls for heapq:**
    - heapq operates on lists directly. The list itself is the heap. You don't create a Heap object.
    - Min-Heap by Default: Always remember heapq is a min-heap. If you need a max-heap, use the negation trick or tuple trick.
    - Tuple Comparison: When storing tuples (priority, item) in a heap, Python compares tuples element by element. If priorities are equal, it will then compare the next elements in the tuples. If these are not comparable (e.g., custom objects without __lt__), it can lead to errors. To break ties predictably or avoid errors with non-comparable items, you can add a unique, always-increasing counter as a secondary sort key: (priority, counter, item).

```python
import itertools
    counter = itertools.count() # Infinite counter
    # heapq.heappush(my_heap, (priority, next(counter), task_object))
```

- Stability: heapq is not stable by default. If two items have the same priority, their original relative order might not be preserved after heap operations. The counter trick above also helps with stability if needed.

Heaps are powerful for problems that require efficiently managing ordered elements, especially the minimum or maximum. Understanding how to use heapq for both min-heaps and simulated max-heaps is key.

## References


