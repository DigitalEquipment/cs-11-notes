# Comments
---
## Inline
```cpp
//This is a comment
//Comment
```
## Block
```cpp
/* This is a comment */

/*
This comment
is much longer
*/
```
# Functions
---
- Functions are the building blocks of programs
- Functions can take inputs and return outputs
```cpp
int main(//arguments)
{
    //function code
    return ret_value;
}
```
- The main function represents a program's entry point. Other functions can be declared as such:
```cpp
double functionator(int conjunction, double junction)
{
    //function code
    double output;
    return output;
}
```
- The function `functionator` can be called in the program by typing `functionator()`. The function returns a type `double` and takes the arguments integer `conjunction` and double `junction`. At the end of its execution, `functionator()` will return double `output`.
# Output
---
## cout
```cpp
cout << "Hello, World!\n";
```
- Outputs `Hello, World!` to the standard output
## endl
```cpp
cout << "Foobar Kilroy" << endl;
```
- Flushes the buffer, then writes `\n` to the standard output
# Input
---
## cin
```cpp
cin >> stringname;
```
- Takes input and writes it to string `stringname`. Delimitated by whitespace.
	**Input** `String Name Johnson`
	**Output** `String`

```cpp
cin >> num
```
- Writes first argument to `int` variable `num`
	**Input** `14 23`
	**Output** `14`

```cpp
cin >> var1 >> var2;
```
- Writes second word to string 2.
	**Input** `String Name Johnson`
	**Output** `String Name`
## getline
```cpp
getline(cin, stringname);
```
- Writes entire `cin` input stream to `stringname`
	**Input** `String Name Johnson`
	**Output** `String Name Johnson`
# Iteration
---
## for()
---
- A `for()` loop takes 3 arguments.
```cpp
for(intitialize; condition; increment_decrement)
{
    //loopcode
}
```
During initialize, the for loop will create variables written there. Then, while looping, the for loop will verify the condition, then increment or decrement according to the code written.
## while()
---
- A `while()` loop takes one condition.
```cpp
while(condition_is_true)
{
    //loopcode
}
```
A while loop will run until the condition no longer equates to true.
## do{} while();
---
- A `do{} while()` loop is similar in operation to a while loop, with the single exception that the `while()` condition is tested after the loop code is executed instead of before.
```cpp
do {
	//loop code
} while(condition_is_true);
```
# Variables
---
- Variables are an essential part of programming. Variables store values that can be referenced, modified, and output. Variables can be hard defined in the program, be used as a modifiable storage spot, as a connector for user input, as a connector for output and more.
## Definitions
---
- Defines an integer variable and initializes it to `0`
```cpp
int var = 0;
```

- Multiple variables can be defined at once
```cpp
int var1 = 0, var2 = 1;
```

- A variable can be initialized using other variables
```cpp
int var1 = varX + varY;
```

*Failure to initialize a variable can lead to unpredictable results*
## Assignment
---
- Assigning is used to place a new value into the variable
```cpp
int var1 = 0; //definition
var1 = 5; //assignment
```

