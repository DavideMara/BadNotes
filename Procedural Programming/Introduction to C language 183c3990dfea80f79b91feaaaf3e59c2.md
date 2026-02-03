# Introduction to C language

C is a high-level general-purpose, procedural language.

> Dennis Ritchie first devised C in the 1970s at AT&T Bell Laboratories in Murray Hill, New Jersey, for the purpose of implementing the `Unix operating system` and utilities with the greatest possible degree of indipendence from specific hardware platforms.
> 

The key characteristics of the C language are the qualities that made it suitable for that purpose

- Source code portability
- The ability to operate “close to the machine”
- Efficiency

As a result, the developers of Unix were able to write most of the operating system in C, leaving only a minimum of system-specific hardware manipulation to be coded in assembler

> C’s ancestors are the typeless programming languages
BCPL (the Basic Combined Programming Language), developed by Martin Richards; and B, a descendant of BCPL, developed by Ken Thompson.
> 

A new feature of C was its variety of data types like characters, numeric types, arrays, structures and so on.

C has few hardware-dependent elements. For example, the C language proper has no file access or dynamic memory management statements. No input/output. Instead the extensive standard C library provides the functions for all of these purposes

## Virtues of C

- **Fast** (it’s a compiled language and so is close to the machine hardware)
- **Portable** (you can compile the program to run on just about any hardware platform)
- The language is **small** (unlike other languages)
- **Mature** (a long history and lots of resources and experience available)
- There is a **direct access to memory**
- You have access to **low-level system features** if needed

## Standards

- K & R C (Brian Kernighan and Dennis Ritchie)
  -1972 First created by Dennis Ritchie
  -1978 The C Programming Language described
- ANSI C
         1989 ANSI X.159-1989 aka `C89` - First standardized version
- ISO C
- 1990 ISO/IEC 9899:1990 aka `C90` - Equivalent to `C89`
- 1995 Amendment 1 aka `C95`
- 1999 ISO/IEC 9899:1999 aka `C99`     —→ `gcc file.c -std=c11` for example
- 2018 ISO/IEC 9899:2018 aka `C18`

---

# The structure of C programs

In C, programs are built using **functions**—reusable blocks of code that perform specific tasks. Key points:

- **Design**: Each function should have a clear, singular purpose.
- **Structure**: Functions **cannot be nested** (no functions inside other functions).
- **Execution**: Functions contain **statements** that run sequentially. These can be grouped into **blocks** (using `{ }`) for organization.
- **Libraries**: Use pre-built functions (like `printf()`) or create custom ones.
- **Main Function**: Every C program **must** define `main()`, the starting point when the program runs. `main()` acts as the "control center," calling other functions as needed.

In short, `main()` launches the program, and tasks are divided into functions that work together.

> C is imperative and procedural, the instructions  are grouped into functions
> 

So for example: 

![Screenshot From 2025-02-17 11-10-25.png](Introduction%20to%20C%20language/Screenshot_From_2025-02-17_11-10-25.png)

---

`gcc -o mainfile mainfile.c`  does :  `gcc mainfile.c` ——> `target program a.out`

## Modular programming

![The stack of interpretation ](Introduction%20to%20C%20language/image.png)

The stack of interpretation 

Unlike procedural programming, modular programming is a software design technique that emphasizes separating the functionality of a program into independent, interchangeable modules, such that each contains everything necessary to execute only one aspect of the chosen functionality

For example :

![Screenshot From 2025-02-17 11-18-51.png](Introduction%20to%20C%20language/c1d7d56e-0842-4b08-9df5-a29af47a025d.png)

On the terminal line we will had `gcc -o executable mainfile.c helloc`