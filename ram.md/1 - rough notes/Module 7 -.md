07-05-2025 08:56:15

Status :

Tags :

# Module 7 -

````
# Module 7: Graphs (Conceptual, Representation & Basic Traversal)

**Concept: What is a Graph?**
*   A graph `G = (V, E)` is a data structure consisting of:
    *   `V`: A set of **vertices** (or **nodes**). These represent the objects or entities.
    *   `E`: A set of **edges**. These represent the relationships or connections between pairs of vertices.
*   Unlike trees, graphs can have:
    *   **Cycles:** Paths that start and end at the same vertex.
    *   **Disconnected Components:** Multiple independent subgraphs within the larger graph.
    *   No designated "root" node (unless specified by the problem context, like in a rooted tree which is a special type of graph).

**Types of Graphs:**

1.  **Undirected Graph:**
    *   Edges have no direction. An edge `(u, v)` means `u` is connected to `v`, and `v` is connected to `u`.
    *   Example: A social network where friendships are mutual.

2.  **Directed Graph (Digraph):**
    *   Edges have a direction. An edge `(u, v)` means there's a connection from `u` to `v`, but not necessarily from `v` to `u`.
    *   Example: A web page linking to another, or a dependency graph where task `u` must be completed before task `v`.

3.  **Weighted Graph:**
    *   Each edge has an associated numerical **weight** or **cost**.
    *   Example: A road network where edges are roads and weights are distances or travel times. Can be directed or undirected.

4.  **Unweighted Graph:**
    *   Edges do not have weights. Often treated as if all edges have a weight of 1.

**Graph Terminology:**
*   **Vertex (Node):** An individual element in the graph.
*   **Edge (Arc, Link):** A connection between two vertices.
*   **Adjacent Vertices (Neighbors):** Two vertices are adjacent if there's an edge connecting them.
*   **Degree of a Vertex (Undirected Graph):** The number of edges incident to it.
*   **In-degree of a Vertex (Directed Graph):** The number of edges pointing *to* it.
*   **Out-degree of a Vertex (Directed Graph):** The number of edges pointing *from* it.
*   **Path:** A sequence of vertices where each adjacent pair in the sequence is connected by an edge.
*   **Cycle:** A path that starts and ends at the same vertex, and contains at least one edge.
*   **Connected Graph (Undirected):** There is a path between every pair of distinct vertices.
*   **Disconnected Graph:** A graph that is not connected; it consists of multiple **connected components**.
*   **Strongly Connected Graph (Directed):** There is a directed path from any vertex to any other vertex.
*   **Weakly Connected Graph (Directed):** The underlying undirected graph (ignoring edge directions) is connected.
*   **Subgraph:** A graph whose vertices and edges are subsets of another graph.

**Python Implementation (Representations):**
Choosing the right representation is key for efficiency.

