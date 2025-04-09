22-01-2025 15:10:10

Status : #baby 

Tags : [[C]]

# Introduction to C

C is a relatively "low level" language and deals with the same sort of objects that most computers do, such as *characters, numbers, and addresses*.

These may be combined and moved about with the usual arithmetic and logical operators implemented by actual machines.

C provides no operations to deal directly with composite objects such as 
 - character strings,
 - sets,
 - lists,
 - or arrays considered as a whole, and neither supports **heap or garbage collection**

Similarly, C offers only straightforward 
- **Single-thread control flow constructions** - *tests*, *loops*, *grouping*,  and *subprograms*. 
- but not **Multiprogramming** - *parallel operations*, *synchronization*, or *coroutines*.

- In C we have to declare your variables before using them.
- stdio - is the standard library in C.
- There is no string in C, there is only character array.
- integer division truncates in C.
- In C there is precedence for operators.
## C Operator Precedence

The following table lists the precedence and associativity of C operators. Operators are listed top to bottom, in descending precedence.

| Precedence | Operators    | Description                                       | Associativity |
| ---------- | ------------ | ------------------------------------------------- | ------------- |
| 1          | ++, --       | Suffix/postfix increment and decrement            | Left-to-right |
|            | ()           | Function call                                     | Left-to-right |
|            | []           | Array subscripting                                | Left-to-right |
|            | .            | Structure and union member access                 | Left-to-right |
|            | ->           | Structure and union member access through pointer | Left-to-right |
|            | (type){list} | Compound literal (C99)                            | Left-to-right |
| 2          | ++, --       | Prefix increment and decrement¹                   | Right-to-left |
|            | +, -         | Unary plus and minus                              | Right-to-left |
|            | !, ~         | Logical NOT and bitwise NOT                       | Right-to-left |
|            | (type)       | Cast                                              | Right-to-left |
|            | *            | Indirection (dereference)                         | Right-to-left |
|            | &            | Address-of                                        | Right-to-left |
|            | sizeof       | Size-of²                                          | Right-to-left |
|            | _Alignof     | Alignment requirement (C11)                       | Right-to-left |
| 3          | *, /, %      | Multiplication, division, and remainder           | Left-to-right |
| 4          | +, -         | Addition and subtraction                          | Left-to-right |
| 5          | <<, >>       | Bitwise left shift and right shift                | Left-to-right |
| 6          | <, <=, >, >= | Relational operators                              | Left-to-right |
| 7          | ==, !=       | Equality operators                                | Left-to-right |
| 8          | &            | Bitwise AND                                       | Left-to-right |
| 9          | ^            | Bitwise XOR (exclusive OR)                        | Left-to-right |
| 10         | \|           | Bitwise OR (inclusive OR)                         | Left-to-right |
| 11         | &&           | Logical AND                                       | Left-to-right |
| 12         | \|\|         | Logical OR                                        | Left-to-right |
| 13         | ?:           | Ternary conditional³                              | Right-to-left |
| 14         | =            | Simple assignment                                 | Right-to-left |
|            | +=, -=       | Assignment by sum and difference                  | Right-to-left |
|            | *=, /=, %=   | Assignment by product, quotient, and remainder    | Right-to-left |
|            | <<=, >>=     | Assignment by bitwise left shift and right shift  | Right-to-left |
|            | &=, ^=,\|=   | Assignment by bitwise AND, XOR, and OR            | Right-to-left |
| 15         | ,            | Comma operator                                    | Left-to-right |
> Operators with lower precedence value have higher priority.

## Best Practices
- use symbolic constants or symbolic names for magic numbers(CONSTANTs) in the program for better readability of the code.
- 
# C Programming Language Fundamentals

C is a mid-level programming language known for its efficiency and flexibility. Below are the fundamental concepts you should understand to work effectively in C.

## 1.1 Variables and Data Types
Variables are placeholders that store data values. C has several built-in data types:

- **int**: Stores integers (e.g., `int age = 25;`).
- **float** or **double**: Represents floating-point numbers (e.g., `double weight = 67.5;`).
- **char**: Holds a single character (e.g., `char c = 'A';`).
- **void** : indicates no value is present (e.g, `void malloc()`)

You declare variables using their types and names:
```c
int x;  // declaration of a variable
int a = 10, b;

// Initialization during declaration is optional.
```
 
 In addition to these datatypes, each type has qualifiers which can to applied such as `short`, `long` and `unsigned`. for example 
 ```c
short int x; // 
long int y;
unsigned int z;
 ```
#### Data types

