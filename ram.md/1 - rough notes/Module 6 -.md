07-05-2025 08:56:08

Status :

Tags :

# Module 6 -

 ````
 Module 6: Trees (Conceptual & Basic Traversal)

**Concept: What is a Tree?**
*   A **hierarchical data structure** consisting of **nodes** connected by **edges**.
*   Unlike linked lists or arrays (which are linear), trees can have branching paths.
*   Key characteristics:
    *   One node is designated as the **root** (the topmost node).
    *   Every node (except the root) has exactly one **parent** node.
    *   A node can have zero or more **child** nodes.
    *   Nodes with no children are called **leaf** nodes.
    *   There is a unique path from the root to any other node in the tree.
    *   A tree with N nodes will have N-1 edges.
    *   Trees do not contain cycles (an acyclic connected graph is a tree).

**Common Tree Terminology:**
*   **Root:** The topmost node of the tree. It has no parent.
*   **Parent:** A node that has one or more child nodes.
*   **Child:** A node that is directly connected to another node when moving away from the root.
*   **Siblings:** Nodes that share the same parent.
*   **Leaf Node (or External Node):** A node with no children.
*   **Internal Node:** A node that has at least one child.
*   **Edge:** The connection between two nodes.
*   **Path:** A sequence of nodes and edges connecting a node with a descendant.
*   **Depth of a Node:** The number of edges on the path from the root to that node. The depth of the root is 0.
*   **Height of a Node:** The number of edges on the longest path from that node to a leaf node. The height of a leaf node is 0.
*   **Height of a Tree:** The height of its root node (or equivalently, the maximum depth of any node in the tree).
*   **Level of a Node:** 1 + depth of the node. (Root is at level 1, its children at level 2, etc. Some definitions use depth = level).
*   **Subtree:** A tree consisting of a node and all its descendants.
*   **Degree of a Node:** The number of children a node has.
*   **Degree of a Tree:** The maximum degree of any node in the tree.

**Types of Trees (Common in LeetCode):**

1.  **Binary Tree (BT):**
    *   A tree in which each node has **at most two children**, referred to as the *left child* and the *right child*.
    *   This is the most common type of tree encountered in LeetCode.

2.  **Binary Search Tree (BST):**
    *   A special type of binary tree that satisfies the **BST property**:
        *   For any node `N`:
            *   All values in its **left subtree** are **less than** `N.val`.
            *   All values in its **right subtree** are **greater than** `N.val`.
        *   Both the left and right subtrees must also be binary search trees.
        *   Duplicates: Handling of duplicate values varies (e.g., always in right subtree, or not allowed). LeetCode usually implies unique values or specifies how to handle them.
    *   BSTs allow for efficient searching, insertion, and deletion (average O(log N) if balanced, O(N) worst-case if skewed).

3.  **N-ary Tree (or General Tree):**
    *   A tree where a node can have any number of children (not restricted to two).
    *   LeetCode problems might involve N-ary trees, often with nodes having a `children` attribute that is a list of child nodes.

4.  **Other specific types:**
    *   **Full Binary Tree:** Every node has either 0 or 2 children.
    *   **Complete Binary Tree:** All levels are completely filled except possibly the last level, which is filled from left to right. (Heaps are often complete binary trees).
    *   **Perfect Binary Tree:** A full binary tree where all leaf nodes are at the same depth.
    *   **Balanced Binary Tree:** A binary tree where the height difference between the left and right subtrees of any node is within a certain limit (e.g., for AVL trees, this difference is at most 1). This ensures O(log N) performance for operations.

**Python Implementation (Custom `TreeNode` Class for Binary Trees):**
LeetCode problems involving binary trees usually provide a `TreeNode` class definition or expect you to use a similar one.

