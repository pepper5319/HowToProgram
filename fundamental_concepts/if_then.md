# If this Then that
If you were driving and pressed the brakes on a car, then what happens? If you were getting a phone call and pressed "Answer", then what happens? If you pressed "Ignore", then what? While I said that `Input` and `Output` are the two most fundamental concepts in programming, the concept of `If this Then that` (I'll just call it `ITTT`) it's probably closer to being the most fundamental. It's the backbone behind every nearly every single program written, and very rarely do you find one that doesn't use it in some form or fashion.

### Example 1
Lets look at some pseudocode (or fake code) that better shows `ITTT` in action.
```
I have a SHAPE
IF my SHAPE is a CIRCLE
  THEN roll the SHAPE
IF my SHAPE is a SQUARE
  THEN stack the SHAPE
```
Looking at the pseudocode, what decisions are going to be made? To simplify it more, `If` my `SHAPE` is a `CIRCLE`, `Then` what happens to my shape? `If` it's a `SQUARE`, `Then` what happens? What happens if my `SHAPE` is a `TRIANGLE` (_answer: nothing happens since we aren't checking if it's a TRIANGLE_)? These decisions are made using the `ITTT`.

### A Very Important Note
While we will see examples of this later, but it is important to remember when using this concept to be **specific** and **explicit**. There's a well known programming joke that shows why:
> A wife says to her husband, a computer scientist:
“Could you please go to the market and buy a carton of milk and if they have eggs please buy 6”
So the husband goes to the supermarket and comes back with 6 cartons of milk
When she sees that the wife asks: “Why did you do that?”
And the husband replies: “Well they had eggs.”

In pseudocode, the wife's request would look something like this:
```
IF the market has eggs:
  THEN buy 6 cartons of milk (what??)
```
While context is usually easy for us monkeys to pick up on, a computer has no idea what you are talking about. Always keep this in mind when writing a program.
