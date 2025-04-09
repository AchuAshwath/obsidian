18-03-2025 12:06:11

Status : #child

Tags : [[C]] [[Operators]] [[Expressions]]

# C - Relational Operators
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
### Implicit Type Conversions (Promotion Rules):
- `char` and `short` → **converted to `int`**.
- `float` → **converted to `double`** in expressions.
- If one operand is **double**, the other is converted to `double`, and the result is `double`.
- If one operand is **long**, the other is converted to `long`, and the result is `long`.
- If one operand is **unsigned**, the other is converted to `unsigned`, and the result is `unsigned`.
- Otherwise, both operands remain as `int`, and the result is `int`.
### Conversion in Assignments:
- The right-hand side of an assignment is **converted to match the type of the left-hand side**.
- `int → char`: The high-order bits are **discarded**.
- `char → int`: It may be **sign-extended** or **zero-extended**, depending on the system.
- `float → int`: **Fractional part is truncated**.
- `double → float`: **Rounded to the nearest float value**.
### Function Argument Conversions:
- `char` and `short` → **converted to `int`** when passed as arguments.
- `float` → **converted to `double`**.
### Relational and Logical Operators (`&&`, `||`, `>`, `<`):
- Expressions evaluate to **1 if true, 0 if false**.
- Example:

```c
isdigit = (c >= '0' && c <= '9');  // isdigit is set to 1 or 0`
```

### EOF Handling in `getchar()`:
- `getchar()` returns **an `int` instead of `char`** to accommodate `EOF` (`-1`).
- Example:

```c
int c; c = getchar(); if (c == EOF) ...
```
### Explicit Type Conversion (Casting):
- `(type-name) expression` forces conversion to the specified type.
- Example:

```c
sqrt((double) n);  // Converts n to double before passing to sqrt
```

- The cast **only affects the value**, not the original variable.

## 1.7 Increment and Decrement Operators

- `++` is the increment and `--` is the decrement operators.
- the context of placing these operators in the prefix or postfix changes their behavior in using the value.
- For example,
```c
int n = 5;

int x = n++;    // postfix increment will assing n first and then increment, therefore y will be assigned 5 and then incremented to 6
int y = ++n;    // prefix will increment first before assigning the value, therefore n will be incremented from 6 to 7 first and 7 will be assigned to y
```

 also `x = (i + j)++` Is Illegal because,

The **increment operator (`++`)** works **only on modifiable variables** (also called **lvalues**).
- **Lvalue:** A variable that refers to a memory location and can be assigned a value.
- **Rvalue:** A temporary value that does not have a memory address and cannot be assigned.

>`(i + j)` is an **expression**, not a variable.
 The `++` operator **requires a modifiable variable (lvalue)**.
 Since `(i + j)` is a **computed value (rvalue)**, you cannot apply `++` to it.

## 1.8 Assignment Operators

- Expression like `x = 2` will assign the value of 2 to the x named variable here the `=` is the assignment operator.
- `x += 3` can be seen in practice where it means `x = x + 3`.
- **+  -  *  /  %  <<  >>  &  ^  |** - all of binary operators support this short form of assignment.
```c
x *= y + 1   // equivalent expression => x = x * (y+1) rather than x = x * y + 1
```

### 1.9 Conditional Expression

- For a Expression like this, 
```c
if (a > b)
    z = a;
else
    z = b;
```
- C offers ***ternary operator*** `? :`, which can be used to evaluate conditional expression in one line

_e1_ ? _e2_ : _e3_

```c
z = (a > b) ? a : b; /* z = max(a, b) */
```

- Ternary operators used expression are also treated as normal expressions, therefore they will follow the same type conversions discussed earlier.
- Parentheses are not necessary around the first expression of a conditional expression, since the precedence of `?:` is very low, just above assignment.

### 1.10 Precedence and Order of Evaluation

1. Always use **parentheses** when testing bits to ensure correct precedence, 

```c
if ((x & MASK) == 0)  // Ensures the bitwise operation happens first
```

2. **Associativity of Operators (`*`, `+`, `&`, `^`, `|`)**

- These operators are **associative and commutative**, meaning they can be **rearranged** by the compiler.
- **Example where order matters:**

```c
int a = b + c + d;
```
- The compiler may **rearrange** this, but in most cases, it doesn’t affect results.
- **If order matters, use temporary variables**:

```c
int temp = b + c; 
int a = temp + d;
```

3. **Order of Function Evaluation Is Not Defined**
 
 **Example:**
 
 ```c
 x = f() + g();
```

- The compiler **may call `f()` before `g()` or vice versa**.
- If `f()` or `g()` **modify shared variables**, the result may change.
- **Solution:** Use temporary variables:

 ```c
 int temp_f = f(); 
 int temp_g = g(); 
 x = temp_f + temp_g;
```

4. **Function Argument Evaluation Order Is Not Defined**
 
 **Example:**
 ```c
 printf("%d %d\n", ++n, power(2, n));  // Undefined behavior
```

> The result **depends on whether `n` is incremented before or after `power(2, n)` is evaluated**.

 **Solution:**
```c
++n; 
printf("%d %d\n", n, power(2, n));  // Ensures defined behavior
```

5. **Side Effects in Expressions (`a[i] = i++`)**
 
 **Example:**
```c
a[i] = i++;  // Undefined behavior
```

> It is unclear whether `i` is evaluated **before or after** incrementing.

**Solution:** Use a separate statement:
```c
a[i] = i;
i++;
```

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
> 
## References

More on Operators precedence and associativity on [[CHAPTER 2 - TYPES, OPERATORS and EXPRESSION]]

