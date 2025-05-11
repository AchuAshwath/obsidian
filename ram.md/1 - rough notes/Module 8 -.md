07-05-2025 08:56:23

Status :

Tags :

# Module 8 -

Great! Let's proceed to the final pre-requisite module, **Module 8: Sorted Order Structures & `bisect` (Binary Search Precursor)**. This module focuses on how to efficiently work with sorted data in Python, primarily using sorted lists in conjunction with the `bisect` module. This is a key foundation for understanding and implementing binary search and related algorithms.

# Module 8: Sorted Order Structures & `bisect` (Binary Search Precursor)

**Concept: Importance of Sorted Order**
When data is sorted, many operations can be performed much more efficiently than on unsorted data. The most notable is **searching**, which can be done in logarithmic time (O(log N)) using binary search, compared to linear time (O(N)) for unsorted data. Maintaining sorted order is also crucial for certain types of range queries or finding elements relative to others (e.g., "find the smallest element greater than x").

**Python Implementation for Maintaining Sorted Order:**

1.  **Sorted Python `list` + `bisect` module:**
    *   This is the most common and standard Python approach for LeetCode when you need the functionalities discussed here.
    *   You maintain a Python `list` in sorted order.
    *   The `bisect` module provides functions for efficiently finding insertion points and inserting items into a sorted list while maintaining its sorted order.
    *   **Note:** While `bisect.insort` helps maintain order, the actual insertion into a Python list can still be O(N) in the worst case because it might require shifting elements. Searches (`bisect_left`, `bisect_right`) are O(log N).

2.  **Advanced (External Libraries - Generally NOT for standard LeetCode):**
    *   Libraries like `sortedcontainers` offer a `SortedList` data structure. This provides O(log N) performance for additions, deletions, and lookups, making it more like Java's `TreeSet`/`TreeMap` or C++'s `std::set`/`std::map`.
    *   However, `sortedcontainers` is an external library and **not available by default in LeetCode environments**. You should rely on `list` + `bisect` for problems solvable with this approach within LeetCode's standard library constraints.

**The `bisect` Module:**
The `bisect` module provides support for maintaining a list in sorted order without having to sort the list after each insertion. It uses a binary search algorithm internally.

**Key `bisect` Module Functions (for a *pre-sorted* list `arr`):**
Assume `arr` is already sorted in non-decreasing order.

1.  **`bisect.bisect_left(arr, x, lo=0, hi=len(arr))`:**
    *   **Description:** Returns an *insertion point* `i` for `x` in `arr` to maintain sorted order. If `x` is already present in `arr`, the insertion point will be **before (to the left of)** any existing entries of `x`.
    *   More formally, it returns `i` such that all `e` in `arr[lo:i]` have `e < x`, and all `e` in `arr[i:hi]` have `e >= x`.
    *   **Time Complexity: O(log N)**, where N is the length of the list (or `hi-lo`).
    *   **Use Case:** Useful for finding the first occurrence of `x` or the index where `x` would be inserted to maintain order, preferring the leftmost position for duplicates.
    ```python
    import bisect

    sorted_arr = [10, 20, 20, 30, 40]
    print(f"bisect_left({sorted_arr}, 20): {bisect.bisect_left(sorted_arr, 20)}") # Output: 1 (index before existing 20s)
    print(f"bisect_left({sorted_arr}, 25): {bisect.bisect_left(sorted_arr, 25)}") # Output: 3 (index where 25 would go)
    print(f"bisect_left({sorted_arr}, 5):  {bisect.bisect_left(sorted_arr, 5)}")  # Output: 0
    print(f"bisect_left({sorted_arr}, 50): {bisect.bisect_left(sorted_arr, 50)}") # Output: 5
    ```

2.  **`bisect.bisect_right(arr, x, lo=0, hi=len(arr))` (or `bisect.bisect(arr, x, ...)`):**
    *   **Description:** Returns an insertion point `i` for `x` in `arr` to maintain sorted order. If `x` is already present in `arr`, the insertion point will be **after (to the right of)** any existing entries of `x`.
    *   More formally, it returns `i` such that all `e` in `arr[lo:i]` have `e <= x`, and all `e` in `arr[i:hi]` have `e > x`.
    *   **Time Complexity: O(log N)**.
    *   **Use Case:** Useful if you want to insert after existing duplicates or find the point beyond which all elements are greater than `x`.
    ```python
    sorted_arr = [10, 20, 20, 30, 40]
    print(f"bisect_right({sorted_arr}, 20): {bisect.bisect_right(sorted_arr, 20)}")# Output: 3 (index after existing 20s)
    print(f"bisect_right({sorted_arr}, 25): {bisect.bisect_right(sorted_arr, 25)}")# Output: 3
    ```
    *   `bisect.bisect` is an alias for `bisect.bisect_right`.

