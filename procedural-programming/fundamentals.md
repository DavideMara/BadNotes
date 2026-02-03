# Fundamentals of language

# Comments

The are 2 ways to insert comments in C:

- **block comments:** it begins with `/*` and end with `*/`
- **line comments:** begin with `//` and end with the new line character

So you can use the `/*` and `*/` delimiters to begin and end comments within a line, and to enclose comments of **several lines**. Or you can use `//` to insert comments that fill an **entire line**, or to write source code in a two-column format, with program code on the left and comments on the right

# Character sets

In the C language are defined two character sets:

- the `source character` set is the set of characters that **may be used in C source code**
- the `execution character` set is the set of characters that **can be interpreted by running program**

> So we are talking about for example the *Latin alphabet,* the decimal digits, the punctuation marks and the five white-space characters (space, horizontal tab, vertical tab, new line and form feed)
> 

# Identifiers

With `identifiers` we are refer to names of variables, function, macros , structures and other objects defined in a C program. Identifiers can contain the following characters:

> Identifiers are case-sensitive
> 
- The letters in the basic character set, `a-z` and `A-Z`
- The underscore character, `_`
- The decimal digits `0-9` , although the first character of an identifier must not be a digit

## Reserved Keywords

The following **44 keywords** are reserved in C, each having a specific meaning to the compiler, and must not be used as identifiers

| `auto` | `else` | `long` | `switch` |
| --- | --- | --- | --- |
| `break` | `enum` | `register` | `typedef` |
| `case` | `extern` | `return` | `union` |
| `char` | `float` | `short` | `unsigned` |
| `const` | `for` | `signed` | `void` |
| `continue` | `goto` | `sizeof` | `volatile` |
| `default` | `if` | `static` | `while` |
| `do` | `int` | `struct` | `_Packed` |
| `double` |  |  |  |

for example:

```c
// The following examples are valid identifiers
x
dollar
While
error_handler
scale64
//The following are not valid identifiers
1st_rank
switch
y/n
x-ray
```

When choosing identifiers in your programs, remember that many identifiers are already used by the C standard library (for example the name of library functions). 

> There is no limit on the length of identifiers. However most compilers consider only a limited number of characters in identifiers to be significant : 31 or 63
> 

---

# Scope and Binding

## Identifier scope

The *scope* of an identifier refers to that part of the translation unit in which the identifiers is meaningful. Basically the identifier’s scope is that part of the program that can “**see**” that identifiers.

> In C, an identifier **must be declared** before being used (except for labels)
> 

The **type** of scope is determined by the location at which you declare the identifier.

### File scope

Variables and function that are declared outside every function. They are **visible** from the **point of declaration** to **the end of the file.** If declared with`static` , they are visible only in the current file.

Example code:

```c
#include <stdio.h>

int globale;  // File scope

void funzione() {
    globale = 5;  // OK
}
```

### Block scope

Variables declared inside a block `{ }` . They are **visible** from the **point of declaration** to the **closure of the block** `}` 

Example code:

```c
{
    int x = 10;  // x has a block scope
    printf("%d", x);  // OK
}
printf("%d", x);  // ERRORE: x is not visible here
```

### Function scope

It applies only on the **labels** used with `goto` . The label is **visible throughout the function**, even before his first declaration

Example code:

```c
void funzione() {
    goto label;  // OK if the label is declared later
    label: printf("Salto qui");
}
```

### Function parameter scope

Function parameters are only **visibile** **inside the function**

```c
void somma(int a, int b) {
    int c = a + b;  // a e b visibili solo qui
    printf("%d\n", c);
}
```

> If you write outside the function  `print(”%d”, a);` ,  it’s an error: `a` doesn’t exist there
> 

### Global vs Local Shadowing

A **local** variable with the **same name as a global one** hides it 

```c
int x = 1;  // file scope

void f() {
    int x = 2;  // block scope, hides the global one
    printf("%d\n", x); // print 2
}
```

> If you **want to force the use globally**, you can use `::x` in C++ but in C you can only **rename** and move.
> 

## Binding

The **binding (process)** is the **association** between a name (like `x` ) and the object/program it names  (like a variable, function, type, ecc..).

> *Binding time* is the time which a biding is created or the time at which any implementation decision is made. On the other hand the textual region of the program in which a binding is active is its *scope*
> 

In C, this association is made in compilation stage: in C is determined statically, so at compile time

```c
int main(){
	int x= 1, y= 2, z = 3;
	printf(" x = %d, y = %d, z = %d \n ", x, y, z);
	  
```