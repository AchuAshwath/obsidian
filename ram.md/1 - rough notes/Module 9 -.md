07-05-2025 09:10:27

Status :

Tags :

# Module - 9

````

# Module 9: Union-Find (Disjoint Set Union - DSU)

**Concept:**
*   The Union-Find (or Disjoint Set Union - DSU) data structure is designed to efficiently manage a collection of elements partitioned into a number of **disjoint (non-overlapping) sets**.
*   It's particularly useful for problems where you need to:
    1.  Determine if two elements belong to the same set.
    2.  Merge two sets into a single set.
*   Think of it as managing groups or connected components. Initially, each element might be in its own group. As you process relationships (e.g., edges in a graph), you "union" or merge the groups of connected elements.

**Core Operations:**

1.  **`make_set(element)` (Implicitly done during initialization):**
    *   Creates a new set containing only the given `element`.
    *   In most implementations, this means initializing the `element` to be its own parent (representing a set of size 1).

2.  **`find(element)`:**
    *   Returns a **representative** (often called the "root" or "leader") of the set to which `element` belongs.
    *   If `find(element1) == find(element2)`, then `element1` and `element2` are in the same set.
    *   This operation is key to checking connectivity.

3.  **`union(element1, element2)` (or `unite`):**
    *   Merges the set containing `element1` with the set containing `element2` into a single set.
    *   If they are already in the same set, this operation typically does nothing.

**Python Implementation:**
The most common way to implement Union-Find is using an array (or list) called `parent`.
*   `parent[i]` stores the parent of element `i`.
*   If `parent[i] == i`, then `i` is the representative (root) of its set.