## Constants
---
- A constant is used for protected and unchanging values. `const` prevents a variable from being changed. Good writing practice dictates `const` variables should have capital names.
```cpp
int ex1 //regular integer
const int EX2 //constant integer
```
- Constants can be any type
```cpp
const int NUM = 5; //constant integer
const double DOUB = 13.23; //constant double
const string NAME = "John"; //constant string
```
## Types
---
### int
- A number with no fraction/decimals. Can be negative or zero.
```cpp
int var = 0;
```
### double
- Most common type used for [[Terminology#Floating Point|floating-point]] numbers. Can be negative, or expressed as scientific notation.
```cpp
double var = 0.0;
```
### unsigned
- `int` with no negative abilities
```cpp
unsigned positive = 15; //legal
positive = -4; //illegal
positive = 3.6; //illegal
```
### short
- `int` but with a smaller value range (-32768, 32767)
```cpp
short small = 12; //legal
small = 32768; //overflow
```
### unsigned short
- `unsigned` with `short` size. (0, 65535)
```cpp
unsigned short stupid_var = 15; //legal
stupid_var = -5; //illegal
stupid_var = 65536; //overflow
```
### long
- Either the same as `long long` or `int`, depends on compiler. 
```cpp
long big_var = 15; //legal
big_var = 9223372036854775808; //overflow if == long long
big_var = 2147483648; //overflow if == int
```
### long long
- Larger 8 byte variable
```cpp
long long big_var = 15; //legal
big_var = 9223372036854775808; //overflow
```
### float
- Shorter 4 byte version of double
```cpp
float decimal_variable = 3.14;
```
### auto
- Derives the variable type from its definition automatically.
```cpp
auto var = 6; //actually int
auto bar = 4.55; //actually double
```
## Strings
---
- Strings are essentially lists of characters that can be used for words, sentences, etc.
```cpp
#include <string>
string word = "Words!";
```
- Strings can have methods that allow for manipulations and other data to be pulled
### .substr()
- The `.substr()` method allows for pulling certain parts of the string out. It takes two arguments, the first for the starting position in the string, and the second for how much to pull from the string
```cpp
int position = 0;
int amount_of_characters = 1;
cout << word.substr(position, amount_of_characters); //outputs "W"
cout << word.substr(1, 3); //outputs "ord"
```
### .length()
- Returns the length of the string as an `int`
```cpp
cout << word.length(); //outputs 6
```
### .at()
- Returns the character at the position specified in a given string
```cpp
cout << word.at(3); //outputs "r"
```
### \[]
- Same as `.at`
```cpp
cout << word[3]; //outputs "r"
```
## Booleans
---
### bool
- The `bool` type represents a boolean variable, which is a variable that represents the `true` or `false` states.
```cpp
bool state = true;
```
## Arrays
---
### 1D Arrays
- An array can be any data type, and is declared by adding square brackets to the end of the variable. The number in the square brackets is the length of the array.
```cpp
int ary[5] = {6, 9, 4, 2, 0};
```
- In C++, all the values in an array can be set to 0 by declaring:
```cpp
int zer[7] = {0};
```
- An array will also auto-size to the number of initial values:
```cpp
int marget[] = {1, 2, 3, 4, 5, 6, 7, 8 ,9};
//Array is now sized 9
```
### 2D Arrays
- A 2D array is an array that has elements which contain arrays. They are declared by adding a second set of square brackets to the end of the declaration.
```cpp
int mlr[5][5] = {0};
```


# Math
---
## Arithmetic
---
### Addition
```cpp
x + y;
```
### Subtraction
```cpp
x - y;
```
### Multiplication
```cpp
x * y;
```
### Division
- If both numbers are `int`, no numbers after the decimal are preserved. 
```cpp
x / y;
```
### Remainder/Modulus
```cpp
x % y; //returns the remainder of x/y
```
### Increment
```cpp
x++; //x = x + 1
```
### Decrement
```cpp
x--; //x = x -1
```
## Useful Division and Modulus values
---

| n = 1729 | Value | Comment |
| --- | --- | --- |
| `n % 10` | `9` | `n % 10` is always the last digit of `n` |
| `n / 10` | `172` | Always `n` without the last digit |
| `n % 100` | `29` | Last two digits of `n` |
| `n / 10.0` | `172.9` | Doesn't discard fraction because of floating point |
| `-n % 10` | `-9` | Value is negative because argument is negative |
| `n % 2` | `1` | `n % 2` is `0` if `n` is even and `1` or `-1` if `n` is odd|

## Rounding
---
- To easily round a floating point number while converting to an integer, add 0.5 then convert
## Exponents and Roots
---
- Included in the `<cmath>` library
### sqrt(x)
- `√x` is expressed as `sqrt(x)
```cpp
#include <cmath>
int var1 = 100;
var1 = sqrt(var1)
```
### pow(x, n)
- x<sup>n</sup> is expressed as `pow(x, n)`
```cpp
#include <cmath>
int var1 = 10;
int var2 = 0;
var2 = pow(var1, 2)
```
# Comparison
---
## Operators
---
- Comparison and logical operators are used to perform logic operations
- When stacking conditions, you must use the boolean `&&` or the boolean `||`. An expression `0 < x < 5` will cause errors because if x is greater than 0, this will become 1 to represent true, which will then be less than 5. If x were to equal a number of 5 or greater, this expression will provide an incorrect return. The correct way to write this expression is `x > 0 && x < 5`.
### >
- The `>` comparison operator functions the same as it does in math. It outputs true if the first argument is greater than the second argument.
```cpp
int num = 15;
int other_num = 4;
int another_num = 15;
cout << (num > other_num) << "\n"; //outputs 1
cout << (num > another_num) << "\n"; //outputs 0

### >=
- The `>=` comparison operator is similar to `>`, except that equivalency also returns true.
```cpp
int num = 15;
int other_num = 4;
int another_num = 15;
cout << (num >= other_num) << "\n"; //outputs 1
cout << (num >= another_num) << "\n"; //outputs 1
```
### <
- The `<` comparison operator is the opposite of `>`.
```cpp
int num = 15;
int other_num = 4;
int another_num = 15;
cout << (num < other_num) << "\n"; //outputs 0
cout << (other_num < num) << "\n"; //outputs 1
cout << (num < another_num) << "\n"; //outputs 0
```
### <=
- The `<=` comparison operator is similar to `<`, except that equivalency also returns true.
```cpp
int num = 15;
int other_num = 4;
int another_num = 15;
cout << (num <= other_num) << "\n"; //outputs 0
cout << (other_num <= num) << "\n"; //outputs 1
cout << (num <= another_num) << "\n"; //outputs 1
```
### ==
- The `==` comparison operator will output true (1) if the arguments are equivalent
```cpp
int num = 15;
int other_num = 15;
int another_num = 42;
cout << (num == other_num) << "\n"; //outputs 1
cout << (num == another_num) << "\n"; //outputs 0
```
### !=
- The `!=` comparison operator will output true (1) if the arguments are **not** equivalent
```cpp
int num = 15;
int other_num = 15;
int another_num = 42;
cout << (num != other_num) << "\n"; //outputs 0
cout << (num != another_num) << "\n"; //outputs 1
```
### +=
- The `+=` equality operator will set the first argument equal to itself plus the second argument
```cpp
int num = 5;
int othernum = 7;

num += othernum;
cout << num << "\n"; //outputs 12
```
### ?
- `?` is the conditional operator.  Its usage is similar to `if else` statements.
- `var < num ? output : output2` can be read as `if var is less than num then output, else output2`
```cpp
out = in < 10 ? 0 : 1; 
/*
Is the Same as:
*/
if(in < 10)
{
    out = 0;
}
else
{
    out = 1;
}
```
### !
- `!` is the operator for `NOT`. Adding `!` ahead of operators, variables, etc. will invert the return
```cpp
int x = 15;
int y = 42;
cout << x == !y; //returns 1
cout << x !< y; //returns 0
```
### &&
- `&&` is a boolean `AND`. When added between comparisons, it passes each comparison through a logical `AND`
```cpp
if(num1 < 5 && num2 == 30 && num3 != 4)
{
    //Conditional Code, only runs if num1 is less than 5 AND num2 equals 30 AND num3 doesn't equal 4
}
```
### ||
- `||` is a boolean `OR`. When added between comparisons, it passes each comparison through a logical `OR`
```cpp
if(num1 < 5 || num2 == 30 || num3 != 4)
{
    //Conditional Code, only runs if num1 is less than 5 OR num2 equals 30 OR num3 doesn't equal 4
}
```
### Lexicographic Ordering
- When using operators on strings, strings will be ordered lexicographically. For instance, when comparing a string "Foo" to a string "Bar", "Bar" will be less than "Foo" because B comes before F in the alphabet. However, when comparing a string "Foo" to a string "bar", "Foo" will come first because uppercase letters are prioritized.
```cpp
string foo = "Foo";
string bar = "Bar";
string lowbar = "bar";

cout << foo > bar << "\n"; //returns 1
cout << bar > foo << "\n"; //returns 0
cout << foo > lowbar << "\n"; //returns 0
 ```
## Statements
---
### if()
- `if()` is the primary comparison statement. Code nested in an `if()` statement will only execute if the argument equals true.
- Can be read as "If `condition`, then `conditional code`"
```cpp
if(condition)
{
    //conditional code
}
```
### else if()
- `else if` adds the condition that an above `if()` statement fails its condition
```cpp
if(false_condition)
{
    //conditional code (doesn't run)
}
else if(true_condition)
{
    //conditional code (runs)
}
```
### else
- `else` executes code only if all `if()` and `else if()` statements above fail to execute
```cpp
if(false_condition)
{
    //conditional code (doesn't run)
}
else if(false_condition)
{
    //conditional code (doesn't run)
}
else
{
    //conditional code (runs)
}
```
### switch() {case}
- Switch cases can be used to replace long chains of `if else()` statements.
```cpp
int num = 0;

...

switch (num)
{
    case 1:
        cout << "Case 1\n";
        break;
    case 2:
        cout << "Case 2\n";
        break;
    default:
        cout << "Default Case\n";
        break;
}
```
- Multiple cases can also be assigned to a certain output:
```cpp
switch (num)
{
    case 1: case 3: case 5: case 7: case 9:
        cout << "Odd Case\n";
        break;
}
```
# Libraries
---
## C++ Standard Library Header Files

### iostream
- `<iostream>` adds standard input/output to your C++ project.
### cmath
- `cmath` adds a variety of complex math functions
### iomanip
- `iomanip` adds a variety of methods that allow for the manipulation and editing of IO