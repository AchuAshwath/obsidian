07-05-2025 12:12:04

Status : #child 

Tags : [[LeetCode]] [[Strings]]

# Strings

**Concept:**
- An ordered, **immutable** sequence of characters.
- Immutable means once a string is created, it cannot be changed. Operations that appear to modify a string (like concatenation or replace) actually create and return a new string object.

**Python Implementation:** The built-in str type.

```python
message = "Hello, LeetCode!"
empty_string = ""
char = 'c'  # Single characters are also strings
```

**Core Operations (with Time/Space Complexity):**

-  **Access a character by index:** my_str[i]
    - Syntax: char = my_str[index]
    - Description: Retrieves the character at the specified index.
    - Time Complexity: **O(1)**.
    - Space Complexity: O(1).
   
```python
s = "python"

print(s[0])   # Output: p
print(s[-1])  # Output: n
```
   
- **Slicing:** my_str[start:end:step]
    - Syntax: sub_string = my_str[start:end:step]
    - Description: Creates a new string containing a portion of the original.
    - Time Complexity: **O(k)**, where k is the length of the slice.
    - Space Complexity: **O(k)** (for the new string slice).
   
```python
s = "LeetCode"

print(s[0:4])    # Output: Leet
print(s[4:])     # Output: Code
print(s[::-1])   # Output: edoCteeL (reverses the string)
```
   
- **Concatenation:** str1 + str2
    - Syntax: new_str = str1 + str2
    - Description: Creates a new string by joining str1 and str2.
    - Time Complexity: **O(n + m)**, where n and m are lengths of str1 and str2 (due to new string creation and copying).
    - Space Complexity: **O(n + m)**.
   
```python
s1 = "abc"
s2 = "def"

s3 = s1 + s2
print(s3)  # Output: abcdef
```

> **Pitfall:** Repeatedly concatenating strings in a loop (s = s + char) is inefficient (O(n^2) if n appends of single chars) because new strings are created each time. Use "".join() instead for building strings from many parts.

- **Joining a list of strings:** separator.join(list_of_strings)
    - Syntax: new_str = separator_string.join(iterable_of_strings)
    - Description: Concatenates strings from an iterable, with separator_string placed between each element. This is the preferred way to build strings from multiple parts.
    - Time Complexity: **O(N)**, where N is the total length of all strings in the iterable plus separators.
    - Space Complexity: **O(N)**.
   
```python
words = ["Hello", "World", "Python"]
sentence = " ".join(words)
print(sentence)  # Output: Hello World Python

chars = ['L', 'e', 'e', 't']
word = "".join(chars)
print(word)      # Output: Leet
```

- **Length of a string:** len(my_str)
    - Syntax: length = len(my_str)
    - Time Complexity: **O(1)**.
    - Space Complexity: O(1).
   
```python
print(len("code")) # Output: 4
```
   
- **Find substring / Check membership:** sub_str in my_str
    - Syntax: is_present = sub_string in my_string
    - Time Complexity: Generally **O(n*m)** in the worst case (n=len(string), m=len(substring)) due to string searching algorithms, but often faster in practice due to optimizations.
    - Space Complexity: O(1).
   
```python
print("code" in "LeetCode")  # Output: True
print("java" in "LeetCode")  # Output: False
```
   
- **Find index of substring:** my_str.find(sub, [start, [end]]), my_str.index(sub, [start, [end]])
    - find(): Returns the lowest index of sub or -1 if not found.
    - index(): Similar to find(), but raises ValueError if sub is not found.
    - Time Complexity: Similar to membership testing, O(n*m) worst-case.
    - Space Complexity: O(1).
   
```python
s = "banana"

print(s.find("na"))     # Output: 2
print(s.find("apple"))  # Output: -1

print(s.index("na"))    # Output: 2
# print(s.index("apple")) # Raises ValueError
```
   
- **Count occurrences of substring:** my_str.count(sub, [start, [end]])
    - Syntax: occurrences = my_str.count(substring)
    - Time Complexity: O(n*m) worst-case.
    - Space Complexity: O(1).
   
```python
s = "mississippi"

print(s.count("ss"))  # Output: 2
print(s.count("i"))   # Output: 4
```
   
