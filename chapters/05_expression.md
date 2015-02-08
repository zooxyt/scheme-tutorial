Expression
==========


S-Expression
------------

Of course evaluates some basic types and get those basic types return
is useless, for doing more things in Scheme, we need to write more complex
programs. The body of a program is called source code which means it is
the source where the final `program` that machine understand comes from.
  
Contrast to the so-called rich text which contains formats, the most
classic source code of Scheme programs contains only plain text as the 
examples given in the previous chapters. In the perspective of `Syntax` 
we say the source code are basically consists of `s-expression` which
is short for "Symbolic Expression".

An s-expression has two derived forms:
- Atom
- Pair 

Atoms is kind of somehow inseparable thing in syntax, such 
as the values of the basic types. Pairs are different, they consist of
two parts, the "car" part and the "cdr" part and denotes 
as `(<car> . <cdr>)`, the "car" and "cdr" parts themselves are 
s-expressions.

The benefit of this form is that you can construct more complex forms of
data structures base on it. For example, to represent a list, we use the 
following form:
```
(a . (b . (c . NIL)))
```
The `NIL` here represents an "empty list".

For convenient, the expression above could be written as below as well:
```
(a b c)
```

Using in Lisp
-------------

We already know how a little about how to represent data with s-expressions.
And to represent programs is possible.

For expression, we want to represent the meaning of 
"the result of adding 1 to 2", in mathematics we write `1 + 2` which we
already adopt to. This form in mathematics is called "infix notation"
which means the operation we want to perform on the numbers is written in
the middle of the numbers.

In Lisp (also in Scheme) we use a different order to represent the same
meaning which is named "prefix notation". In prefix notation, we write
the operator `+` in the front of the expression instead of writing in the
middle with a pair of parenthesis around:
```
(+ 1 2) ; 3
```

The `;` in the code means the text starts from ";" to the end of the line
are "comments". Comments doens't do anything to your program, you just write
anything you want in the comments to make you code easy to understand by 
people.

This looks a bit weird for people who never used Lisp before, but sometimes
we benefit from writing in prefix notation. For example, we want to
represent the some from 1 to 5, in classic infix notation which has been
widely used in mathematics, we write `1 + 2 + 3 + 4 + 5`. Looks pretty
normal. But in prefix notation, we just need to write `(+ 1 2 3 4 5)`.

For people who has experience of other "classic programming languages", the
one thing should be noticed is that the `+` here is NOT an "operator", it
is more like a "function".

The difference between the "+" function in Scheme and the `+` in mathematics
is that the "+" function accepts arbitrary number of "arguments" instead of
two. The following expressions are legal in Scheme:
```
(+)        ; 0
(+ 1)      ; 1
(+ 1 2)    ; 3
(+ 1 2 3)  ; 6
```

The "+" function has an initial zero value for represent the sum of 
all arguments. if no available argument, it evaluates to 0. 

Let's take a look at another procedure "-". "-" function accepts at least one
argument which means the following code:
```
(-)
```
is illegal.

While applying on only one number, it evaluates to the negative number of the
original number:
```
(- 123) ; -123
```

while applying on more than one numbers, it set the first number as the 
"initial value" of the while process, and subtracts the initial value by the 
remained numbers one by one.
```
(- 10 1 2 3) ; 4
```

