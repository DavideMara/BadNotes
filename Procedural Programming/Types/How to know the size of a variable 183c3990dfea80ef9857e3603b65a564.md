# How to know the size of a variable

## SIZEOF

To obtain the exact size of a type or a variable, use the `sizeof` operator. The expressions `sizeof(type)`. This expression *yield* the **storage size** of the object or **type in bytes**. If the operand is an **expression**, the size is that **the expression’s type**

```c
int ilndex;
ilndex = 1000;
```

Here the `sizeof(int)` and `sizeof(ilndex)` returns 4

## LIMITS

You can find the *value ranges* of the integer types for C compiler in the header file `limits.h`, which defines macros such as `INT_MIN`, `INT_MAX`, `UINT_MAX` and so on

```c
int main() {
	printf(" char %d %d %d\n", sizeof(char), CHAR_MIN, CHAR_MAX );
	printf(" int %d %d %d\n", sizeof(int), INT_MIN, INT_MAX );
	return 0;
}
```