```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val    # The data stored in the node
        self.left = left  # Pointer to the left child TreeNode
        self.right = right # Pointer to the right child TreeNode

# Example usage:
# root = TreeNode(1)
# root.left = TreeNode(2)
# root.right = TreeNode(3)
# root.left.left = TreeNode(4)
# root.left.right = TreeNode(5)
#
# This creates a tree:
#      1
#     / \
#    2   3
#   / \
#  4   5
````

IGNORE_WHEN_COPYING_START

Use code [with caution](https://support.google.com/legal/answer/13505487). Markdown

IGNORE_WHEN_COPYING_END

**Core Concepts/Operations (Focus on Understanding and Traversal):**

Tree problems often revolve around traversing the tree in specific orders to process nodes or gather information. Recursion is a very natural and common way to implement tree traversals.

**Tree Traversal Algorithms (O(N) Time, where N is number of nodes):**

These algorithms visit every node in the tree exactly once. The difference lies in the order nodes are visited relative to their subtrees.

1. **Depth-First Search (DFS) Traversals:** Explores as far as possible along each branch before backtracking.
    
    - **Space Complexity for DFS:** O(H) for the recursion call stack, where H is the height of the tree. In the worst case (a skewed tree resembling a linked list), H can be N, so space becomes O(N). For a balanced tree, H is O(log N).
        
    - **a) Pre-order Traversal (Root, Left, Right):**
        
        1. Visit the current node (Root).
            
        2. Recursively traverse the left subtree.
            
        3. Recursively traverse the right subtree.
            
        
        - **Use Cases:** Useful for creating a copy of the tree, or when you need to process the root before its children (e.g., expression trees where an operator is the root).
            
        
              `def preorder_traversal_recursive(root):     result = []     if root:         result.append(root.val)            # Visit Root         result.extend(preorder_traversal_recursive(root.left))  # Traverse Left         result.extend(preorder_traversal_recursive(root.right)) # Traverse Right     return result  # Iterative Pre-order (using a stack): def preorder_traversal_iterative(root):     if not root:         return []     result = []     stack = [root]     while stack:         node = stack.pop()         result.append(node.val) # Visit Root         if node.right:          # Push right child first (so left is processed first)             stack.append(node.right)         if node.left:             stack.append(node.left)     return result`
            
        
        IGNORE_WHEN_COPYING_START
        

