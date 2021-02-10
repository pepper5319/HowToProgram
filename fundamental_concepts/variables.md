# Variables
`Variables` are another fundamental programming concept that allows us store information for later use.

## Basic Idea
Imagine you had a box, named `Box`, and you put something in it, let's say a `Ball`. You then give the box to a computer and say "Bounce `Box`". Well, the computer does understand some things without us having to specify. It understands that `Box` is just holding something, so it will check inside and see `Ball` and attempt to bounce it.

Our box would be a `Variable` named `Box`, and `Ball` would be the data stored inside it, or it's `Value`.
_Note: While nothing is technically "stored" in the variable, it's MUCH easier to think of it this way, at least when starting off._

If we were to look at this as pseudocode (a little more advanced than before), it would look something like this:
```
let box = "ball"
Bounce(box)
```
Ignoring the syntax (the language specific words/characters used to write code), lets look at the first line. We are telling the computer "Let our variable `box` equal a value of `"ball"`". Anytime we refer to `box`, the computer will "look inside" the variable and see the value `"ball"`. In the second line, it then passes `box` to a function (don't worry about what this is, we'll learn about it later) called `Bounce()` as an `Input` (remember what that is?), which will do something. It doesn't do something with the actual `box` variable, it does something with the value stored in it: `"ball"`.

## Variable Data Types
It's trash day, and you have two kinds of bins: A recycling bin, and a trash bin. As the name indicates, one only holds recyclable items, while the other only holds regular trash. You know this just from the name, I know this, but the computer doesn't know this. Remember, we monkeys understand context, but computers don't. So we have to tell it what kind of items the bins can store.

If the bins were variables and we wanted to specify the kind of items they were allowed to hold, we would specify the `type` or `data type`. Many older languages require you to do this, however many newer ones don't. It is usually good practice to specify the `data type` when writing a `variable` for the first time. Let's look at some pseudocode:
```
let recycle_bin: Recyclable = "a recyclable item"
let trash_bin: Trash = "a trash item"
```
We can see here that the `type` of items that our variable `recycle_bin` is allowed to hold are `Recyclable` items, and only `Trash` items are allowed to go into the `trash_bin` variable. What would happen if we put a `Trash` item in `recycle_bin`? Well, in most programming languages it would tell you "Only `Recyclable` items are allowed in `recycle_bin`". However other's might not do anything at first, but if you try and use `recycle_bin` as an `Input` for code that can only handle `Recyclable` items, and you have a `Trash` item stored, then all kinds of things can go wrong and break, or you'll get an unexpected `Output`.

Every programming language has built in `data types` that we will look at in the next section, but you can create your own too if you want.
