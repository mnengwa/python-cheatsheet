# INTEGERS, FLOATING-POINT & COMPLEX NUMBERS

#### Python has 3 built-in numeric data types

> **_Integer_** - (from the Latin integer meaning **"whole"**) is a number that can be written without a fractional component (decimals or fractions).

> **_Floating point number_** - is a number that has decimal places in a computing system. e.g **1.2**, **3.5**, **1.0**, **3.141592653589793238462643**

> **_Complex number_** - is a value used to represent imaginary numbers [Wikipedia](https://www.wikiwand.com/en/Complex_number), [Numberphile II](https://www.youtube.com/watch?v=-IJuqR6nz_Q&ab_channel=Numberphile2), [Veritasium](https://www.youtube.com/watch?v=cUzklzVXJwo&ab_channel=Veritasium)

### + Addition

```python
# 2 plus 3
print(f'2 + 3 = {2+3}')
```

### - Subtraction

```python
# 7 minus 5
print(f'7 - 5 = {7-5}')

# 11 minus 13
print(f'11 - 13 = {11-13}')
```

### x Multiplication

```python
# 1 times 5
print(f'1 * 5 = {1*5}')

# 2 times 4
print(f'2 * 4 = {2*4}')
```

### &#247; Division & Interger division

```python
# 2 divide by 5
print(f'2 / 5 = {2/5}')

# 2 divide by 5 interger
print(f'2 / 5 = {2//5}')
```

### % Modulo (remider of division)

```python
# 9 module 7
print(f'9 / 7 = {9/7}')
```

### x <sup>y</sup> Exponents (raise a number to a power) - i.e multiply x by itself y times

```python
# 3 power 2
print(f'3 ** 2 = {3**2}')

# 4 power 2
print(f'4 ** 2 = {pow(4,2)}')
```

### Rounding up numbers

```python
# round up 2.56 to the nearest whole number
print(f'round(2.56) = {round(2.56)}')

# round up 2.5 to the nearest 2 decimal place
print(f'round(2.56) = {round(2.56)}')
```

### Get the absolute number

```python
# ignore the negative sign
print(f'abs(-1.4) = {abs(-1.4)}')

# ignore the positive sign
print(f'abs(1.4) = {abs(1.4)}')
```

### Complex numbers

To create complex numbers, you simply write the real part, then a plus sign, then the imaginary part with the letter j at the end

```python
print(f' 1 + 2j = {1 + 2j}')
```
