16-06-2025 10:42:15

Status :

Tags : [[Two Pointers]]

# Two Pointers: A Powerful Problem-Solving Pattern

The "Two Pointers" pattern is a highly effective technique used in algorithm design, particularly for problems involving arrays and strings. It significantly improves time complexity by using two variables (pointers) to traverse a data structure, often reducing an O(N2) solution to O(N).

## What is a Pointer?

In this context, a **pointer** is simply a variable that represents an index or a position within a linear data structure like an array or a linked list. By strategically positioning and moving these pointers, we can efficiently compare elements and make decisions without resorting to nested loops.

## Types of Two Pointers Strategies

The two-pointer technique can be applied in three common ways, depending on the problem's requirements:

### 1. Converging Pointers

- **Description:** Pointers start at opposite ends of a data structure and move inward towards each other. They adjust their positions based on comparisons until a certain condition is met or they cross each other.
- **Ideal for:** Problems requiring comparison of elements from opposite ends (e.g., checking for symmetry).
- **Example: Checking for a Palindrome**
    - A palindrome is a word, phrase, or sequence that reads the same forward and backward (e.g., "madam").
    - **Mechanism:**
        1. Initialize a `left` pointer at the beginning and a `right` pointer at the end of the string.
        2. Compare characters at `left` and `right`.
        3. If they match, move both pointers inward (`left++`, `right--`).
        4. If they don't match, the string is not a palindrome; return `false`.
        5. Repeat until `left` meets or crosses `right`.
            
    - **Conceptual Visual:** ```

```
String: [ M A D A M ]
          ^       ^
          L       R

Step 1: M == M. L moves right, R moves left.
String: [ M A D A M ]
            ^   ^
            L   R

Step 2: A == A. L moves right, R moves left.
String: [ M A D A M ]
              ^
              L/R (Pointers meet)
```

### 2. Parallel Pointers

- **Description:** Both pointers start at the same end (usually the beginning) and move in the same direction. They often serve different, complementary roles. The right pointer explores or finds new information, while the left pointer tracks progress or maintains constraints.
- **Variation:** The **Sliding Window Technique** is a popular variation where two pointers define a dynamic range (window) that slides across the array/string to find sub-structures meeting specific criteria.
- **Conceptual Visual:**
    
```
    Array: [ 0, 1, 0, 3, 12 ]
             ^
             L
             ^
             R (L and R start at the same position)
    
    R explores, L places elements based on R's findings.
```

### 3. Trigger-Based Pointers

- **Description:** The first pointer moves independently until it meets a specific condition. Once that condition is met, the second pointer starts traversing, often in relation to the first, to find additional information.
- **Ideal for:** Problems requiring staged processing of elements.
- **Example: Finding the Nth Node from the End of a Linked List**
    - **Mechanism:**
        1. Move the `first` pointer `N` steps forward from the head.
        2. Once `first` reaches the `N`th node, initialize the `second` pointer at the head.
        3. Move both `first` and `second` pointers one step at a time until `first` reaches the end of the list.
        4. At this point, `second` will be at the `N`th node from the end.
    - **Conceptual Visual:**

```
List: Head -> Node1 -> Node2 -> Node3 -> Node4 -> Node5 -> Null
																	^
																	First (after N steps)
								^
								Second (starts here)

Both move until First hits Null.
```

## When to Use the Two-Pointers Pattern

The two-pointers algorithm is generally applied to **linear data structures** such as arrays, strings, or linked lists. Here are some strong indicators that suggest its applicability:

- **Predictable Data Patterns:** The input data follows a predictable pattern, such as a **sorted array** or a **palindromic string**.

> "In a salted array moving a pointer to the right ensures you're always moving to a greater or equal value making it easy to compare the values at both the pointers."

- **Pair/Value Conditions:** The problem explicitly asks for a **pair of values** that satisfy a certain condition, or a result that can be generated from two values.

# Prerequisite 

## [[125. Valid Palindrome]]

## [[26. Remove Duplicates From Sorted Array]]

## [[167. Two Sum II Input Array Is Sorted]]

## [[11. Container With Most Water]]

## [[80. Remove Duplicates From Sorted Array II]]



## References

[AlgoMasterIO](https://youtu.be/QzZ7nmouLTI?si=5MN3-7QWrxGc3wN0)

[LeetCode](https://leetcode.com/discuss/post/1688903/solved-all-two-pointers-problems-in-100-z56cn/)