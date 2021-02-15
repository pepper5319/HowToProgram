# Bits and Bytes
Every computer (yes, every single one) is basically just a fancy rock that someone stuck electricity into and electricity came out. Now the way it handles that electricity is a bit more complicated, but that's just all it is. It helps if you imagine the rock as having a series of switches inside that can either be turned on or turned off (Hey, Just like the [Input and Output](https://github.com/pepper5319/HowToProgram/blob/master/fundamental_concepts/input_output.md) example from before!) and if those switches are turned on and off in a certain way or pattern, it could output a signal in another pattern that looks kind of like it just did math or something.

The way that these switches are represented in programming is through `bits`, the most basic way a computer can hold information because the value is quite literally `On` or `Off` in our processor (the fancy rock). In code the actual value is `1` or `0`. Now that's cool and all, but how are you going to get a number like "25" out of a `1` or `0`. Well, if you combine multiple bits together, and then assign each place value of the bit to equal a value that is _double_ that of the previous place value (starting at 1), you can turn our traditional numbers ([base 10](http://www.amathsdictionaryforkids.com/qr/b/base10system.html) numbers) into `binary` numbers ([base 2](https://www.expii.com/t/base-binary-numbers-9192) numbers).
```
11001 = 25
-------------------------------------------
1   1   0   0   1 - Bit value
16  8   4   2   1 - Place value
-------------------------------------------
As a math equation:
(1 * 16) + (1 * 8) + (0 * 4) + (0 * 2) + (1 * 1) = 25
16 + 8 + 0 + 0 + 1 = 25
16 + 8 + 1 = 25
25 = 25
```

### Bytes
Now that you understand how combining bits can result in different values, what can we do with those combinations? Well if you combine **8** bits together, you get what's called  a `byte` (if you combine 4 bits you get a `nibble`). Bytes are much easier for a human to understand because they can contain more data than just a `1` or `0`. If we take these bytes and apply and `encoding` to them (a way to interpret them), we can change them into letters, numbers, and symbols. For example, the `ASCII` encoding turns _h_ into `01101000`. As computers are able to handle more information in a much faster way, different encodings are able to interpret more bytes into single characters (the `UTF-8` Unicode encoding is basically the new standard and can handle up to 5 bytes per character!)