3.  **`bisect.insort_left(arr, x, lo=0, hi=len(arr))`:**
    *   **Description:** Inserts `x` into `arr` in sorted order. If `x` is already present, it's inserted **before (to the left of)** existing entries.
    *   Equivalent to `arr.insert(bisect.bisect_left(arr, x, lo, hi), x)`.
    *   **Time Complexity: O(N)** in the worst case for the `list.insert` part (due to shifting elements). The `bisect_left` part is O(log N). For many LeetCode problems, if N is reasonably small or insertions are infrequent, this can be acceptable.
    *   **Space Complexity: O(1)** if list capacity allows, O(N) if list needs resizing (amortized).
    ```python
    arr_ins_left = [10, 20, 30, 40]
    bisect.insort_left(arr_ins_left, 25)
    print(arr_ins_left) # Output: [10, 20, 25, 30, 40]
    bisect.insort_left(arr_ins_left, 20)
    print(arr_ins_left) # Output: [10, 20, 20, 25, 30, 40] (new 20 inserted before old one)
    ```

4.  **`bisect.insort_right(arr, x, lo=0, hi=len(arr))` (or `bisect.insort(arr, x, ...)`):**
    *   **Description:** Inserts `x` into `arr` in sorted order. If `x` is already present, it's inserted **after (to the right of)** existing entries.
    *   Equivalent to `arr.insert(bisect.bisect_right(arr, x, lo, hi), x)`.
    *   **Time Complexity: O(N)** (worst case for `list.insert`).
    ```python
    arr_ins_right = [10, 20, 30, 40]
    bisect.insort_right(arr_ins_right, 25)
    print(arr_ins_right) # Output: [10, 20, 25, 30, 40]
    bisect.insort_right(arr_ins_right, 20)
    print(arr_ins_right) # Output: [10, 20, 20, 25, 30, 40] (new 20 inserted after old one)
    ```
    *   `bisect.insort` is an alias for `bisect.insort_right`.

**Using `bisect` for Queries on a Sorted List:**
This is where `bisect` truly shines, allowing for efficient queries. Let `sorted_arr` be a pre-sorted list.

1.  **Check if a value `x` exists:**
    *   Find the insertion point using `bisect_left`.
    *   Check if the element at that point (if within bounds) is actually `x`.
    *   Time Complexity: O(log N)
    ```python
    def exists(arr, x):
        i = bisect.bisect_left(arr, x)
        return i < len(arr) and arr[i] == x

    print(f"Does 20 exist in {sorted_arr}? {exists(sorted_arr, 20)}") # Output: True
    print(f"Does 25 exist in {sorted_arr}? {exists(sorted_arr, 25)}") # Output: False
    ```

2.  **Count occurrences of `x`:**
    *   `count = bisect_right(arr, x) - bisect_left(arr, x)`
    *   Time Complexity: O(log N)
    ```python
    sorted_arr_counts = [10, 20, 20, 20, 30, 40, 40]
    count_20 = bisect.bisect_right(sorted_arr_counts, 20) - bisect.bisect_left(sorted_arr_counts, 20)
    print(f"Count of 20 in {sorted_arr_counts}: {count_20}") # Output: 3
    count_35 = bisect.bisect_right(sorted_arr_counts, 35) - bisect.bisect_left(sorted_arr_counts, 35)
    print(f"Count of 35 in {sorted_arr_counts}: {count_35}") # Output: 0
    ```

3.  **Check if a value less than `x` exists:**
    *   `idx = bisect.bisect_left(sorted_arr, x)`
    *   If `idx > 0`, then `sorted_arr[idx-1]` is less than `x`.
    *   Time Complexity: O(log N)
    ```python
    def has_less_than(arr, x):
        idx = bisect.bisect_left(arr, x)
        return idx > 0 # If idx is 0, no elements are less than x

    print(f"In {sorted_arr}, value < 25 exists? {has_less_than(sorted_arr, 25)}") # True (20)
    print(f"In {sorted_arr}, value < 10 exists? {has_less_than(sorted_arr, 10)}") # False
    print(f"In {sorted_arr}, value < 5 exists?  {has_less_than(sorted_arr, 5)}")  # False
    ```

4.  **Find smallest value greater than or equal to `x` (Lower Bound):**
    *   `idx = bisect.bisect_left(sorted_arr, x)`
    *   If `idx < len(sorted_arr)`, then `sorted_arr[idx]` is the smallest value `>= x`. Otherwise, no such element exists.
    *   Time Complexity: O(log N)
    ```python
    def find_ge(arr, x): # Greater than or Equal
        idx = bisect.bisect_left(arr, x)
        return arr[idx] if idx < len(arr) else None

    print(f"Smallest val >= 20 in {sorted_arr}: {find_ge(sorted_arr, 20)}") # Output: 20
    print(f"Smallest val >= 25 in {sorted_arr}: {find_ge(sorted_arr, 25)}") # Output: 30
    print(f"Smallest val >= 45 in {sorted_arr}: {find_ge(sorted_arr, 45)}") # Output: None
    ```