```python
class UnionFind:
    def __init__(self, n):
        """
        Initializes the Union-Find structure for 'n' elements (0 to n-1).
        Each element initially belongs to its own set.
        """
        # parent[i] stores the parent of element i.
        # Initially, each element is its own parent.
        self.parent = list(range(n))
        # OPTIONAL: For Union by Rank/Size optimization
        # self.rank = [0] * n  # For union by rank (tree height)
        self.num_components = n # Keep track of number of disjoint sets
        self.size = [1] * n # For union by size (number of elements in set)


    def find(self, i):
        """
        Finds the representative (root) of the set containing element 'i'.
        Implements Path Compression optimization.
        """
        if self.parent[i] == i: # If i is its own parent, it's the root
            return i
        # Path Compression: Make all nodes on the path point directly to the root
        self.parent[i] = self.find(self.parent[i])
        return self.parent[i]

    def union(self, i, j):
        """
        Merges the set containing element 'i' with the set containing element 'j'.
        Implements Union by Size (or Rank) optimization.
        Returns True if a merge happened, False if they were already in the same set.
        """
        root_i = self.find(i)
        root_j = self.find(j)

        if root_i != root_j: # Only union if they are in different sets
            # Union by Size: Attach smaller tree under root of larger tree
            if self.size[root_i] < self.size[root_j]:
                self.parent[root_i] = root_j
                self.size[root_j] += self.size[root_i]
            else: # self.size[root_i] >= self.size[root_j]
                self.parent[root_j] = root_i
                self.size[root_i] += self.size[root_j]
            
            # # OPTIONAL: Union by Rank (alternative to Union by Size)
            # if self.rank[root_i] < self.rank[root_j]:
            #     self.parent[root_i] = root_j
            # elif self.rank[root_i] > self.rank[root_j]:
            #     self.parent[root_j] = root_i
            # else: # Ranks are equal, make one the parent and increment its rank
            #     self.parent[root_j] = root_i
            #     self.rank[root_i] += 1
            
            self.num_components -= 1 # A merge occurred, so one less component
            return True
        return False # i and j were already in the same set

    def is_connected(self, i, j):
        """Checks if elements i and j are in the same set."""
        return self.find(i) == self.find(j)

    def get_num_components(self):
        """Returns the current number of disjoint sets."""
        return self.num_components

# Example Usage:
# uf = UnionFind(5) # For elements 0, 1, 2, 3, 4
# print(f"Initial components: {uf.get_num_components()}") # Output: 5

# uf.union(0, 1)
# print(f"Components after union(0,1): {uf.get_num_components()}") # Output: 4
# print(f"0 and 1 connected? {uf.is_connected(0, 1)}")      # Output: True

# uf.union(2, 3)
# print(f"Components after union(2,3): {uf.get_num_components()}") # Output: 3
# print(f"0 and 2 connected? {uf.is_connected(0, 2)}")      # Output: False

# uf.union(0, 2) # Merges the set {0,1} with {2,3}
# print(f"Components after union(0,2): {uf.get_num_components()}") # Output: 2
# print(f"0 and 3 connected? {uf.is_connected(0, 3)}")      # Output: True
# print(f"Parent array: {uf.parent}") # Example: [0, 0, 0, 2, 4] or similar after path compression
# print(f"Size array: {uf.size}")     # Example: [4, 1, 1, 1, 1] (size of root_i or root_j is updated)
````

IGNORE_WHEN_COPYING_START

Use code [with caution](https://support.google.com/legal/answer/13505487). Markdown

IGNORE_WHEN_COPYING_END

**Optimizations (Crucial for Performance):**

1. **Path Compression:**
    
    - **Idea:** When performing a find(i) operation, after finding the root r of the set containing i, make all nodes on the path from i to r point directly to r.
        
    - **Effect:** This flattens the tree structure significantly, making future find operations for these nodes (and their descendants) much faster (closer to O(1)).
        
    - **Implementation:** Achieved by the recursive line self.parent[i] = self.find(self.parent[i]) in the find method.
        
2. **Union by Rank (or Union by Height):**
    
    - **Idea:** When merging two sets (trees), attach the root of the tree with a smaller "rank" (an upper bound on its height) to the root of the tree with a larger rank. If ranks are equal, arbitrarily choose one as the parent and increment its rank.
        
    - **Effect:** Helps keep the trees relatively shallow, preventing them from becoming long chains (which would degrade find performance).
        
3. **Union by Size:**
    
    - **Idea:** Similar to Union by Rank, but instead of rank, use the "size" (number of elements) of the sets. Attach the root of the smaller set (by size) to the root of the larger set. Update the size of the new root.
        
    - **Effect:** Also helps keep trees shallow. Often simpler to implement and performs just as well in practice as Union by Rank.
        
    - **Implementation:** The example code uses Union by Size.
        

**Time Complexity (with Path Compression AND Union by Rank/Size):**

- For a sequence of M union or find operations on N elements:
    
    - The amortized time complexity per operation is **O(α(N))**, where α(N) is the **inverse Ackermann function**.
        
    - The inverse Ackermann function grows extremely slowly. For all practical values of N (even astronomically large numbers), α(N) is less than 5.
        
    - Therefore, these operations are **effectively almost constant time on average**.
        
- Without these optimizations:
    
    - A naive find could take O(N) (if the tree is a linked list).
        
    - A sequence of naive union operations could create such skewed trees.
        

**Key LeetCode Use Cases for Union-Find:**

1. **Detecting Cycles in an Undirected Graph:**
    
    - Iterate through the edges (u, v) of the graph.
        
    - For each edge, if find(u) == find(v), then u and v are already in the same connected component, and adding this edge would form a cycle.
        
    - Otherwise, union(u, v).
        
    - (e.g., LeetCode #261. Graph Valid Tree, #684. Redundant Connection)
        
2. **Finding/Counting Connected Components:**
    
    - Initialize Union-Find with N elements (each in its own set).
        
    - Iterate through edges (u, v) and perform union(u, v).
        
    - The number of distinct roots (or a separate counter decremented on successful unions) gives the number of connected components.
        
    - (e.g., LeetCode #323. Number of Connected Components in an Undirected Graph, #547. Number of Provinces)
        
3. **Kruskal's Algorithm for Minimum Spanning Tree (MST):**
    
    - Sort all edges by weight in ascending order.
        
    - Iterate through sorted edges (u, v, weight).
        
    - If find(u) != find(v), add the edge to the MST and perform union(u, v).
        
    - Stop when V-1 edges are added to the MST.
        
4. **Equivalence Relation Problems / Grouping:**
    
    - When you need to determine if items are equivalent based on a series of direct equivalences, and then group them.
        
    - (e.g., LeetCode #990. Satisfiability of Equality Equations, #721. Accounts Merge)
        
5. **Percolation Problems (Grid-based):**
    
    - Simulating flow or connectivity in a grid. Union-Find can track connected open sites.
        

**Pythonic Tips & Common Pitfalls for Union-Find:**

- **0-Indexed vs. 1-Indexed Elements:** Be careful if problem elements are 1-indexed. You might need to adjust them for a 0-indexed parent array or make your parent array one size larger.
    
- **Initialization:** Ensure every element is initially its own parent. The self.parent = list(range(n)) is a clean way for 0-indexed elements.
    
- **Path Compression in find:** This is the most critical optimization for performance. Make sure it's implemented correctly (the recursive update to self.parent[i]).
    
- **Union by Rank/Size in union:** Also essential. Choose one (size is often slightly simpler) and implement it correctly to update the parent of the smaller component's root.
    
- **Counting Components:** The num_components variable, decremented on successful unions, is a clean way to track this. Alternatively, after all unions, you can count distinct roots by iterating through self.parent and calling find(i) for each element i, then adding find(i) to a set to count unique representatives.
    

---

Union-Find is a specialized but very powerful tool. When a problem involves grouping elements, checking connectivity dynamically, or finding components, consider if Union-Find is applicable. Its near-constant time operations (amortized) make it extremely efficient for these tasks.

This concludes our detailed pre-requisite modules! You now have a comprehensive foundation covering essential Python features, core data structures, and some key algorithmic tools like Union-Find.

## References


