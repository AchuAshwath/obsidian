20-03-2025 17:24:00

Status : #adult 

Tags : [[C]] 

# CHAPTER 3 - CONTROL FLOW

The control flow statements of a language specify the order in which computations are done. We have already met the most common control flow constructions of C in earlier examples; here we will complete the set, and be more precise about the ones discussed before.

[Page 51](https://www.cc4e.com/book/chap03.md#)
## 3.1 Statements and Blocks

An _expression_ such as `x = 0` or `i++` or `printf( ... )` becomes a _statement_ when it is followed by a semicolon, as in

```c
x = 0;
i++;
printf(...);
```

In C, the semicolon is a statement terminator, rather than a separator as it is in Algol-like languages.

The braces { and } are used to group declarations and statements together into a _compound statement_ or _block_ so that they are syntactically equivalent to a single statement. The braces that surround the statements of a function are one obvious example; braces around multiple statements after an `if`, `else`, `while` or `for` are another. (Variables can actually be declared inside _any_ block; we will talk about this in [Chapter 4](https://www.cc4e.com/book/chap04.md).) There is never a semicolon after the right brace that ends a block.

_Ah C, how do I love thee? Let me count the ways._ - Dr. Chuck with homage to [Elizabeth Barrett Browning](https://en.wikipedia.org/wiki/Elizabeth_Barrett_Browning)

The humble [semicolon](https://en.wikipedia.org/wiki/Semicolon) is why spacing and line-ends do not matter to C and C-like languages. It means we as programmers can focus all of our white space and lines on communicating our intent to humans. This freedom is not an excuse to write obtuse or dense code (see the [Obfuscated Perl Contest](https://en.wikipedia.org/wiki/Obfuscated_Perl_Contest)) but instead freedom to describe what we mean or use spacing to help us understand our code.

We can take a quick look at how a few other C-like languages treat the semicolon. Java is just like C in that the semicolon terminates statements. Python treats the semicolon as a separator - allowing more than one statement on a single line. But since Python treats the end of line as a statement separator - you generally never use semicolon in Python. But for people like me who automatically add a semicolon when typing code too fast, at least Python ignores the few semicolons I add to my code out of habit. JavaScript treats semicolon as a separator but since JavaScript ignores the end of a line (it is whitespace), semicolons are required when a block of code consists of more than one line. When I write JavaScript, I meticulously include semicolons at the end of all statements because "any good C programmer can write C in any language".

[Page 51](https://www.cc4e.com/book/chap03.md#)
## 3.2 If-Else

The `if-else` statement is used to make decisions. Formally, the syntax is

```c
if (expression)
    statement-1
else
    statement-2
```

where the `else` part is optional. The _expression_ is evaluated; if it is "true" (that is, if _expression_ has a non-zero value), _statement-1_ is done. If it is "false" _(expression_ is zero) and if there is an `else` part, _statement-2_ is executed instead.

Since an `if` simply tests the numeric value of an expression, certain coding shortcuts are possible. The most obvious is writing

```c
if (expression)
```

instead of

```c
if (expression != 0)
```

Sometimes this is natural and clear; at other times it is cryptic.

Because the `else` part of an `if-else` is optional, there is an ambiguity when an `else` is omitted from a nested `if` sequence. This is resolved in the usual way - the `else` is associated with the closest previous `else`-less if. For example, in

```c
if (n > 0)
  if (a > b)
      z = a;
  else
      z = b;
```

the `else` goes with the inner `if`, as we have shown by indentation. If that isn't what you want, braces must be used to force the proper association:

```c
if (n > 0) {
  if (a > b)
      z = a;
}
else
  z = b;
```

The ambiguity is especially pernicious in situations like:

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

The indentation shows unequivocally what you want, but the compiler doesn't get the message, and associates the `else` with the inner `if`. This kind of bug can be very hard to find.

By the way, notice that there is a semicolon after `z = a` in

```c
if (a > b)
  z = a;
else
  z = b;
```

This is because grammatically, a _statement_ follows the `if`, and an expression statement like `z = a` is always terminated by a semicolon.

[Page 53](https://www.cc4e.com/book/chap03.md#)

## 3.3 Else-If

The construction

```c
if (expression)
    statement
else if (expression)
    statement
else if (expression)
    statement
else
    statement
```

occurs so often that it is worth a brief separate discussion. This sequence of `if`'s is the most general way of writing a multi-way decision. The _expression's_ are evaluated in order; if any _expression_ is true, the _statement_ associated with it is executed, and this terminates the whole chain. The code for each _statement_ is either a single statement, or a group in braces.

The last `else` part handles the "none of the above" or default case where none of the other conditions was satisfied. Sometimes there is no explicit action for the default; in that case the trailing

```c
else
    statement
```

can be omitted, or it may be used for error checking to catch an "impossible" condition.

To illustrate a three-way decision, here is a binary search function that decides if a particular value `x` occurs in the sorted array `v`. The elements of `v` must be in increasing order. The function returns the position (a number between 0 and n-1) if `x` occurs in `v`, and -1 if not.

```c
#include<stdio.h>

int binary(int x,int v[],int  n) /* find x in v[0] ... v[n-1] */{
  int low, high, mid;

  low = 0;
  high = n - 1;
  while (low <= high)
  {
    mid = (low+high) / 2;
    if (x < v[mid])
      high = mid - 1;
    else if (x > v[mid])
      low = mid + 1;
    else /* found match */
      return (mid);
  }
  return(-1);
}

int main() {
    int v[] = {1, 3, 5, 7, 9, 11, 13, 15, 17, 19}; // Must be sorted
    int n = sizeof(v) / sizeof(v[0]);
    int x;

    printf("Enter a number to search: ");
    scanf("%d", &x);

    int result = binary(x, v, n);

    if (result != -1)
        printf("Element found at index %d\n", result);
    else
        printf("Element not found.\n");

    return 0;
}
```

The fundamental decision is whether `x` is less than, greater than, or equal to the middle element `v[mid]` at each step; this is a natural for `else-if`.

Note that in the above examples, the `else` and the `if` are two language constructs that are just being used idiomatically to construct an `else if` pattern with indentation that captures the idiom.

If we are pedantic about indentation of the above sequence we would be separating the `else` and `if` and then indenting each succeeding block further as follows (brackets added for clarity):

```c
if (expression) {
    statement
}
else 
{
    if (expression) {
        statement
    }
    else 
    {
        if (expression) {
            statement
        }
        else
        {
            statement
        }
    }
}
```

Java and JavaScript keep the `else` and `if` as separate language elements and document their idiomatic usage and indentation just like C.

But the Python `elif` is a new language construct that achieves the same end as shown below:

```c
if (expression) :
    block
elif (expression) :
    block
elif (expression) :
    block
else :
    block
```

The C/Java/JavaScript and Python idioms thankfully look the same when the idiomatic indentation is used. Even FORTRAN 77 supports the `ELSE IF` construct.

[Page 54](https://www.cc4e.com/book/chap03.md#)
## 3.4 Switch

The `switch` statement is a special multi-way decision maker that tests whether an expression matches one of a number of _constant_ values, and branches accordingly. In [Chapter 1](https://www.cc4e.com/book/chap01.md) we wrote a program to count the occurrences of each digit, white space, and all other characters, using a sequence of `if ... else if ... else`. Here is the same program with a `switch`.

```c
#include <stdio.h>

int main() /* count digits, white space, others */
{
  int c, i, nwhite, nother, ndigit[10];

  nwhite = nother = 0;
  for (i = 0; i < 10; i++)
      ndigit[i] = 0;

  while ((c = getchar()) != EOF)
      switch (c) {
      case '0':
      case '1':
      case '2':
      case '3':
      case '4':
      case '5':
      case '6':
      case '7':
      case '8':
      case '9':
            ndigit[c-'0']++;
            break;
      case ' ':
      case '\n':
      case '\t':
            nwhite++;
            break;
      default:
            nother++;
            break;
      }

  printf("digits =");
  for (i = 0; i < 10; i++)
    printf(" %d", ndigit[i]);
  printf("\nwhite space = %d, other = %d\n", nwhite, nother);
}
```

The `switch` evaluates the integer expression in parentheses (in this program the character `c`) and compares its value to all the cases. Each case must be labeled by an integer or character constant or constant expression. If a case matches the expression value, execution starts at that case. The case labeled `default` is executed if none of the other cases is satisfied. A `default` is optional; if it isn't there and if none of the cases matches, no action at all takes place. Cases and default can occur in any order. Cases must all be different.

The `break` statement causes an immediate exit from the `switch`. Because cases serve just as labels, after the code for one case is done, execution _falls through_ to the next unless you take explicit action to escape. `break` and `return` are the most common ways to leave a `switch`. A `break` statement can also be used to force an immediate exit from `while`, for and do loops as well, as will be discussed later in this chapter.

Falling through cases is a mixed blessing. On the positive side, it allows multiple cases for a single action, as with the blank, tab or newline in this example. But it also implies that normally each case must end with a break to prevent falling through to the next. Falling through from one case to another is not robust, being prone to disintegration when the program is modified. With the exception of multiple labels for a single computation, fall-throughs should be used sparingly.

As a matter of good form, put a `break` after the last case (the `default` here) even though it's logically unnecessary. Some day when another case gets added at the end, this bit of defensive programming will save you.

Ah the `switch` statement. What is there to say? I think that the `switch` statement was added to C to compete with the earlier FORTRAN "computed GOTO" statement and to keep low-level programmers from switching to assembly language to implement a [branch table](https://en.wikipedia.org/wiki/Branch_table).

The authors spend most of the previous section apologizing for the `switch` statement, so perhaps you should take that as a hint and avoid it in your code.

There are very few situations where a branch table outperforms a series of if-else checks and those are likely deep in library or operating system code. Programmers should only use `switch` if they understand what a branch table is, and why it is more efficient for this particular bit of their program. Otherwise just use `else if` to do the readers of your code a favor.

One can only wonder if Guido van Rossum or someone else at Centrum Wiskunde & Informatica (CWI) in the Netherlands looked at the above code example and thought, "Interesing how `case` works in a C `switch` statement - a colon at the end of the line and indenting the following lines _is_ an elegant way to visually denote blocks of code."

**Exercise 3-1.** Write a function `expand(s, t)` which converts characters like newline and tab into visible escape sequences like \n and \t as it copies the string `s` to `t`. Use a `switch`.

[Page 56](https://www.cc4e.com/book/chap03.md#)

## 3.5 Loops and stuff

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


The **`break`** statement provides an early exit from `for`, `while`, and `do`, just as from `switch`. A `break` statement causes the innermost enclosing loop (or `switch`) to be exited immediately.

The `continue` statement is related to `break`, but less often used; it causes the _next iteration_ of the enclosing loop (`for`, `while`, `do`) to begin. In the `while` and `do`, this means that the test part is executed immediately; in the `for`, `control` passes to the re-initialization step. (`continue` applies only to loops, not to `switch`. A continue inside a `switch` inside a loop causes the next loop iteration.

## 3.6 Goto's and Labels

The `goto` is never necessary, and in practice it is almost always easy to write code without it.

The most common use is to abandon processing in some deeply nested structure, such as breaking out of two loops at once. The `break` statement cannot be used directly since it leaves only the innermost loop.
# Reference