5.  **Check if a value greater than `x` exists:**
    *   `idx = bisect.bisect_right(sorted_arr, x)`
    *   If `idx < len(sorted_arr)`, then `sorted_arr[idx]` is greater than `x`.
    *   Time Complexity: O(log N)
    ```python
    def has_greater_than(arr, x):
        idx = bisect.bisect_right(arr, x)
        return idx < len(arr) # If idx is len(arr), no elements are strictly greater than x

    print(f"In {sorted_arr}, value > 25 exists? {has_greater_than(sorted_arr, 25)}") # True (30)
    print(f"In {sorted_arr}, value > 40 exists? {has_greater_than(sorted_arr, 40)}") # False
    print(f"In {sorted_arr}, value > 50 exists? {has_greater_than(sorted_arr, 50)}") # False
    ```

6.  **Find largest value less than or equal to `x` (Upper Bound - related concept):**
    *   `idx = bisect.bisect_right(sorted_arr, x)`
    *   If `idx > 0`, then `sorted_arr[idx-1]` is the largest value `<= x`. Otherwise, no such element exists.
    *   Time Complexity: O(log N)
    ```python
    def find_le(arr, x): # Less than or Equal
        idx = bisect.bisect_right(arr, x)
        return arr[idx-1] if idx > 0 else None

    print(f"Largest val <= 20 in {sorted_arr}: {find_le(sorted_arr, 20)}") # Output: 20
    print(f"Largest val <= 25 in {sorted_arr}: {find_le(sorted_arr, 25)}") # Output: 20
    print(f"Largest val <= 5 in {sorted_arr}: {find_le(sorted_arr, 5)}")   # Output: None
    ```

**Binary Search: The Underlying Principle**
The `bisect` module effectively implements binary search to find these insertion points. Binary search is a fundamental algorithm for searching in sorted arrays.

*   **Concept:** Repeatedly divide the search interval in half. If the value of the search key is less than the item in the middle of the interval, narrow the interval to the lower half. Otherwise, narrow it to the upper half. Continue until the value is found or the interval is empty.
*   Many LeetCode problems explicitly require you to implement binary search, either on a sorted array or to find a value within a range that satisfies certain conditions (e.g., "find minimum k such that..."). Understanding `bisect` helps solidify binary search concepts.

**Key LeetCode Use Cases for Sorted Lists & `bisect`:**
*   **Maintaining a dynamic sorted collection:** When you need to add elements and query the collection efficiently (e.g., find median from a data stream, if combined with two heaps, or for smaller N with `insort`).
*   **Problems involving ranges or "closest element" queries on a sorted array.**
*   **Optimizing search steps in algorithms:** If a subproblem involves searching in a collection that can be kept sorted.
*   **As a direct tool for problems like "Search Insert Position" (LeetCode #35), which is exactly what `bisect_left` does.**
*   **Counting elements in ranges `[a, b]`:** `bisect_right(arr, b) - bisect_left(arr, a)`.
*   Many dynamic programming problems where states depend on sorted sub-sequences or finding optimal points in sorted ranges.
*   Problems that can be reduced to finding an element, or the count of elements, satisfying a condition in a sorted array (e.g., "Number of Smaller by Current Number" after sorting).

**Pythonic Tips & Common Pitfalls for `bisect`:**
*   **List MUST be sorted:** `bisect` functions assume the input list is already sorted. They do not sort it for you. Results will be incorrect if the list is not sorted.
*   **`insort` is O(N):** While finding the insertion point is O(log N), the `list.insert` operation within `insort_left` and `insort_right` is O(N) because it may need to shift all subsequent elements. If you have a very large number of insertions, this can become a bottleneck.
*   **`bisect_left` vs. `bisect_right`:** Understand the subtle difference, especially when dealing with duplicates or when you need to find the first/last occurrence or specific boundary conditions.
    *   `bisect_left` is good for "find first element >= x".
    *   `bisect_right` is good for "find first element > x".
*   The `lo` and `hi` parameters in `bisect` functions allow you to operate on a sub-segment of the list, which can be useful.

---
This module on `bisect` and sorted lists concludes our pre-requisite learning phase. You now have a foundational understanding of Python's core data types, their operations, complexities, and common use cases, as well as conceptual understanding of more complex structures like trees and graphs, and utility modules like `heapq` and `bisect`.

With this knowledge, you are much better prepared to approach LeetCode problems. The next step would be to start practicing problems, categorizing them by data structure or common patterns (like those on NeetCode or AlgoMap), and applying these fundamentals.

## References


