# Data Types
Data values in Python are known as **objects**; each object has a type.

* 
    ```
    type(obj)       
    ```
    accepts any object and returns the **type object** that is the type of obj.

*
    ``` 
    isinstance(obj, type)
    ```
## Numbers

#### integers
```
1, 23, 3493         # Decimal integer literals
0b010101, 0b110010          # Binary integer literals
0o1, 0o27, 0o6645           # Octal integer literals
0x1, 0x17, 0xDA5            # Hexadecimal integer literals
```

#### floating-point 
```
0., 0.0, .0, 1., 1.0, 1e0, 1.e0, 1.0e0 # Floating-point literals
```
#### complex numbers 
* A complex number is made up of two floating-point values, one each for the real and imaginary parts. 
* You can access the parts of a complex object z as read-only attributes **z.real** and **z.imag**.
```
0j, 0.j, 0.0j, .0j, 1j, 1.j, 1.0j, 1e0j, 1.e0j, 1.0e0j
```

#### underscores in numeric literals
to improve readability:
```
>>> 100_000.000_0001, 0x_FF_FF, 0o7_777, 0b_1010_1010
    (100000.0000001, 65535, 4095, 170)
```

## Sequences
an ordered **container** of items, **indexed** by integers

#### build-in sequence types
* strings (bytes or Unicode) 
* tuples
* lists

#### iterables
* All sequences are iterable
* All sequences are ***bounded**

#### strings
* **immutable**
* Unicode strings: text-based information
* byte objects: store and represent arbitrary sequences of binary bytes

* single quote and double quote are identical except that while using double quote there's no need to escape a single quote from within:
    ```
    "I've found that Python is cooooool"
    ```
* continuation: 
    ```
    'A not very long string \
    that spans two lines' # comment not allowed on previous line
    ```
* newline:
    ```
    'A not very long string\n\
    that prints on two lines' # comment not allowed on previous line
    ```
* triple-quoted strings:
    line breaks in the literal remain as newline characters in the resulting string object.
    ```
    the_text = """\
    First line
    Second line
    """ # like 'First line\nSecond line\n' but more readable
    ```
    The only character that cannot be part of a triple-quoted string is an unescaped backslash, 

* **raw string**: a variant of a string literal. 
    * The syntax is the same as for quoted or triple-quoted string literals, except that an r or R immediately precedes the leading quote. 
    * In raw strings, escape sequences are literally copied into the string, including backslashes and newline characters.

#### Tuples
* **immutable**
* **ordered**
* **heterogeneous** items. Can contain mutable items (e.g. lists), but best not to.
* **pair**: a tuple of two items

* constructor:
    1. 
        ```
        (100, 200, 300)         # Tuple with three items
        (3.14,)                 # Tuple with 1 item needs trailing comma
        ()                      # Empty tuple (parentheses NOT optional)
        ```
    1. built in function tuple().
        * When x is iterable, tuple(x) returns a tuple whose items are the same as those in x.
        ```
        tuple('wow')            # equivalent to ('w', 'o', 'w')
        tuple()                 # returns an empty tuple ()
        ```

#### Lists
* **mutable**

