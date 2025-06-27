07-05-2025 08:55:58

Status : #child

Tags : [[LeetCode]]
# Linked Lists 

**Concept:**
*   A **linear data structure** where elements (called **nodes**) are not necessarily stored in contiguous memory locations.
*   Each **node** contains two main parts:
    1.  **Data (or Value):** The actual information stored in the node.
    2.  **Pointer(s) (or Link/Reference):** Address(es) of the next (and possibly previous) node in the sequence.
*   The sequence starts with a **head** pointer, which points to the first node. The last node typically points to `None` (or `null`) to signify the end of the list.

**Types of Linked Lists:**
1.  **Singly Linked List:**
    *   Each node has data and a pointer to the *next* node only.
    *   Traversal is unidirectional (forward).
2.  **Doubly Linked List:**
    *   Each node has data, a pointer to the *next* node, and a pointer to the *previous* node.
    *   Traversal can be bidirectional (forward and backward).
3.  **Circular Linked List:**
    *   The last node's `next` pointer points back to the head node (or another node in the list), forming a circle.
    *   Can be singly or doubly circular.

**Advantages of Linked Lists (over Arrays/Lists):**
*   **Dynamic Size:** Can easily grow or shrink without reallocation of the entire structure (unlike static arrays, though Python lists handle this dynamically too).
*   **Efficient Insertions/Deletions (at known positions):** If you have a pointer to the node *before* the insertion/deletion point (or the node itself for deletion in doubly linked lists), these operations can be O(1). Finding the position, however, might take O(n).

**Disadvantages of Linked Lists (compared to Arrays/Lists):**
*   **No Random Access:** To access an element at a specific index `k`, you must traverse the list from the head, taking O(k) time. Arrays offer O(1) indexed access.
*   **Extra Memory for Pointers:** Each node requires additional space to store the pointer(s).
*   **Potentially Slower Traversal (Cache Inefficiency):** Nodes might be scattered in memory, leading to more cache misses compared to contiguous arrays.

**Python Implementation (Custom `Node` Class):**
LeetCode problems involving linked lists usually provide a `ListNode` class definition or expect you to use a similar one.

*   **Singly Linked List Node:**

    ```python
class ListNode:
	def __init__(self, val=0, next=None):
		self.val = val    # The data stored in the node
		self.next = next  # Pointer to the next node in the list

# Example usage:
# node1 = ListNode(1)
# node2 = ListNode(2)
# node3 = ListNode(3)
#
# node1.next = node2
# node2.next = node3
# head = node1 # head now points to the start of the list 1 -> 2 -> 3 -> None
```

*   **Doubly Linked List Node (less common in basic LeetCode but good to know):**

```python
class DoublyListNode:
	def __init__(self, val=0, next=None, prev=None):
		self.val = val
		self.next = next
		self.prev = prev
```

- We will primarily focus on **Singly Linked Lists** as they are more common in LeetCode introductions.

**Core Operations (Singly Linked List, assuming `head` points to the first node):**

1.  **Traversal (Loop over linked list):**
    *   Description: Iterate through the list, typically starting from the `head`, until you reach `None`.
    *   Time Complexity: **O(N)**, where N is the number of nodes.
    *   Space Complexity: **O(1)** (for the `current` pointer).

    ```python
def print_list(head):
	current = head
	nodes_str = []
	while current: # or while current is not None
		nodes_str.append(str(current.val))
		current = current.next
	print(" -> ".join(nodes_str) + " -> None")

# Example:
# head = ListNode(1, ListNode(2, ListNode(3)))
# print_list(head) # Output: 1 -> 2 -> 3 -> None
 ```

2.  **Find a node (by value):**
    *   Description: Traverse the list to find the first node containing a specific value.
    *   Time Complexity: **O(N)** (worst case, if value is last or not present).
    *   Space Complexity: **O(1)**.

    ```python
def find_node(head, target_val):
	current = head
	while current:
		if current.val == target_val:
				return current # Return the node itself
		current = current.next
	return None # Value not found

# node_found = find_node(head, 2)
# if node_found:
#     print(f"Found node with value: {node_found.val}")
```

