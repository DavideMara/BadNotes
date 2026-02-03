# Sign and magnitude

It uses one bit (the leftmost if big endian) to indicate the sign.

*“0”* indicates a `positive integer`, and *“1”* indicate a `negative integer`. The rest of the bits are used for the magnitude of the number.

For example:

$$
1001 1000 = -24
$$

If *1001 1000* is used to represent *positive numbers* the result will be

$$
1001 1000 = 152
$$

So if we consider the previous example we can represent with *n* bits

- From (-2^n-1 + 1) to (2^n-1 -1)
- and +- 0

So if again we take 8 bits :

from *-127*  to *+127*