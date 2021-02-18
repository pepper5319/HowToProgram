# Conditionals
Now it's time to learn how to make our code actually do stuff. Recalling back to the [If this Then that](https://github.com/pepper5319/HowToProgram/blob/master/fundamental_concepts/if_then.md) article, we use the concept of If this Then that to make decisions as to what operations we can perform with our data in our code. We make these decisions by writing statements that evaluate a boolean condition and choses which "path" to take depending on its value. These statements are known as _Conditionals_.

## If Statements
The first statement we can use is called an _if statement_. In most languages, the syntax and structure are very similar and relatively easy to read.
~~~python
# Python
if x % 2 == 0:
    print("Even")
~~~
~~~java
// Java
if (x % 2 == 0) {
    System.out.println("Even");
}
~~~
~~~basic
' Visual Basic
If x % 2 == 0 Then
   Console.WriteLine("Even");
End If
~~~
In each of these examples, the `if` statement is checking if the expression after the `if` keyword evaluates to true, which happens in this case when the variable `x` is an even number. If that expression is indeed true, then the program will run anything "inside" the `if` statement (either anything inside the curly brackets (`{...}`) or indented after the statement depending on the language). In this case, it just displays "Even" to the user.

## Else Statements
Now if we run the above example but `x` isn't an even number (`x % 2 = 1`), what will happen? Currently...nothing. The program will just see that the statement evaluates to false and moves on to the next line that **isn't** inside that `if` statement. So, what if we want to do something when that statement is false? We could change the boolean conditional to be `x % 2 != 1`, but we want to keep that first `if` statement. Instead, we could add an `else` statement afterwards.
~~~python
# Python
if x % 2 == 0:
    print("Even")
else:
    print("Odd")
~~~
~~~java
// Java
if (x % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
~~~
~~~basic
' Visual Basic
If x % 2 == 0 Then
    Console.WriteLine("Even");
Else
    Console.WriteLine("Odd");
End If
~~~
These `else` statements extend our conditional to say "If x is even, show 'Even', or else, show 'Odd'". You put `else` statements directly after `if` statements, never before.

## Else-If Statements
Now this is all fine and dandy, but this means we can only take two possible paths: If `x` evaluates to this value go this way, or go this way if it evaluates to any other value. What if we wanted to check and see if it's another specific value, let's say a multiple of 3. We could change the `if` statement to be `if x % 2 == 0 || x % 3 == 0`, but we want it to show something other than "Odd" or "Even" for a multiple of 3. We could use _nested_ `if-else` statements (`if-else` statements inside other `if-else` statements):

~~~python
# Python
if x % 2 == 0:
    print("Even")
else:
    if x % 3 == 0:
        print("Multiple of 3")
    else:
        print("Odd")
~~~

This conditional is saying "If x is even, show 'Even', or else, if x is a multiple of 3, show 'Multiple of 3', or else, show 'Odd'". While this works, it is a bit lengthy and can be confusing with figuring out the exact possible path. We can shorten this and make it a bit clearer with `else if` statements.

~~~python
# Python
if x % 2 == 0:
    print("Even")
else if x % 3 == 0:
    print("Multiple of 3")
else:
    print("Odd")
~~~
~~~java
// Java
if (x % 2 == 0) {
    System.out.println("Even");
} else if (x % 3 == 0) {
    System.out.println("Multiple of 3");
} else {
    System.out.println("Odd");
}
~~~
~~~basic
' Visual Basic
If x % 2 == 0 Then
    Console.WriteLine("Even");
ElseIf x % 3 == 0 Then
    Console.WriteLine("Multiple of 3");
Else
    Console.WriteLine("Odd");
End If
~~~
Now our conditional says "If x is even, display 'Even', or if x is a multiple of 3, display 'Multiple of 3', or else, display 'Odd'".

These statements are great if you need to specify multiple possible paths that your program can take, and you can have as many as you want (doesn't mean you should though). `else-if` statements go in between `if` and `else` statements, never before `if` and never after `else`.
