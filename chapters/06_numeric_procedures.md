Numeric Procedures
==================

This chapter will gives more examples on numeric procedures.


Arithmetic Procedures
---------------------

The addition and subtraction has been introduced in the previous chapter.
For doing multiplication and division, we use the "*" and "/" because 
there are no such symbols looks like the symbol that represents the 
meaning of multiplication and division in mathematics.

```
(* 2 3) ; 6
(. 12 4) ; 3
```

We all know that the number 0 could not been used as a divisor, once you
try to do the following thing:

```
(/ 4 0) ; Oops! Divided by zero!
```

the program will stopped from execution and 
an runtime error is going to be raised, 
the content of the error is "division by zero". 

You probably will try if the procedures applies on "float-point numbers", of course:
```
(* 1.2 2.0) ; 2.4
(/ 15.0 3.0) ; 5.0
```


Type Promotion
--------------

Does float-point numbers operate with integer numbers? The answer is yes:
```
(* 1.2 2) ; 2.4
(/ 15.0 3) ; 5.0
```

A float-point number multiply by an integer number evaluates to a float-point number
because the float-point numbers could also represent some integers, roughly speaking,
the float-point numbers has the ability of integer numbers. This automatic conversion
happens as above is called "type promotion"

The result of division 15.0 by 3 evaluates to "5.0" instead of an integer "5", this is 
because of there is no such an "inverse operation" for type promotion that will automatically
executed.


There are some divisions work for only integers, called integer division:
```
(quotient 9 4) ; 2
(remainder 9 4) ; 1
(modulo 9 4) ; 1
```


Rational Numbers
----------------

Rational numbers are supported by Scheme:
While dividing applies on integers and could not evaluates to an integer,
instead of returning an approximative integer which is supported by most
machine directly, the value returned is a rational numbers
```
(/ 4 12) ; 1/3
```


Exactness
---------

In the example above, we already know it returns the value 1/3 exactly
represents the meaning of the result of `(/ 4 12)`, but the 
rational number type is not directly provided by CPU hardware in most
machines. Those CPU normally use float-point number like 
`0.33333333333...`
to represent this value. But no matter how accurate the number is, it can't
"precisely" represents as `1/3`. So we normally say values like
`0.33333333333...` are "inexact", but those values in rational number 
types (or integer numbers types etc.) like `1/3` or `123` are "exact".

Conversion from exact numbers to inexact numbers are usually easy:
```
(exact->inexact (/ 4 12)) ; 0.3333333333333333
```

But the inverse process isn't that much easy:
```
(inexact->exact (exact->inexact (/ 4 12))) ; 6004799503160661/18014398509481984
```

Because the conversion from exact to inexact loses some information of
the original value and the lossing is irreversable.

