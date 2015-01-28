Basic Data Types
================

Every data has a type, the type of a data indicates the abilities 
of the data and has its own way been used. For example, the expression
we typed in the previous chapter itself is a value of a data in type `string` which means a string of some characters. 
A string which has none character is also OK, and 
will be written as `""`.

There are many other types besides `string`, this
chapter is only going to talk about some basic types, because
Scheme contains too many and advanced data types is not needed currently.
Let's take a look at some examples of other types.


Integers
--------

Integers here are integers in mathematics, 
the following numbers are legal integers in Scheme:
```
123
0
-123
```

The most significant difference between Scheme and 
some other programming languages designed in early age 
is that Scheme supports big integers, the following number is an example:
```
93326215443944152681699238856266700490715968264381621468592963895217599993229915608941463976156518286253697920827223758251185210916864000000000000000000000000
```

The number above is the exact value of `100!`, and 
the only limit of the size of number is 
probably the memory of your computer.


Float-Point Numbers
-------------------

It could be a bit unfamiliar for beginners to the concept of 
float-point number. 
Float-point numbers are look like decimal numbers in mathematics but not entirely.  
We all know decimals that look like:
```
0.1
-0.123
```

In mathematics, it is able to represent a decimal number with has many
digits after the decimal point such as `0.12345678901234567890`
due to the limit of hardware. The problem doesn't only occurred on a decimal with high precision, for example, the result of sum of two decimals `0.1` and `0.2` is `0.30000000000000004` this is because the computer represents the numbers in binary format in the machine level, and there isn't a number `0.3`.

For people who needs to know how machines work with float-point numbers, check the 
[IEEE-754](http://en.wikipedia.org/wiki/IEEE_floating_point) standard.