1.  **Adjacency List (Most Common for LeetCode):**
    *   **Description:** For each vertex, store a list (or set) of its adjacent vertices.
    *   **Implementation:** Often a dictionary where keys are vertices and values are lists (or sets) of their neighbors. For N-ary trees or general graphs where nodes might be integers 0 to N-1, a list of lists can also be used: `adj[i]` is a list of neighbors of node `i`.
    *   **Pros:**
        *   Space-efficient for **sparse graphs** (graphs with relatively few edges compared to the number of possible edges, i.e., |E| is much smaller than |V|²). Space complexity: O(V + E).
        *   Efficiently find all neighbors of a vertex: O(degree(v)).
        *   Efficiently add/remove edges (if using dynamic lists/sets for neighbors).
    *   **Cons:**
        *   Checking if an edge `(u, v)` exists can take O(degree(u)) time (scan `u`'s neighbor list).
    ```python
    # Using a dictionary (good for arbitrary node labels like strings or non-sequential ints)
    from collections import defaultdict

    adj_list_dict = defaultdict(list) # Or defaultdict(set) for unique neighbors and O(1) neighbor check

    def add_edge_dict(u, v, is_directed=False):
        adj_list_dict[u].append(v)
        if not is_directed:
            adj_list_dict[v].append(u) # For undirected graph

    add_edge_dict('A', 'B')
    add_edge_dict('A', 'C')
    add_edge_dict('B', 'D')
    # adj_list_dict: defaultdict(<class 'list'>, {'A': ['B', 'C'], 'B': ['A', 'D'], 'C': ['A'], 'D': ['B']}) (if undirected)

    # Using a list of lists (good if vertices are integers 0 to N-1)
    num_vertices = 4
    adj_list_list = [[] for _ in range(num_vertices)] # Or [defaultdict(int) for _ in range(num_vertices)] for weighted

    def add_edge_list(u, v, is_directed=False): # u, v are 0-indexed integers
        adj_list_list[u].append(v)
        if not is_directed:
            adj_list_list[v].append(u)

    add_edge_list(0, 1)
    add_edge_list(0, 2)
    add_edge_list(1, 3)
    # adj_list_list: [[1, 2], [0, 3], [0], [1]] (if undirected)
    ```

2.  **Adjacency Matrix:**
    *   **Description:** A 2D matrix (e.g., list of lists) `adj_matrix[V][V]` where `adj_matrix[u][v] = 1` (or the weight of the edge) if an edge exists from `u` to `v`, and `0` (or infinity for weights) otherwise.
    *   **Pros:**
        *   Efficiently check if an edge `(u, v)` exists: O(1).
        *   Conceptually simpler for dense graphs.
    *   **Cons:**
        *   Space complexity: **O(V²)**, which is inefficient for sparse graphs.
        *   Finding all neighbors of a vertex takes O(V) time (scan a whole row).
        *   Adding/removing a vertex is expensive (matrix needs resizing).
    ```python
    num_vertices_mat = 3
    # Unweighted graph
    adj_matrix = [[0 for _ in range(num_vertices_mat)] for _ in range(num_vertices_mat)]

    def add_edge_matrix(u, v, is_directed=False, weight=1):
        adj_matrix[u][v] = weight
        if not is_directed:
            adj_matrix[v][u] = weight

    add_edge_matrix(0, 1)
    add_edge_matrix(1, 2)
    # adj_matrix (undirected, weight 1):
    # [[0, 1, 0],
    #  [1, 0, 1],
    #  [0, 1, 0]]
    ```

3.  **Edge List:**
    *   **Description:** A simple list of all edges in the graph. Each edge can be represented as a tuple `(u, v)` or `(u, v, weight)`.
    *   **Pros:**
        *   Very simple representation.
        *   Space complexity: O(E).
        *   Often how graph input is given in LeetCode problems.
    *   **Cons:**
        *   Most operations (finding neighbors, checking for an edge) require iterating through the entire edge list, which is O(E).
        *   Typically converted to an Adjacency List or Matrix for efficient processing.
    ```python
    edge_list = [('A', 'B'), ('A', 'C'), ('B', 'D')]
    weighted_edge_list = [(0, 1, 10), (1, 2, 5), (0, 2, 20)] # (u, v, weight)
    ```

**Core Graph Operations & Traversal Algorithms:**
Traversal algorithms are fundamental for exploring graphs.

**Building Adjacency List (from Edge List input - common in LeetCode):**
```python
def build_adj_list(edges, num_nodes, is_directed=False):
    adj = defaultdict(list) # Or [[] for _ in range(num_nodes)] if nodes are 0 to num_nodes-1
    for u, v in edges:
        adj[u].append(v)
        if not is_directed:
            adj[v].append(u)
    return adj

# edges_input = [[0,1], [0,2], [1,3], [2,3]]
# num_nodes_input = 4
# graph_adj = build_adj_list(edges_input, num_nodes_input)
# print(graph_adj)
# Output: defaultdict(<class 'list'>, {0: [1, 2], 1: [0, 3], 2: [0, 3], 3: [1, 2]})
````

IGNORE_WHEN_COPYING_START

Use code [with caution](https://support.google.com/legal/answer/13505487). Markdown

IGNORE_WHEN_COPYING_END

**1. Depth-First Search (DFS):**

- **Concept:** Explores as far as possible along each branch before backtracking. Uses a **stack** (implicitly via recursion, or explicitly with an iterative approach).
    
- **Algorithm Outline (Recursive):**
    
    1. Mark current node u as visited.
        
    2. Process node u (e.g., add to a path, check a property).
        
    3. For each unvisited neighbor v of u:
        
        - Recursively call DFS on v.
            
- **Algorithm Outline (Iterative):**
    
    1. Initialize a stack and push the starting node s.
        
    2. Initialize a visited set.
        
    3. While stack is not empty:
        
        - Pop a node u from stack.
            
        - If u has not been visited:
            
            - Mark u as visited.
                
            - Process u.
                
            - For each neighbor v of u:
                
                - If v has not been visited, push v onto stack.
                    
- **Time Complexity: O(V + E)** (Each vertex and edge is visited at most once/twice).
    
- **Space Complexity: O(V)** (For visited set and recursion stack/explicit stack in worst case - e.g., a path graph).
    

      `# Recursive DFS def dfs_recursive(graph, start_node, visited=None):     if visited is None:         visited = set() # Keep track of visited nodes      visited.add(start_node)     print(start_node, end=" ") # Process node      for neighbor in graph.get(start_node, []): # Use .get for defaultdict or dict         if neighbor not in visited:             dfs_recursive(graph, neighbor, visited)  # Iterative DFS def dfs_iterative(graph, start_node):     visited = set()     stack = [start_node]     result_path = []      while stack:         node = stack.pop()         if node not in visited:             visited.add(node)             result_path.append(node) # Process node             # Add unvisited neighbors to stack. Order might matter for path reconstruction.             # Adding in reverse order of how you want them processed (due to LIFO)             # For example, if graph[node] is [neighbor1, neighbor2], stack.extend([neighbor2, neighbor1])             # will process neighbor1 first.             for neighbor in reversed(graph.get(node, [])): # Process earlier neighbors first                 if neighbor not in visited:                     stack.append(neighbor)     print("DFS Path (Iterative):", result_path)  # Example usage with graph_adj from above # print("DFS Path (Recursive):", end=" ") # dfs_recursive(graph_adj, 0) # Example: 0 1 3 2 (path can vary based on neighbor order) # print() # dfs_iterative(graph_adj, 0)`
    

IGNORE_WHEN_COPYING_START

Use code [with caution](https://support.google.com/legal/answer/13505487). Python

IGNORE_WHEN_COPYING_END

**2. Breadth-First Search (BFS):**

- **Concept:** Explores all neighbors at the present depth level before moving on to nodes at the next depth level. Uses a **queue**.
    
- **Algorithm Outline:**
    
    1. Initialize a queue and enqueue the starting node s.
        
    2. Initialize a visited set and add s to it.
        
    3. While queue is not empty:
        
        - Dequeue a node u.
            
        - Process node u.
            
        - For each neighbor v of u:
            
            - If v has not been visited:
                
                - Mark v as visited.
                    
                - Enqueue v.
                    
- **Time Complexity: O(V + E)**
    
- **Space Complexity: O(V)** (For visited set and queue in worst case - e.g., a star graph or when a level is very wide).
    

      `from collections import deque  def bfs(graph, start_node):     visited = set()     queue = deque([start_node])     visited.add(start_node)     result_path = []      while queue:         node = queue.popleft()         result_path.append(node) # Process node          for neighbor in graph.get(node, []):             if neighbor not in visited:                 visited.add(neighbor)                 queue.append(neighbor)     print("BFS Path:", result_path)  # bfs(graph_adj, 0) # Example: [0, 1, 2, 3] (path can vary slightly based on neighbor order within a level)`
    

IGNORE_WHEN_COPYING_START

Use code [with caution](https://support.google.com/legal/answer/13505487). Python

IGNORE_WHEN_COPYING_END

**Core Graph Operations (from your initial list):**

- **Insert a node into a graph:**
    
    - Adjacency List: adj[new_node] = [] (if using dict) or ensure list is large enough.
        
    - Adjacency Matrix: Requires resizing matrix, O(V²).
        
- **Remove a node from a graph:**
    
    - Adjacency List: Remove the node as a key, and also remove it from all other nodes' adjacency lists. O(V+E) in worst case.
        
    - Adjacency Matrix: Requires zeroing out row/column, or more complex resizing.
        
- **Add an edge between two nodes:** (Shown in representation examples). O(1) for adj list (append), O(1) for adj matrix.
    
- **Find the neighbors of a node:**
    
    - Adjacency List: graph[node], O(degree(node)) to iterate, O(1) to get the list.
        
    - Adjacency Matrix: Iterate row graph[node], O(V).
        
- **Find a path between two nodes:** Use DFS or BFS. BFS finds the shortest path in terms of number of edges in unweighted graphs.
    

**Key LeetCode Use Cases for Graphs:**

- **Connectivity Problems:**
    
    - Number of connected components (LeetCode #323).
        
    - Checking if a graph is connected.
        
    - Finding if a path exists between two nodes.
        
- **Shortest Path Problems:**
    
    - BFS for unweighted graphs (e.g., shortest path in a maze - LeetCode #127 Word Ladder).
        
    - Dijkstra's Algorithm for weighted graphs with non-negative weights.
        
    - Bellman-Ford Algorithm for weighted graphs with possible negative weights (but no negative cycles).
        
- **Cycle Detection:**
    
    - In undirected graphs (using DFS and keeping track of parent).
        
    - In directed graphs (using DFS and tracking nodes in current recursion stack). (LeetCode #207 Course Schedule)
        
- **Topological Sort (for Directed Acyclic Graphs - DAGs):**
    
    - Linear ordering of vertices such that for every directed edge (u, v), vertex u comes before v in the ordering. (e.g., Kahn's algorithm (BFS-based) or DFS-based). (LeetCode #210 Course Schedule II)
        
- **Minimum Spanning Tree (MST):** Prim's algorithm, Kruskal's algorithm (less common in typical LC interviews but good to know for graph theory).
    
- **Matrix Traversal as Graphs:** Many grid/matrix problems can be modeled as graphs where cells are nodes and adjacent cells (up, down, left, right) have edges. (e.g., Number of Islands - LeetCode #200).
    

**Pythonic Tips & Common Pitfalls for Graphs:**

- **defaultdict(list) or defaultdict(set):** Extremely convenient for building adjacency lists, especially when nodes might be added dynamically or node labels are not simple 0-indexed integers.
    
- **visited Set:** Crucial for both DFS and BFS to avoid infinite loops in graphs with cycles and to prevent redundant processing.
    
- **Handling Disconnected Graphs:** If you need to process all nodes, you might need to iterate through all potential starting nodes and run DFS/BFS if they haven't been visited yet.
    
          `# visited_all = set() # for node in all_nodes_in_graph: #     if node not in visited_all: #         dfs_recursive(graph, node, visited_all) # or bfs call`
        
    
    IGNORE_WHEN_COPYING_START
    

- Use code [with caution](https://support.google.com/legal/answer/13505487). Python
    
    IGNORE_WHEN_COPYING_END
    
- **Input Format:** Pay attention to how graph input is given (edge list, adjacency matrix, etc.) and be ready to convert it to your preferred representation (usually adjacency list).
    
- **Directed vs. Undirected:** Ensure you add edges correctly based on whether the graph is directed or undirected. For undirected, if you add u -> v, you must also add v -> u.
    

---

Graphs are a rich area. Mastering DFS and BFS is the first essential step. From there, you can explore more advanced algorithms like Dijkstra's and topological sort as you encounter problems requiring them.

## References