- Use code [with caution](https://support.google.com/legal/answer/13505487). Python
    
    IGNORE_WHEN_COPYING_END
    
- **b) In-order Traversal (Left, Root, Right):**
    
    1. Recursively traverse the left subtree.
        
    2. Visit the current node (Root).
        
    3. Recursively traverse the right subtree.
        
    
    - **Use Cases:** For Binary Search Trees (BSTs), an in-order traversal visits nodes in non-decreasing (sorted) order. This is a key property.
        
    
          `def inorder_traversal_recursive(root):     result = []     if root:         result.extend(inorder_traversal_recursive(root.left)) # Traverse Left         result.append(root.val)           # Visit Root         result.extend(inorder_traversal_recursive(root.right))# Traverse Right     return result  # Iterative In-order (using a stack): def inorder_traversal_iterative(root):     result = []     stack = []     current = root     while current or stack:         while current: # Go as left as possible             stack.append(current)             current = current.left         # Current is None, pop from stack (this is the node to visit)         current = stack.pop()         result.append(current.val) # Visit Root         current = current.right    # Move to right subtree     return result`
        
    
    IGNORE_WHEN_COPYING_START
    - Use code [with caution](https://support.google.com/legal/answer/13505487). Python
    
    IGNORE_WHEN_COPYING_END
    
- **c) Post-order Traversal (Left, Right, Root):**
    
    1. Recursively traverse the left subtree.
        
    2. Recursively traverse the right subtree.
        
    3. Visit the current node (Root).
        
    
    - **Use Cases:** Useful for deleting nodes in a tree (you delete children before the parent), or for evaluating expression trees where operands are processed before the operator.
        
    
          `def postorder_traversal_recursive(root):     result = []     if root:         result.extend(postorder_traversal_recursive(root.left))  # Traverse Left         result.extend(postorder_traversal_recursive(root.right)) # Traverse Right         result.append(root.val)            # Visit Root     return result  # Iterative Post-order (using two stacks, or one stack with modifications): # Method 1: Using two stacks (simpler to understand) def postorder_traversal_iterative_two_stacks(root):     if not root:         return []     s1 = [root]     s2 = [] # This will store the post-order sequence in reverse     result = []     while s1:         node = s1.pop()         s2.append(node.val) # Add to s2 (effectively "visiting" the root for s2's order)         if node.left:             s1.append(node.left)         if node.right:             s1.append(node.right)     while s2: # Pop from s2 to get correct post-order         result.append(s2.pop())     return result  # Method 2: Using one stack (more complex) def postorder_traversal_iterative_one_stack(root):     if not root: return []     result = []     stack = []     current = root     last_visited = None     while current or stack:         while current:             stack.append(current)             current = current.left         peek_node = stack[-1]         # If right child exists and hasn't been visited yet         if peek_node.right and peek_node.right != last_visited:             current = peek_node.right         else:             # No right child, or right child already visited             result.append(peek_node.val)             last_visited = stack.pop()     return result`
        
    
    IGNORE_WHEN_COPYING_START
    - - Use code [with caution](https://support.google.com/legal/answer/13505487). Python
        
        IGNORE_WHEN_COPYING_END
        
- **Breadth-First Search (BFS) / Level-Order Traversal:**
    
    - Visits nodes level by level, from left to right within each level.
        
    - Implemented using a **queue**.
        
    - **Space Complexity for BFS:** O(W), where W is the maximum width of the tree (the maximum number of nodes at any single level). In the worst case (a "bushy" tree), W can be close to N.
        
    
          `from collections import deque  def level_order_traversal(root):     if not root:         return []      result = []     queue = deque([root])      while queue:         level_size = len(queue) # Number of nodes at the current level         current_level_nodes = []         for _ in range(level_size):             node = queue.popleft()             current_level_nodes.append(node.val)             if node.left:                 queue.append(node.left)             if node.right:                 queue.append(node.right)         result.append(current_level_nodes) # Add list of nodes for current level     return result  # Example tree: #      1 #     / \ #    2   3 #   / \   \ #  4   5   7 # root = TreeNode(1, TreeNode(2, TreeNode(4), TreeNode(5)), TreeNode(3, None, TreeNode(7))) # print(level_order_traversal(root)) # Output: [[1], [2, 3], [4, 5, 7]]`
        
    
    IGNORE_WHEN_COPYING_START
    

1. Use code [with caution](https://support.google.com/legal/answer/13505487). Python
    
    IGNORE_WHEN_COPYING_END
    

**Key LeetCode Use Cases for Trees:**

- **Validating Tree Properties:** Is it a BST? Is it balanced? Is it symmetric?
    
- **Path Sum Problems:** Find if a path from root to leaf sums to a target value, find all such paths, find max path sum.
    
- **Lowest Common Ancestor (LCA):** Find the lowest node that has two given nodes as descendants.
    
- **Tree Construction:** Build a tree from its pre-order/in-order traversal, or post-order/in-order traversal.
    
- **Serialization/Deserialization:** Convert a tree to a string representation and back.
    
- **View Problems:** Right side view, boundary view.
    
- Problems involving diameters, depths, heights.
    
- Trie data structure (a specialized tree for string prefix searching) is also common.
    

**Pythonic Tips & Common Pitfalls for Trees:**

- **Recursion is your friend:** Many tree problems have elegant recursive solutions. Clearly define your base case(s) and recursive step(s).
    
- **Helper Functions for Recursion:** Often, the main function signature given by LeetCode isn't ideal for recursion. You might define a helper function that takes additional parameters (like current path sum, current depth).
    
- **None Checks:** Always check if a node (especially root, node.left, node.right) is None before trying to access its attributes (.val, .left, .right) to avoid AttributeError.
    
- **Base Cases in Recursion:**
    
    - if not root: return ... is a very common base case. What you return depends on the problem (e.g., 0 for sum, True/False for validation, [] for list of values).
        
- **Passing State in Recursion:**
    
    - If you need to accumulate results (like a list of node values), you can pass the accumulator (e.g., a list) as an argument to the recursive function.
        
    - Alternatively, recursive functions can return values that are then combined by the caller.
        
- **Iterative vs. Recursive Traversals:** While recursion is often more intuitive for DFS, iterative solutions using a stack (for DFS) or queue (for BFS) are important to know, especially if recursion depth becomes an issue or if the iterative logic is cleaner for a specific problem.
    

---

Trees are a vast topic. This module covers the basics, focusing on binary trees and fundamental traversals. Mastering these traversals is essential as they form the building blocks for solving many tree-based LeetCode problems.


## References


