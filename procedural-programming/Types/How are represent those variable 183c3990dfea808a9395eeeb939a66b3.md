# How are represent those variable?

# *THE NUMERAL SYSTEM*

In mathematics and digital electronics is typical to use the *binary* and the *hexadecimal*

## Binary Numeral System

A *binary* number is a number expressed in the binary numeral system or base-2 numeral system which represents numeric values using two different symbols: typically `0` (zero) and `1` (one).

> Usually the binary numeral system is implemented in digital circuitry using logic gates, is also internally used by almost all modern computers and computer-based devices.
> 

Each digit is referred to as a `bit` . 

$$
Example : 1001 = 1*2₀+0*2₁++0*2₂+1*2₃ = 1+0+0+8
$$

## Hexadecimal Numeral System

*Hexadecimal* (also base 16, or hex) is a positional numeral system with a **radix**, or base, of **16**. It uses sixteen distinct symbols, most often the symbols *0–9* to represent values *zero* to *nine*, and **A, B, C, D, E, F** (or alternatively a, b, c, d, e, f) to represent values *ten* to *fifteen*.

> Hexadecimal numerals are widely used by computer system designers and programmers. As each hexadecimal digit represents four binary digits (bits), it allows a more human-friendly representation of *binary-coded* values.
> 

One hexadecimal digit represents a `nibble` (*4 bits*), which is half of an `octet` or byte (*8 bits*).

## How many numbers can i  represent ?

*Form 0 to (`2^n - 1`)*

So with 8 bits (one `byte`  ):

               0 to 255 —>[0 ; 2^16-1]

0000 0000 to 1111 1111

However we can also represent negative numbers in 2 different ways:

[Sign and magnitude](How%20are%20represent%20those%20variable/Sign%20and%20magnitude%20183c3990dfea806093bdfadcb08eb9b1.md)

[Two’s complement](How%20are%20represent%20those%20variable/Two%E2%80%99s%20complement%20183c3990dfea80138421cb85edc482b9.md)

## And how are stored those numbers ?

We need to talk about Endianness that refers to the sequential order used to interpret a range of bytes in computer memory as a larger. composed word value. 

> It also describe the order of byte transmission over a digital like
> 

Words may be represented in **big-endian** or **little-endian** format, depending on whether bits or bytes or other components are numbered form *the big end* (most significant bit) or *the little end* (least significant bit).

 

---

## THE MEMORY REPRESENTATION

They are stored in an array of bytes, and every byte has its logical address ( a positive number)

A **logical address** is the **address** at which an item appears to reside from the perspective of an executing application program

![Screenshot 2025-01-23 120949.png](How%20are%20represent%20those%20variable/1fef5968-2373-4e95-a635-c9b208d853f8.png)

## BIG ENDIAN, LITTLE ENDIAN

![image.png](How%20are%20represent%20those%20variable/image.png)

## To sum up

![image.png](How%20are%20represent%20those%20variable/image%201.png)