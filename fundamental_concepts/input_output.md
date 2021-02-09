# Understanding Input and Output
While you might not necessarily see the terms `Input` and `Output` too much while writing code, you will definitely come across concepts that are some form of either, like 'return values' or 'parameters' (these are discussed later). These are the two most fundamental ideas not just behind how code works, but also how a computer actually works and functions.

### Example 1
Imagine you have a `switch` and a `light` that's turned off in a room. When you flip the `switch` up, what should happen to the `light`? It turns on, right? When you flip the `switch` down, what happens? The `light` will turn off. While this is oversimplified, you are essentially giving information (the `switch` is up or down) and getting back information (the `light` is on, or the `light` is off).

Now, replace `switch` with `Input` and `light` with `Output`, and you have a very basic example of the two concepts. If you pass (_give_) an `Input` to some sort of machine or program, you will be returned (_receive_) some sort of an `Output`. The machine or program can do a lot of work to the `Input` before giving an `Output`. Here's another example.

### Example 2
Let's say you are playing a video game and you press a button on your controller to make the player jump. What would the `Input` be? It would be pressing the jump button on the controller. Now what would the `Output` be? The player jumping. Now, the program that handles how the player jumps does a little bit more than just reads your button press and moves the player up. It's going to look at a number of different factors, like "How long was the button held for", "Can the player even jump", "How high should the player jump", before calculating where the player moves to in the game using those factors, and then actually moving them. In this case, the program that handles the player jumping actually handles **multiple** `Inputs`, and gives a single `Output`: The player's new position (probably up in the air a bit). That `Output` position can then be used as an `Input` in another program that will actually display the player in the position (possibly over time so it looks nice and smooth) for you to see onscreen.

While programs can quickly get complicated with multiple `Inputs` and `Outputs` and what the program actually does with those `Inputs` and where those `Outputs` go, it's important to remember it all just boils down to the following:

An `Input` is passed to a program. The program does something. The program returns an `Output`.
