17-05-2025 17:36:36

Status :

Tags :

# Introduction to Excel

### Create, Save and Navigate 
- talk about workbook and worksheet - rename worksheet
- cells, columns and rows
- create a columns of names and subjects
	- tell about data types
	- `enter` - move down to the next cell
	- `tab` - move right to the next cell
	- drag down the right bottom to auto fill
### Formulas and Function
- create mark columns with `=` and do a operation
- talk about functions
- introduce the `=rand()` and `=randbetween()`


### Cell References
- create a new sheet called Summary, and store full marks in a cell
- cell reference
	- Relative cell reference
		- A relative cell reference is the default type. 
		- When you copy a formula containing relative cell references to another cell, Excel automatically adjusts the references to match the new location `=A1+B1`
	- Absolute cell reference
		- An absolute cell reference always refers to the same cell, regardless of where you copy the formula.
		- You make a cell reference absolute by preceding both the column letter and row number with a dollar sign ($).
		- `=B1*$A$1` - A1 will never change.
		- create summary page
			- `=(B2/100)*(Summary!$B$2)`
	- Mixed cell reference
		- A mixed cell reference is a combination of relative and absolute references. Either the row or the column is fixed, while the other is relative.
		- You create a mixed reference by placing a dollar sign ($) before either the column letter or the row number.
		    - `$A1` - the column is absolute, the row is relative
		    - `A$1` - the row is absolute, the column is relative

### Reference Operators
- generate 5 subjects, insert columns to the left of maths
- after converting written marks (out of 70) to 100 in other column round the decimals with number data type.
- conditional formatting

### Basic functions
1. Total - `=sum()`
2. for the functions `average()` `=min()` and `=max()`
	1. create columns and rows for average, minimum and max for all subjects with total
	2. and use subtotal for others
3. before doing count - make a student absent and some subjects
	1. `=count()` for present
	2. `=countblank` for absent
	3. `=counta()` for total students

### Strings
1. new worksheet named biodata
2. get names from student marksheet
3. create rollno
4. `=concat()` for email
5. play with other functions as separate columns

### Date
1. create DOB column in biodata
2. show the 0 - date and explain
3. assign dates
4. show conversion with other datatypes
5. show which weekday is the DOB using `=weekday()`
6. show 10 workdays after using `=workdays()`
7. show working days between

### Basic function IF and SUMIF
1. create a coaching class column in Summary
2. use if for the average of every subject to determine if we need coaching class or not.
3. `=IFS(L2>450, "A", L2>400, "B", L2>300, "C", L2>250,"D", L2>200, "E", TRUE, "F")`
4. Total calculation without fail marks `=SUMIF(G2:K2, ">35")` where the condition is for every cell not the sum's output
5. explain sumif with a sales example.

### Vlookup
- use vlookup to make a report card on the summary page, where name on one block will search and return the specific mark.
- `=VLOOKUP(lookup_value, range/table to look at, index of the column where the value must be returned, approx match TRUE/FALSE`

### Hlookup 
- we will use hlookup to compare students mark with the horizontal data in the summary page for every subject.
- `=HLOOKUP(C13,B1:H7,2,TRUE)`
### Home work
1. Union
2. networkdays and workday with weekends included
3. 
## References


