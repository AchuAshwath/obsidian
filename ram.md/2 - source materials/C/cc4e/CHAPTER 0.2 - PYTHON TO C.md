14-01-2025 17:24:47

Status : #adult

Tags : [[C]]

# PYTHON TO C

| **Python**                                       | **C**                                               |
| ------------------------------------------------ | --------------------------------------------------- |
| white spaces are essential                       | white spaces are ignored                            |
| very object oriented                             | not object oriented at all                          |
| convenient data structures<br> - list<br> - dict | fast efficient powerful<br> - struct<br> - Pointers |
| auto memory management                           | manual memory management                            |
In many ways, Python is a convenience layer built on top of C to make it so users could write code without worrying about the complex details.

### Similarities

- Arithmetic Operators: + - * / % 
- Comparison Operators: == != < > <= the same
- Variable naming rules – letter/underscore +numbers/letters/underscores – also case matters
- While loops – also break and continue in loops
- Constants similar except for strings and characters and booleans
- Both have int / float, and char / byte
	- C has no str, list, or dict
	- Python has no struct or double

### Differences

- Boolean operators
	 - and / not / or  versus &&  !  ||
- C for loops are indeterminant (i.e. no for ... in in C)
- C has no pre-defined True or False
- None and NULL are similar concepts but quite different
- Strings and character arrays are similar concepts but *very* different
- C has no list, or dict
- Python has no struct  - float in Python is a C double

### Printing in python

```python 
# this is a comment
print('Hello world')
print('Answer', 42)
print('Name', 'Sarah')
print('x',3.5,'i',100) 
```
#### Output

```shell
Hello world
Answer 42
Name Sarah
x 3.5 i 100
```

```c
#include <stdio.h>
/* this is a comment */
int main() {
    printf("Hello world\n");
    printf("Answer %d\n", 42);
    printf("Name %s\n", "Sarah");
    printf("x %.1f i %d\n", 3.14, 100);
}
```

- stdio - is the standard library in C.
- printf has the \n which a character to specify newline.
- printf is a function from the standard library, essentially the printf function formats the first argument with the arguments that are followed by it in sequence.
- %d, %s and %f are nothing but the format specifiers and there are more than two, here the %d specifies decimal integer, %s specifies character array (string) and %f specifies floating point.

> The numbers before f are the used to control the precision of the numbers.
> since the format is controlled to be 1 decimal value after the decimal point, the output is just 3.1 instead of 3.14


### Getting number input

US floor to European floor converter program.

```python
print('Enter US Floor')
usfloor = int(input())
eufloor = usfloor - 1
print('EU Floor', eufloor)
```

#### Output
```shell 
Enter US Floor
2
EU Floor 1
```

```c
#include <stdio.h>
int main() {
    int usfloor, eufloor;
    printf("Enter US Floor\n");
    scanf("%d", &usfloor);
    eufloor = usfloor – 1;
    printf("EU Floor %d\n", eufloor);
}
```

- In C we have to declare your variables before using it.
- scanf is similar to input but the %d specifies the scanf to look for integers only, the & is the address operator which specifies the scanf to put the value into the address of the given variable, scanf basically scans for the specific format we ask to scan for. 
### Getting String Input

```python 
print('Enter name')
name = input()
print('Hello', name)
```

#### Output

```shell
Enter name
Sarah
Hello Sarah
```

```c
#include <stdio.h>
int main() {
    char name[101];
    printf("Enter name\n");
    scanf("%100s", name);
    printf("Hello %s\n", name);
}
```

- There is no string in C, there is only character array.
- We also should specify how to the character array should be, or else the program might blow up, memory might leak, there is not automatic append.
- here there is no & before name because in C the name of the character array doesn't hold the value of the array but it holds the address to the array, where name[0] or name[1] is used to get the character present in the array.

### Getting a whole line as input

```python 
print('Enter line')
line = input()
print('Line:', line)
```

#### Output

```shell
Enter line
Hello world - have a nice day
Line: Hello world - have a nice day
```

```c
#include <stdio.h>
int main() {
    char line[1001];
    printf("Enter line\n");
    scanf("%1000[^\n]s", line);
    printf("Line: %s\n", line);
}
```

- scanf("%1000[^\n]s", line); is roughly scan until end of the new line character or 1000 letters.
- [^\n ] - is a regular expression which says match everything expect for new line.
#### safe program

```c
#include <stdio.h>
int main() {r
    char line[1000];
    printf("Enter line\n");
    fgets(line, 1000, stdin);
    printf("Line: %s\n", line);
}
```

- fgets is part of the standard library.
- stdin - is the standard input file, usually in C has three basic files such as, 
	1. standard input.
	2. standard output.
	3. standard error.
- all of the three are named stdin, they are predefined constants in the kc standard library.
>  For a program to UPPERCASE we would read the input into the standard input and the uppercase it and then send it to the standard output, but in case if there is an error we send it to the standard error.
>  keyboard(stdin) -> output -> screen(stdout)
>                  -> error -> scrren (stderr)
### Read a File

```python
hand = open('romeo.txt')
for line in hand:
    print(line.strip())
```

#### Output

```shell
But soft what light through yonder window breaks
It is the east and Juliet is the sun
Arise fair sun and kill the envious moon
Who is already sick and pale with grief
```

```c 
#include <stdio.h>
int main() {
    char line[1000];
    FILE *hand;
    hand = fopen("romeo.txt", "r");
    while( fgets(line, 1000, hand) != NULL ) {
        printf("%s", line);
    }
}
```

- FILE is a type, it is declared in the stdio.h and * is the pointer operator.
- open from python is inspired from the fopen from C, here we use read mode while opening the file using the "r" argument.
- NULL is a constant which is defined the stdio.h

