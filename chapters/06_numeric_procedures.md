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
an runtime error is going to be rised, 
the content of the error is "division by zero". 

You probably will try if the procedures applys on "float-point numbers", of course:
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
the float-point numbers has the abbility of integer numbers. This automatic convertion
happens as above is called "type promotion"

The result of division 15.0 by 3 evaluates to "5.0" instead of an integer "5", this is 
because of there is no such an "inverse operation" for type promotuon that will automatically
executed.


There are some divisions work for only integers, called integer division:
```
(quotient 9 4) ; 2
(remainder 9 4) ; 1
(modulo 9 4) ; 1
```


Rational Numbers
----------------


Convertion Between Types
------------------------


