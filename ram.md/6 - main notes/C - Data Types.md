18-03-2025 11:55:45

Status : #child

Tags : [[C]] [[Data Types]]
# C - Data Types

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


## References

[[CHAPTER 2 - TYPES, OPERATORS and EXPRESSION]]