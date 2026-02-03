# Integers

# *The standard and extended integer types.*

There are five signed integer types. Most of these types can be designated by several synonyms

- `signed char`
- `int`                             signed, signed int
- `short`                         short int, signed short, signed short int
- `long`                           long int, signed long, signed long int
- `long long` (C99)        long long int, unsigned long long, signed long long int

C defines only the *minimum* storage sizes of the other standard types:

- `short` *at last* 2 bytes
- `long` *at last* 4 bytes
- `long long` *at last* 8 bytes

Although the integer types may be larger than their minimum sizes, the sizes implemented must be in this order :

`sizeof(short) ≤ sizeof(int) ≤ sizeof(long) ≤ sizeof(long long)` 

---

## BOOLEAN

In C there is no `TRUE` or `FALSE`, the only certainty is that `0` is false

Any value different from `0` is true

For example: 

```c
if (3){
	printf(”YES\n");
}
else{
	printf("NO\n");
}
// it will print YES

if (0){
	printf(”YES\n");
}
else {
	printf("NO\n");
}
// it will print NO
```

**C99** introduced the `unsigned integer type_Bool` to represent Boolean truth values 

The Boolean value `true`  is coded as `1`, and `false` is coded as `0`

With the library `stdbool.h` in a program you can also use the *identifiers* `bool`, `true`, and `false` . 

The macro `bool`  is a synonym for the `type_Bool`, and `true` and `false` are symbolic constants equal to `1` and `0`

---

## CHARS

The type `char` is also one of the standard **integer types.**

However, the one-word type name `char` is synonymous either with `signed char` or with `unsigned char`, depending on the compiler.

It occupies **1 byte** of memory and you can check the correspondence in the [ASCII table](http://www.asciitable.com) 

Arithmetic with character variables are possible, it’s **up to the code to decide** whether the *program* interprets the number in a `char` variable as a character code or as something *else.*

Here an example:

```c
char ch = 'A'; // A variable with type char.
printf("The character %c has the character code %d.\n", ch, ch);
printf(”%c", ch + 1);
```