### Counted loop

```python
for i in range(5) :
	print(i)
```

#### Output

```shell
0
1
2
3
4
```

```c
#include <stdio.h>
int main() {
    int i;
    for(i=0; i<5; i++) {
        printf("%d\n",i);
    }   
}
```

- for (declare variable; condition to check on the variable; increment or decrement to the variable )

### Min/ Max problem

```python
maxval = None
minval = None
while True:
    line = input()
    line = line.strip()
    if line == "done" : break
    ival = int(line)
    if ( maxval is None or ival > maxval) :
        maxval = ival
    if ( minval is None or ival < minval) :
        minval = ival
        
print('Maximum', maxval)
print('Minimum', minval)
```

#### Output

```shell
5
2
9
done
Maximum 9
Minimum 2
```

```c
#include <stdio.h>
int main() {
    int first = 1;
    int val, maxval, minval;

    while(scanf("%d",&val) != EOF ) {
        if ( first || val > maxval ) maxval = val;
        if ( first || val < minval ) minval = val;
        first = 0;
    }

    printf("Maximum %d\n", maxval);
    printf("Minimum %d\n", minval);
}
```

> 5
> 2
> 9
> (EOF) - crtl+d
> Maximum 9
> Minimum 2

> 5 2 9
  (EOF)
  Maximum 9
  Minimum 2

- EOF is End Of File, for windows we use crtl+z and for linux we use crtl+d.
### Guessing Game

```python
while True:
    try:
        line = input()
    except:  # If we get EOF
        break
    line = line.strip()
    guess = int(line)
    if guess == 42:
        print('Nice work!')
        break
    elif guess < 42 : 
        print('Too low - guess again')
    else :
		print('Too high - guess again')
```

#### Output

```shell 
5
Too low - guess again
50
Too high - guess again
42
Nice work!
```

```c
#include <stdio.h>
int main() {
    int guess;
    while(scanf("%d",&guess) != EOF ) {
        if ( guess == 42 ) {
            printf("Nice work!\n");
            break;
        }
        else if ( guess < 42 ) 
            printf("Too low - guess again\n");
        else
            printf("Too high - guess again\n");
    }
	} 
```

> A very important concept here is that the python's elif is a mulit-way if statement but in C there is no multi-way

if you can see **else if** are two keywords meaning that, all the else if statements are nothing but nested if else statement. so now it should be actually intended like this.

```c
if(condition){
	...
}else{
	if(condition){
		...	
	}else{}
		if(condition(){
			...
		}
	}
}
```
> by convention we don't add that indentation but we use is without even thinking, but we should know that there is no multi-way if else
### Functions (call by value)

```python 
def mymult(a,b):
    c = a * b
    return c

retval = mymult(6, 7)
print('Answer:', retval)
```

#### Output

```shell
Answer: 42
```

```c
#include <stdio.h>
int main() {
    int mymult(); 
    int retval;

    retval = mymult(6,7);
    printf("Answer: %d\n",retval);
}

int mymult(a, b)
    int a,b;
{
    int c = a * b;
    return c;
}
```

- In C we specify the return type of the function before the function name, followed by the arguments inside the curly brackets.
- we also should mention the type of the parameters
- any variable that you define inside a function only lives within that function, here c variable only lives inside the myult function.

### SHOUT 

```python 
hand = open('romeo.txt')
for line in hand:
	print(line.strip().upper())
```

#### Output

```shell
BUT SOFT WHAT LIGHT THROUGH YONDER WINDOW BREAKS
IT IS THE EAST AND JULIET IS THE SUN
ARISE FAIR SUN AND KILL THE ENVIOUS MOON
WHO IS ALREADY SICK AND PALE WITH GRIEF
```

```c
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int main() {
    char line[1000];
    FILE *hand;
    int i; 
    hand = fopen("romeo.txt", "r");
    while( fgets(line, 1000, hand) != NULL )
        for(i=0; i<strlen(line); i++) 
            putchar(toupper(line[i]));
}
```

### Character Arrays
we must carefully understand the **size** of the character array, and not exceed it because nothing in C is *auto-extended*

```c
#include <stdio.h>
int main(){
	char x[10];
	int i;

	for(i=0; i<1000; i++){
		printf("%s\n", x);
	}
}
```

```shell
$ a.out
Segmentation fault : 11
```

In C if try to add characters more than what is allocated the program blows up. Code like this is the reason for 90% of the security vulnerabilities that occur in computing. This kind of code gives hackers to inject things into operating systems and routers. This why we don't programs in C.
### String/ Character Constants
- Languages like PHP, JavaScript and python treat single and double quotes nearly the same. Both create *string* constants.
- In C single quotes are single character and double quotes are character array.
- In C, a character is a byte - short (typically 8 bit) integer, single quotes character in C are far more like integers(ASCII).

```c
printf("%c %d\n", 'A', 'A');
```

```shell
$ a.out
A 65
```

- the size of a string in C array is not the length of the array.
- C uses a special character '\0' that marks the string end by convention.
- character arrays needs to be allocated an extra byte to store the line end character.
```c
#include <stdio.h>
int main() {
    char x[6];
    x[0] = 'H';
    x[1] = 'e';
    x[2] = 'l';
    x[3] = 'l';
    x[4] = 'o';
    x[5] = '\0';
    printf("%s\n",x);

    x[2] = 'L';
    printf("%s\n",x);

    x[3] = '\0';
    printf("%s\n",x);
}
```

> you have to terminate the string with '\0' because the C might go on to search for the terminating character into the memory until it blows up.


## References

[From Python to C - The Rosetta Stone Lecture](https://www.cc4e.com/lessons/python#)