| Type    | Description                                    |
| ------- | ---------------------------------------------- |
| char    | character - a single byte                      |
| short   | short integer                                  |
| long    | long integer                                   |
| double  | double-precision floating point                |
| int     | integer numbers                                |
| float   | floating point numbers                         |
| pointer | points to a memory address                     |
| array   | collection of multiple values of the same type |

| Data Type                  | Size (bytes) | Range                           | Format Specifier |
| -------------------------- | ------------ | ------------------------------- | ---------------- |
| **short int**              | 2            | -32,768 to 32,767               | %hd              |
| **unsigned short int**     | 2            | 0 to 65,535                     | %hu              |
| **unsigned int**           | 4            | 0 to 4,294,967,295              | %u               |
| **int**                    | 4            | -2,147,483,648 to 2,147,483,647 | %d               |
| **long int**               | 4            | -2,147,483,648 to 2,147,483,647 | %ld              |
| **unsigned long int**      | 4            | 0 to 4,294,967,295              | %lu              |
| **long long int**          | 8            | -(2^63) to (2^63)-1             | %lld             |
| **unsigned long long int** | 8            | 0 to 18,446,744,073,709,551,615 | %llu             |
| **signed char**            | 1            | -128 to 127                     | %c               |
| **unsigned char**          | 1            | 0 to 255                        | %c               |
| **float**                  | 4            | 1.2E-38 to 3.4E+38              | %f               |
| **double**                 | 8            | 1.7E-308 to 1.7E+308            | %lf              |
| **long double**            | 16           | 3.4E-4932 to 1.1E+4932          | %Lf              |
> There are more datatypes other than these primitive datatypes in C, such as 
> 1. Derived Types - pointers, arrays, functions
> 2. User defined Data Types - structure, union, enum

## 1.2 Constants
### Integer and Floating-Point Constants  
- **Floats**: Can use scientific notation, e.g., `123.456e-7`, `0.12E3`.  
- **Double by default**: Every floating-point constant is treated as `double`.  
-  *Long Constants* are **Indicated by `L`**: e.g., `123L`.  
### Octal and Hexadecimal Constants  
- **Octal**: Begins with `0`, e.g., `037` (decimal 31).  
- **Hexadecimal**: Begins with `0x` or `0X`, e.g., `0x1F`.  
- **Can be long**: Add `L`, e.g., `0x1FL`.  
- **Octal representation**: `'\ddd'`, e.g., `'\014'` (form feed).  
### Character Constants  
- **Single quotes**: e.g., `'x'`.  
- **Represents numeric value** in the character set (ASCII/EBCDIC).  
## Escape Sequences  
| Escape Sequence | Meaning        |
| --------------- | -------------- |
| `\n`            | Newline        |
| `\t`            | Tab            |
| `\\`            | Backslash      |
| `\'`            | Single quote   |
| `\0`            | Null character |
## Constant Expressions  
- **Evaluated at compile-time**.  

```c
  #define MAXLINE 1000
  char line[MAXLINE+1];
```
## String Constants

- **Double quotes**: e.g., `"I am a string"`, `""` (null string).
- **Auto null-terminated** (`\0`).
- **Example**:
  
    ```c
char s[] = "Hello";  // Stored as {'H', 'e', 'l', 'l', 'o', '\0'}`
```

## Character vs. String Constants

- **Character**: `'x'` → Represents numeric value of `x`.
- **String**: `"x"` → Array with `x` and `\0`.

## 1.3 Declarations and Initialization

### Declaration

- All variables **must be declared before use**.  
- A **declaration specifies a type** followed by one or more variables:  

  ```c
  int lower, upper, step;
  char c, line[1000];
- ```

- Variables can also be declared separately:
```c
int lower;
int upper;
int step;
char c;
char line[1000];
```

>**Separate declarations are useful** for adding comments or future modifications.

### Initialization

- Variables can be initialized at declaration:
```c
char backslash = '\\';
int i = 0;
float eps = 1.0e-5;
```

- *Automatic variables* (inside functions)
	- Explicitly initialized **each time the function runs**.
	- If **not initialized**, they contain **garbage values**.
- *External and static variables*
	- **Initialized once** before program execution.
	- **Default value is `0`** if not explicitly initialized.
### Best Practices
- **Always initialize variables explicitly**, even if defaults apply.
- **Use separate declarations for clarity** when necessary.

## 1.4 Arithmetic Operators

- The binary arithmetic operators are **`+`**, **`-`**, **`*`**, **`/`**, and the modulus operator **`%`**. 
- There is a unary **`-`**, but no unary **`+`**.
- Integer division truncates any fractional part.
- The **`%`** operator cannot be applied to `float` or `double`.

>The order of evaluation is not specified for associative and commutative operators like `*` and `+`; the compiler may rearrange a parenthesized computation involving one of these. Thus `a+(b+c)` can be evaluated as `(a+b)+c`. This rarely makes any difference, but if a particular order is required, explicit temporary variables must be used.

## 1.5 Relational and Logical Operators

- Relational operators are `>`, `<`, `<=`, `>=` - all have same precedence.
- Just below them in precedence are the equality operators `==`, `!=`.
- Relational operators have lower precedence than arithmetic operators, so expressions like `i < lim-1` are taken as `i < (lim - 1)`.
- unary negator operator `!` converts a non-zero or true operand into 0, and a zero or false operand into 1.

```c
if (!inword)

