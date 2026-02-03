# Floating Point

C also include special numeric types that can represent non-integers with a decimal point in any position.  The floating-point types are used to represent real numbers with decimal points. 

> *They are essential for scientific calculations, graphics and any requiring fractional precisio*n
> 

The standard *floating-point types* for calculations with real numbers are like this:

| Type | Size (Bytes) | Range | Precision (Digital Digits) | Format Specifiers |
| --- | --- | --- | --- | --- |
| `float` | 4 | ±1.2e-38 to ±3.4e+38 | ~6-7 | `%f` (printf/scanf) |
| `double` | 8 | ±2.3e-308 to ±1.7e+308 | ~15-16 | `%lf` (scanf), `%f` (printf) |
| `long double`  | 10+ | ±3.4e-4932 to ±1.1e+4932 | ~18-19 | `%Lf` |

The header file `float.h` defines macros that allow to use these values and other details about representation of real numbers in programs. The macros `FTL_MIN` , `FTL_MAX` and `FTL_DIG` indicate the value range and the precision of the float type

### Precision

A `floating-point` value can be stored only with a limited precision, which is determined by the binary format used to represent it an the amount of memory used to store it.

The precision is expressed as a number of significant digits, so that its conversion back into a six-digit decimal number and trailing zeros are not counted in the six digits.

The position of the decimal point does not matter,  leading and trailing zeros are not counted in the six digits

> The numbers `123,456.000` and `0.0012345`  can **both** be stored in a type with six-digits precision
> 

## Arithmetic operations

In C when we use floating-points numbers are performed internally with double or greater precision

```c
float height = 1.2345, width = 2.3456;                   #Float variables ahve single precision
double area = height * width;                  #The actual calculation is performed with double precision

```

---

## Floats

The header file `float.h`  defines macros that allow you to use these values and other details about the binary representation of real numbers in the program. The macros `FTL_MIN` , `FTL_MAX` and `FTL_DIG` indicate the value range and the precision of the float type

![Screenshot From 2025-09-03 04-12-05.png](Floating%20Point/Screenshot_From_2025-09-03_04-12-05.png)