3.  **Insert a node:**
    *  At the beginning (new head):**
        *   Time Complexity: **O(1)**
        *   Space Complexity: O(1) (for the new node).

        ```python
def insert_at_beginning(head, val_to_insert):
	new_node = ListNode(val_to_insert)
	new_node.next = head
	return new_node # The new_node is now the head

# head = ListNode(2, ListNode(3))
# head = insert_at_beginning(head, 1) # head is now 1 -> 2 -> 3 -> None
# print_list(head)
        ```

    *   **b) At the end:**
        *   Time Complexity: **O(N)** (must traverse to find the last node). If you maintain a `tail` pointer, it becomes O(1).
        *   Space Complexity: O(1) (for the new node).
  
    ```python
def insert_at_end(head, val_to_insert):
	new_node = ListNode(val_to_insert)
	if not head: # If list is empty
		return new_node
	current = head
	while current.next: # Traverse to the last node
		current = current.next
	current.next = new_node
	return head

# head = ListNode(1, ListNode(2))
# head = insert_at_end(head, 3) # head is 1 -> 2 -> 3 -> None
# print_list(head)
```

    * **After a given node (if you have a pointer to that node `prev_node`):**
        *   Time Complexity: **O(1)**
        *   Space Complexity: O(1).

        ```python
def insert_after_node(prev_node, val_to_insert):
	if not prev_node:
		print("Previous node cannot be None")
		return
	new_node = ListNode(val_to_insert)
	new_node.next = prev_node.next
	prev_node.next = new_node

# node1 = ListNode(1)
# node3 = ListNode(3)
# node1.next = node3
# head = node1 # 1 -> 3 -> None
# insert_after_node(node1, 2) # Insert 2 after node1
# print_list(head) # Output: 1 -> 2 -> 3 -> None
```

4.  **Remove a node:**
    *  **Removing the head node:**
        *   Time Complexity: **O(1)**

        ```python
def remove_head(head):
	if not head:
		return None
	new_head = head.next
	head.next = None # Optional: Disconnect old head
	return new_head

# head = ListNode(1, ListNode(2, ListNode(3)))
# head = remove_head(head)
# print_list(head) # Output: 2 -> 3 -> None
```

    * **Removing a node with a given key (value):**
        *   Time Complexity: **O(N)** (to find the node and its predecessor).
        *   Space Complexity: O(1).

        ```python
def remove_node_by_key(head, key_to_remove):
	if not head:
		return None

	# If head itself holds the key
	if head.val == key_to_remove:
		return head.next

	current = head
	# Search for the node to be deleted, keep track of the previous node
	while current.next:
		if current.next.val == key_to_remove:
			node_to_remove = current.next
			current.next = node_to_remove.next # Unlink the node
			node_to_remove.next = None # Optional: Disconnect removed node
			return head
		current = current.next
	return head # Key not found

# head = ListNode(1, ListNode(2, ListNode(3, ListNode(4))))
# head = remove_node_by_key(head, 3)
# print_list(head) # Output: 1 -> 2 -> 4 -> None
# head = remove_node_by_key(head, 1)
# print_list(head) # Output: 2 -> 4 -> None
```

    *   **c) Removing a node at a given position/index (0-based):**
        *   Time Complexity: **O(N)** (to reach the position).
  
        ```python
def remove_at_position(head, position):
	if not head:
		return None
	if position == 0:
		return head.next

	current = head
	count = 0
	# Find predecessor of the node to be deleted
	while current and count < position - 1:
		current = current.next
		count += 1

	# If position is out of bounds or list is too short
	if not current or not current.next:
		return head

	node_to_remove = current.next
	current.next = node_to_remove.next
	node_to_remove.next = None # Optional
	return head
```

5.  **Update a node's value:**
    *   If you have a pointer to the node:
        *   Time Complexity: **O(1)**
    *   If you need to find the node by value/position first:
        *   Time Complexity: **O(N)**

    ```python
def update_node_value(node_to_update, new_val):
		if node_to_update:
				node_to_update.val = new_val

# head = ListNode(1, ListNode(2, ListNode(3)))
# node_to_change = find_node(head, 2)
# update_node_value(node_to_change, 200)
# print_list(head) # Output: 1 -> 200 -> 3 -> None
```