rather than

if (inword == 0)
```

## 1.6 Type Conversions



## 1.2 Control Structures

Control structures determine the flow of execution.
### If-Else Statements
Use `if` to execute code when a condition is true and `else` for other cases:
```c
if (x > 5) {
    // Execute when x is greater than 5.
} else {
    // Execute when x is less than or equal to 5.
}
```

after the *if expression* statements are supposed to be grouped by braces, or else the the last if will be associated with the else statement, so always use braces to bring the associativity of appropriate if and else block because the complier won't check on its own.

```c
if (n > 0)
  for (i = 0; i < n; i++)
      if (s[i] > 0) {
          printf("...");
          return(i);
      }
else /* WRONG */
  printf("error - n is zero\n");
```


> there is no multiway statement in C, else if statements are essentially if(condition){...}esle{if(condition){...}}
### Switch-Case Statements
Use `switch` to evaluate expressions against multiple cases:
```c
switch (grade) {
    case 'A':
        printf("Excellent\n");
    case 'B':
        printf("Good\n");
        break;
    default:
        printf("Other\n");
}
```

> here since the case 'A' has no **break** the compiler will get into the case and then *fall through* until it encounters a break statement, so the output would be,

```bash
Excellent
Good
```
### Loops
- **For Loop**: Iterates based on initialization, condition, and update:
  ```c
  for (int i = 0; i < 10; i++) {
      // Execute 10 times.
  }
  ```

- **While Loop**: Repeats while a condition is true:
  ```c
  int n = 5;
  while (n > 0) {
      printf("Count: %d\n", n);
      n--;
  }
  ```

- **Do-While Loop**: Repeats until a condition is met, ensuring at least one execution:
  ```c
  do {
      // Code block.
  } while (condition);
  ```

## 1.3 Functions
Functions are reusable code blocks with specific purposes.

### Function Declaration and Definition
```c
// Declaration
void greet(char* name);

// Definition
void greet(char* name) {
    printf("Hello, %s!\n", name);
}
```

### Function Parameters
```c
void sum(int a, int b); // Function declaration.
void sum(int a, int b) { // Function definition.
    return a + b;
}
```

### Return Values
Return values with `return` statement:
```c
int multiply(int a, int b) {
    return a * b;
}
```
## 1.4 Arrays
Arrays store multiple values of the same type.

### Initialization and Access
Declare and initialize an array:
```c
int arr[5] = {1, 2, 3, 4, 5};
int a = arr[0]; // Access first element.
```

- C arrays cannot be changed in runtime, size of the array must be a *constant* in compile time. due to this inability to automatically resize C arrays leads to **buffer overflow**.

> arrays are passed by reference in C functions when they are passed as arguments/parameters.
## 1.5 Pointers
Pointers point to memory addresses of variables or functions.

### Pointer Declaration and Initialization
```c
int a = 10;
int* ptr = &a; // Points to 'a'.
```

### Pointer Arithmetic
Perform arithmetic on pointers:
```c
ptr++; // Increment pointer.
```

### Common Pitfalls
Avoid dereferencing null (e.g., `*null` is undefined behavior).

## 1.6 Structures and Unions
Structures group data of different types, while unions group varying data sizes.

### Structure Declaration
```c
struct Student {
    char name[5];
    int age;
};

struct Student s = {"Alice", 20};
```

### Union Declaration
```c
union Weekday {
    int day; // Integer (1-7).
    charabbr; // Character with weekday abbreviations.
};

union Weekday w = THU; // Thursday.
```

## 1.7 Bit Manipulation
Use bitwise operators to manipulate binary data.

### Basic Operators
- `&` : AND
- `|` : OR
- `^` : XOR (used for toggling bits)
- `<<`, `>>` : Shift left or right

### Example
```c
int x = 5; // Binary: 101.
x |= 3;    // Binary: 101 | 011 = 111 (7).
```


## References

More on Operators precedence and associativity on [[CHAPTER 2 - TYPES, OPERATORS and EXPRESSION]]

[Operator Precedence](*https://en.cppreference.com/w/c/language/operator_precedence)