- **Check prefix/suffix:** my_str.startswith(prefix), my_str.endswith(suffix)
    - Time Complexity: **O(k)**, where k is the length of the prefix/suffix.
    - Space Complexity: O(1).
   
```python
filename = "script.py"

print(filename.startswith("script"))  # Output: True
print(filename.endswith(".java"))     # Output: False
```
   
- **Replace substring:** my_str.replace(old, new, [count])
    - Syntax: new_string = my_str.replace(old_substring, new_substring)
    - Description: Returns a new string with all occurrences of old_substring replaced by new_substring. Optional count limits replacements.
    - Time Complexity: **O(n)** (approximately, as it needs to scan and build a new string).
    - Space Complexity: **O(n)** (for the new string).
   
```python
s = "hello world world"
new_s = s.replace("world", "Python", 2)

print(new_s)  # Output: hello Python Python
print(s)      # Output: hello world world (original is unchanged)
```
   
- **Split string into a list:** my_str.split(separator=None, maxsplit=-1)
    - Syntax: list_of_substrings = my_str.split(separator_char)
    - Description: Returns a list of substrings, using separator_char as the delimiter. If separator is not specified or None, splits by whitespace and discards empty strings.
    - Time Complexity: **O(n)**.
    - Space Complexity: **O(n)**.
   
```python
csv_line = "apple,banana,cherry"
fruits = csv_line.split(',')
print(fruits)  # Output: ['apple', 'banana', 'cherry']

sentence = "This is a sentence."
words = sentence.split()  # Default: splits by whitespace
print(words)  # Output: ['This', 'is', 'a', 'sentence.']
```
   
- **Case conversion:** lower(), upper(), capitalize(), title(), swapcase()
    - Description: Return new strings with modified casing.
    - Time Complexity: **O(n)**.
    - Space Complexity: **O(n)**.
   
```python
s = "Hello World"

print(s.lower())  # Output: hello world
print(s.upper())  # Output: HELLO WORLD
```
   
- **Stripping whitespace:** strip(), lstrip(), rstrip()
    - Description: Return new strings with leading/trailing (or both) whitespace (or specified characters) removed.
    - Time Complexity: **O(n)** (in worst case, needs to scan).
    - Space Complexity: **O(n)** (if a new string is created, O(1) if no change).
   
```python
s = "   example   "

print(f"'{s.strip()}'")  # Output: 'example'
print(f"'{s.lstrip()}'") # Output: 'example   '
print(f"'{s.rstrip()}'") # Output: '   example'
```
   
- **Character type checks:** isdigit(), isalpha(), isalnum(), islower(), isupper(), isspace()
    - Description: Check if all characters in the string are of a certain type. Return True or False.
    - Time Complexity: **O(n)** (must check all characters).
    - Space Complexity: O(1).
   
```python
print("123".isdigit())  # Output: True
print("abc".isalpha())  # Output: True
print("a1".isalnum())   # Output: True
print(" ".isspace())    # Output: True
```
   
**Key LeetCode Use Cases for str:**
- String manipulation problems (parsing, formatting, validating).
- Palindrome checks.
- Anagram checks (often combined with hashmaps or sorting).
- Substring search.
- Longest common prefix/substring problems.

**Pythonic Tips & Common Pitfalls for str:**

- **Immutability:** Remember strings are immutable. Operations like s += "x" or s.replace(...) create new strings.
- **Efficient String Building:** For building a string from many small pieces (e.g., in a loop), append pieces to a list and then use "".join(list_of_pieces) at the end. This is much more efficient than repeated string concatenation.
   
```python
def innefficient_way():
  result_str_bad = ""
  for i in range(10000):
      result_str_bad += str(i)  # Creates many intermediate strings
  return result_str_bad

def efficient_way():
  parts = []
  for i in range(10000):
      parts.append(str(i))
  result_str_good = "".join(parts)
  return result_str_good

%timeit innefficient_way()
%timeit efficient_way()

# 2.92 ms ± 544 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
# 1.18 ms ± 8.98 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
```

- **Slicing is alright:** Use it for substrings, reversing, and creating copies.
- Strings can be iterated over directly: for char in my_string:.
- When comparing strings, case sensitivity matters unless you explicitly convert to a common case (.lower() or .upper()).
## References


