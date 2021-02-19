# Operators
Operators in programming languages are used to perform calculations; they are often very similar to the operations you find in math, such as addition or subtraction. There are three kinds of basic operators, _Arithmetic_ Operators, _Comparison_ Operators, and _Logical_ Operators.

## Arithmetic Operators
The most recognizable operators. Deals almost exclusively with numbers and performs traditional mathematical operations.
- `+`: Addition
- `-`: Subtraction
- `*`: Multiplication
- `/`: Division
- `%`: Modulo(the remainder after division)
## Comparison Operators
Takes two inputs and compares the two, returning True or False depending on the operator and the value of the inputs.
- `==`: Is Equal? - Checks if two variables are equal to each other
- `!=`: Is Not Equal? - Checks if two variables are **not** equal to each other
- `<=`: Less Than or Equal? - Checks if a variable is greater than or equal to another variable
- `>=`: , Greater Than or Equal? - Checks if a variable is less than or equal to another variable
- `<`, `>`: Less Than?, Greater Than? - Usually used for comparing numbers
~~~python
x = 5
y = 10

is_equal = x == y         # False
is_not_equal = x != y         # True
is_gte = x >= y         # False
is_lte = x <= y             # True
is_gt = x > y             # False
is_lt = x < y             # True
~~~

## Logical Operators
Takes boolean inputs, returning True or False depending on the operator and the value of the inputs.
- `!`: Not - Switches the True/False input to the opposite value(ie `!True = False`)
- `&&`: And - Returns True if **both** inputs are True
- `||`: Or - Returns True if **one or both** inputs are True
~~~rust
let inp_1 = true;
let inp_2 = false;

let a = inp_1 && inp_2;    // false
let b = inp_1 || inp_2;        // true
let c = !(inp_1 && inp_2);     // true
~~~

## Assignment Operators
If we want to update a variable to be equal to it's previous value plus another value, we could write it like `x = x + 1`. However most languages have a shorthand way of doing this using _Assignment_ operators, and can be used with any _Arithmetic_ operator. 
```
x += 1
x -= 1
x *= 1
x /= 1
x %= 1
```


## Example
You can chain all of these together to get more and more complex logic, and things can quickly look confusing when first learning. An important thing to remember is that like in math, these operators usually follow the same **Order of Operations** (treat _And_ as multiplication and _Or_ as addition)
Here’s an example in Rust:
~~~rust
let inp_1: i32 = 5;
let inp_2: i32 = 10;

let a: bool = ((inp_1 * 2) >= inp_2) && ((inp_2 % 2 == 0) || (inp_1 % 2 == 0));     // true
~~~
Here, we are checking a few things. In the first set of parentheses `((inp_1 * 2) >= inp_2)` we are checking if double the value of `inp_1` is greater or equal to `inp_2`. If it is, this first statement evaluates to `true`. In the second set of parentheses ` ((inp_2 % 2 == 0) || (inp_1 % 2 == 0))` we are checking if either `inp_2` or `inp_1` are _even_ numbers. If at least one of them is, this second statement evaluates to `true`. If **both** statements are `true`, the entire equation evaluates to `true` and the result gets stored in the variable `a`.

_Note: The exact syntax of these operators changes for each language (The _And_ (`&&`) operator is literally `and` in Python), so be sure to double check what they look like in the language of your choice._
