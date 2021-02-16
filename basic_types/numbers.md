# Numbers - Integers and Floats
Since computers store information as numbers, it makes sense that the next most fundamental data types are just that---numbers. Computers define two types for numbers: _Integers_ and _Floats_. You might recall the terms _whole numbers_ and _decimals_ from middle school math. Well, integers are essentially whole numbers (numbers that aren’t fractions or contain a decimal) while fractions / decimals are reserved for _floating point numbers_ (_floats_ for short).

## Example
Let’s look an example in Java:
~~~java
int num1= 10;
int num2 = -100000000;
long bigNum = 3000000000L;
float preciseNum = 2.5f;
double superPreciseNum = 2.3333333333333d;
~~~
The variables `num_1` and `num_2` are standard ints (shorthand for integer) because of their value. `big_num` is a `long` because it’s value is greater than what standard ints can hold. `precise_num` is a standard* floating point variable, while `super_precise_num` is to a `float` what a `long` is to an `int`.

We can see the different data types being specified in addition to the variable name. While the exact wording is different for each language that requires this, the concepts and their underlying values are usually still the same.
