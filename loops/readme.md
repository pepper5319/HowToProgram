# Loops
So far, all the code we've written and concepts discussed will run just once and exit when finished. While this is useful for one time operations with a single piece of data, this almost never happens in the real world. When you open a messaging app it doesn't just show you a single message and stop. What's going on behind the scenes is it's gathering your most recent messages with a specific person, going through each one and formatting it so it looks nice when on the screen, checking if there are any emojis it needs to display, and THEN shows you the messages. Using the correct terminology, your phone is running a _Loop_, or a statement that repeats code while a condition is met, to perform operations with your messages.

There are two major types of loops: a `while` loop and a `for` loop. Both of them are relatively easy to read across almost all languages. They follow the same logic as the [if statements](https://github.com/pepper5319/HowToProgram/blob/master/conditionals/readme.md#if-statements) from before, where it will run the block of code "inside" the loop as long as the condition is met, with the difference being that once it reaches the end of the block it **goes back** to the beginning of the block and checks the conditional again. If it is still true, it will run again.

## While
As the most basic loop, the `while` loop is essentially a repeating `if` statement. It reads "While this is true, do this". Here's an example in Python:
~~~python
x = 1
while x <= 10:
    print(x)
    x = x + 1
~~~
```
Output:
1
2
3
4
5
6
7
8
9
10
```
The above code defines variable `x` and sets its value to `1`. When the loop is reached in the program, it checks if `x` is _less than or equal_ to `10`. If it is, the program will run the block of code inside the loop. The block of code displays `x` to the user, and then _increments_(or increases) `x`'s value by 1, literally saying "set x equal to the current value of x plus 1".

### Infinite Loops
Now why do we need to update `x`? If we didn't, `x` would never reach a value of `10` and this loop would just run on forever, which we usually don't want to happen. These loops that "run on forever" are known as _infinite loops_, which sounds bad at first (and in a lot of cases are the root cause of bugs), but can be useful if handled carefully and used correctly. One of its main uses is for a game. We want our game to keep running, and can wrap our code in an _infinite loop_ to do so.

### break
But what if we wanted to exit our game? We could make the conditional in the loop check each time if the user presses an exit button, but that could be a bit taxing on the computer depending on how the program is set up. What if we were able to check **inside** the loop, and if the user did press an exit button we were able to "break" out of the _infinite_ loop? Well, the keyword `break` has got you covered.
~~~python
x = 1
while True:
    print(x)
    if x == 5:
        break
    x = x + 1
~~~
```
Output:
1
2
3
4
5
```
This `while` loop will do the same thing as before, but instead of checking if `x` is less than 10 each _iteration_ (each time the loop is run), it will just run forever because `True` is always true. Inside the loop we have an `if` statement that is checking if `x` equals 5. If it doesn't, the code below it will continue to run. If it _does_, then we go inside the statement and `break` out of the for loop. When that `break` statement is hit, none of the code below it **that is inside the loop** will run. The program will move onto the next line that is outside of the loop. If the `if` statement doesn't evaluate to true, we would just ignore it and continue running whatever is inside the `while` loop (increasing the value of `x` in this case).

### continue
While `break` is good if we want to exit the loop entirely, what if we just wanted to skip to the next iteration of the loop? That is, stopping wherever we are at in the loop and starting over at the next iteration. This can be achieved using the `continue` keyword.
~~~python
x = 0
while x < 10:
    x = x + 1
    if x == 5:
        continue
    print(x)
~~~
```
Output:
1
2
3
4
6
7
8
9
10
```
The above code will give us the same output as before **except** it skips over the number 5. This is because we check if `x` is 5, and if it is `continue` the loop by going back to the top of the block and checking the conditional again. In this instance we have to put `x = x + 1` at the beginning because if we left it at the end, it would never get called once `x = 5` because the loop would keep "restarting" and none of the code below it **that is inside the loop** will get called.

## For/Foreach Loops
A `for`/`foreach` loop is used primarily for two reasons; Do we want to go through numbers between 2 numbers (in a range), or do we want to go through each item in a list of items?

### Foreach loops
The syntax can be a little bit trickier to read in some languages, so we'll use Python as an example.
~~~python
for number in range(0, 10):
    print(number)
~~~
```
Output:
0
1
2
3
4
5
6
7
8
9
```
In this example, we are saying "for each `number` between 0 and 10 (most languages that use any kind of range functions have their max value as _non-inclusive_, meaning they go up to but **do not** include the max value) display the number to the user. Whatever you put immediately after the `for` keyword is a variable being defined (you can name it however you want) that is usually meant to be used inside the `foreach` loop. The `range()` function (we'll explain functions later) is essentially creating a list of numbers between the two specified numbers(`0` and `10` non-inclusive) and giving it back to us. We then say "for each number in that list, display it".

We mainly use `foreach` loops to _iterate_ (go through) each item in an iterable object like arrays, dicts (all will be discussed later), and even strings!
~~~python
for letter in "Hello, World":
    print(letter)
~~~
```
Output:
H
e
l
l
o
,

W
o
r
l
d
````

Another fun fact is you can use `break` and `continue` statements in `for` loops the same way you can in `while` loops.

### For Loops
While not used as frequently anymore, a `for` loop is a loop that goes through numbers as long as a boolean condition is met (usually if it is less than a number). Here's an example in Java:
~~~java
for(int i = 0; i < 10; i++){
    System.out.println(i);
}
~~~
```
Output:
0
1
2
3
4
5
6
7
8
9
```
What this `for` loop is saying is "for our `int`(integer) variable `i` starting at 0, and while `i` is less than 10, increase `i` by 1 (`i++` is shorthand for `i += 1` in Java) each iteration". These are commonly used as a way to track the indices of items in an array (discussed later) and access them, but in that situation it would be much easier to use an iterator of some kind, usually through a `foreach` loop.
