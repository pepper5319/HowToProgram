# Strings
Oftentimes our programs don’t just deal solely with numbers or booleans, but also words and letters. So, we need a way to store characters like letters and symbols. On their own, these are in fact known as _characters_ (_chars_ for short), but if we "string" them together (see what I did there) we get what’s known as _Strings_.

Strings are usually defined by enclosing a sequence of characters in double quotes `""`.
## Example
Let’s look at an example in Python:
~~~python
my_str = "Hello, World""
my_num = 5
my_num_str = "5"
~~~
We can see `my_str` has a value of `"Hello, World"`, which is wrapped in double quotes*. The next variable, `my_num`, has a value that isn't wrapped in quotes, making it an integer, while `my_num_str`’s value is. It is important to note that in most languages you will not be able to perform any mathematical operations on a number that is a string.
## String Functions
You can perform a lot of different operations with strings. While not all of them are covered here, let’s go over some common ones**:

- _Concatenate_: Adding a string to the end of another string. Each language handles this differently, but here are a few examples that all equal "Hello, World":
  - Python: `my_str = "Hello, " + "World"`
  - Java: `var myStr = "Hello, ".concat("World");`
  - Rust: `let my_str = concat!("Hello, ", "World");`
- _Replace_: Replacing a specified character or string with another character or string. All examples equal "Heppo":
  - Python: `my_str = "Hello".replace("l", "p")`
  - Java: `String myStr = "Hello".replace("l", "p");`
  - Rust: `let my_str = str::replace("Hello", "l", "p");``
- _Substring_: Getting a portion of a string between two specified indices (positions in a string). The start(first) index indicates "select characters **including and after** this position", and the end(second) index indicates "select characters **up to** this position". All examples equal "llo, Wor":
    - Python (also called _slice_): `my_str = "Hello, World"[2:10]`
    - Java: `String myStr = "Hello, World".substring(2, 10);`
    - Rust (also called _slice_): `let my_str = &"Hello, World"[2..10];`
- _Format_: Replaces language specific codes with specified variables. This function can get a bit complicated depending on the language and has a lot of special syntax, so it’s recommended to do additional research into it in the language of your choice. Here is a Python example:
~~~python
location = "World"
msg = f"Hello, {location}"
~~~
