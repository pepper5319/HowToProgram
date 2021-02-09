# How To Program for people who've never programmed before
This is an incomprehensive guide for people who've never programmed on how to get started programming in any language. *This guide is written by a monkey who can computer, so everything will be explained as simply as possible.*

## What you need to know
The following are the concepts one should learn **in order**, as each concept builds off the previous, at minimum in order program a computer. One should think of these not as things one needs in order to write code in a specific language, but rather as tools one needs under their belt in order to solve problems.

### Fundamental Concepts
1. Understand what **Input** and **Output** are
2. Understand **IF** *this* **THEN** *that* concept
3. Understand what **Variables** are

### Programming Basics
1. Basic Data Types
    1. Booleans
    2. Integers
    3. Strings
2. Operators
    1. Arithmetic `+, -, *, /, %(modulus)`
    2. Comparison `==, !=, <, >, <=, >=`
    3. Logical `!, &&, ||`
3. Control Flow
    1. `If` statements
    2. `Else` statements
    3. `Else If` statements
4. Loops
    1. While/Do-While
    2. For Loop
    3. For-each Loop
### Milestone Project 1
Write the game FizzBuzz: 
- Loop through numbers 1 to 20. 
- If a number is a multiple (can be evenly divided) of 3, output "Fizz".
- If a number is a multiple 5, output "Buzz".
- If a number is a multiple 3 and 5, output "FizzBuzz".
- If a number is a multiple of neither 3 nor 5, output just the number.
```
1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, FizzBuzz, 16, 17, Fizz, 19, Buzz
```
### Intermediate Concepts
1. Intermediate Data Types
    1. Floats
    2. Arrays/Lists/Tuples
    3. Dictionaries
    4. Structs/Enums
2. Functions
    1. Parameters and Arguments
    2. Returning values
3. Classes
    1. Constructors
    2. Member Variables/Functions
    3. Instances
### Milestone Project 2
Write a Restraunt Management Program
- Have a class called `Restaurant`
- Have a member variable that holds a collection of menu items and their prices
- Write a function called `display_menu` that when called, outputs each item and their price, as such
```
Cheeseburger: $3.00
French Fries: $1.00
Milk Shake: $2.50
```
- Create an instance of `Restaurant` and a few menu items.
- Call the function `display_menu`
