# Booleans - True or False
A _boolean_ is the simplest data type a computer can use to describe information, because it can only have two possible values: `Yes` or `No`. In most programming languages, this is written as `True` or `False`, but the idea can be expressed in so many ways. _Yes_or _no_, _on_or _off, one or zero, _Yin_or _Yang_. The idea is the same: Is the data `True` or is it `False`?
### Example
Let’s look at some actual code (written in Python 3) to get a clear picture of booleans:

~~~python
is_big = True
is_small = False
if is_big == True and is_small == True:
    print(“How is that possible??”)
~~~

What’s going on here? Well, ignoring what’s happening in the last two lines (we’ll get more into detail on them later), we are creating two variables---`is_big` and `is_small`---and assigning them the boolean values _True_ and _False_. In the third line (don’t worry about specifics yet), we are checking if `is_big` is equal to `True`, and if `is_small` is also equal to `True`, and printing a message for the user to see. There are different ways of making this check in Python, but if you recall from [If this Then that](https://github.com/pepper5319/HowToProgram/blob/master/fundamental_concepts/input_output.md), you can think about it like this:

> If `is_big` is `True` and `is_small` is `True`, then show “How is that possible??”

In other words, “if it’s big and it’s small, then ask the user ‘How is that possible’”