6.  **Reverse a linked list:** (Common LeetCode problem, e.g., #206)
    *   Iterative Approach: Use three pointers: `prev`, `current`, `next_node`.
    *   Time Complexity: **O(N)**
    *   Space Complexity: **O(1)**

    ```python
def reverse_list_iterative(head):
	prev_node = None
	current_node = head
	while current_node:
		next_node_temp = current_node.next # Store next node
		current_node.next = prev_node      # Reverse current node's pointer
		prev_node = current_node           # Move prev one step forward
		current_node = next_node_temp      # Move current one step forward
	return prev_node # prev_node will be the new head

# head = ListNode(1, ListNode(2, ListNode(3)))
# reversed_head = reverse_list_iterative(head)
# print_list(reversed_head) # Output: 3 -> 2 -> 1 -> None
```

    *   Recursive Approach:
    *   Time Complexity: **O(N)**
    *   Space Complexity: **O(N)** (due to recursion call stack).

    ```python
def reverse_list_recursive(head):
	if not head or not head.next: # Base case: empty list or single node
		return head

	# Recursively reverse the rest of the list
	reversed_tail = reverse_list_recursive(head.next)

	# head is now the last node of the original sub-list (e.g., if list was 1->2->3,
	# and we called with head=1, reversed_tail would be 3->2. head.next is 2)
	head.next.next = head # Make the original next node (2) point back to current head (1)
	head.next = None      # Set current head's next to None (it's the new tail)

	return reversed_tail # The head of the fully reversed list
   ```

7.  **Swap two nodes (not just values):**
    *   This is more complex as it involves careful pointer manipulation of up to 4 nodes (the two nodes to be swapped and their predecessors).
    *   Handling edge cases (nodes are head, adjacent, etc.) is tricky.
    *   Time Complexity: O(N) to find the nodes, then O(1) for swapping if pointers are known.

**Common LeetCode Patterns with Linked Lists:**

*   **Dummy/Sentinel Node:**
    *   A placeholder node often inserted *before* the actual head of the list.
    *   Simplifies edge cases, especially when modifying the head of the list (e.g., insertions/deletions at the beginning). The dummy node's `next` pointer always points to the true head.
    *   You return `dummy.next` at the end.

    ```python
    # Example of using a dummy node for insertion at head
    # def insert_at_beginning_with_dummy(head, val_to_insert):
    #     dummy = ListNode(0) # Or any value, it's just a placeholder
    #     dummy.next = head
    #     new_node = ListNode(val_to_insert)
    #     new_node.next = dummy.next # Points to old head
    #     dummy.next = new_node    # Dummy points to new head
    #     return dummy.next
    ```

*   **Two Pointers:** A very common technique.
    *   **Fast and Slow Pointers:**
        *   `slow` moves one step at a time (`slow = slow.next`).
        *   `fast` moves two steps at a time (`fast = fast.next.next`).
        *   **Use Cases:**
            *   **Cycle Detection (Floyd's Tortoise and Hare):** If there's a cycle, `fast` and `slow` will eventually meet. (LeetCode #141)
            *   **Finding the Middle Node:** When `fast` reaches the end, `slow` will be at (or near) the middle. (LeetCode #876)
    *   **Other Two-Pointer Scenarios:**
        *   One pointer to `current`, another to `previous` (e.g., in reversal).
        *   Two pointers starting at different positions and moving towards each other or in the same direction with a fixed gap.

**Pythonic Tips & Common Pitfalls for Linked Lists:**
*   **`None` Checks:** Always be vigilant about checking for `None` before accessing `node.next` or `node.val` to avoid `AttributeError`.
*   **Losing the Head:** Be careful not to lose the reference to the `head` of the list if you're modifying it, especially if you're not using a dummy node.
*   **Pointer Assignments:** Understand that `a = b` for nodes means `a` now refers to the same node object as `b`. Changing `a.next` will also change `b.next` if they point to the same object.
*   **Edge Cases:**
    *   Empty list (`head` is `None`).
    *   Single-node list.
    *   Operations at the head or tail of the list.
*   **Visualizing:** Drawing out the nodes and pointers on paper can be extremely helpful when working through linked list problems, especially for reversal or complex swaps.
*   When a problem statement says "Given the `head` of a linked list...", your function will receive this `head` node as an argument.

---
Linked lists are a foundational topic. Practice the core operations, especially reversal and problems involving two pointers, as they form the basis for many more complex linked list questions on LeetCode.

## References


