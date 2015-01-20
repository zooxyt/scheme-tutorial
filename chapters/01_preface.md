Preface
=======

One of the greatest innovations in the past century is computer, it 
was original designed for science computing and used for rare people
in research facilities from the beginning, but now spreads into every
corner in our daily life. Even people with little experience with 
computers know click some buttons and install the applications they want
to solve the problem in real world or to do some entertainment.

I was heavily afraid of touching such machines when I was in early age
cause computers are pretty expensive and I'm afraid of if broke it down.
But one day, I became deeply into it, the turning point was programming.

Programming makes people freely control the machine and schedule things 
for it to make it solving problems automatically, just 
like placing dominoes in appropriate positions and push the first
one to see the how dominoes falling down one by one automatically. 
To release the power of computer and to command it working in the willing
of people, programming is essential. 

The tutorial is about programming for absolute beginners, with
a programming language named "Scheme".


Specification
-------------

The latest fully (at the time of this tutorial been written) 
published specification of Scheme Programming Language could be 
R6RS, which is short for 
**The Revised<sup>6</sup> Report on the Algorithmic Langauge**
and could be viewed at: 
http://www.r6rs.org/ 

The specification contains 4 parts including Libraries and so on, 
makes Scheme bias the original simple design, 
so the tutorial covers a previous version, 
R5RS and could be downloaded at:
http://www.schemers.org/Documents/Standards/R5RS/

The document is pretty short, only contains 50 pages 
(as a specification of a programming language
 compares to other programming languages 
 such as C++ which contains more than 1000 pages).


Lisp?
-----

You may already know a bit Scheme before or just have read the 
specification mentioned above, and seen tons of parenthesis which
is probably the most famous characteristic of a series of programming 
languages with name of `Lisp`, (Lisp has also been called `Lost In Stupid Parentheses`).

The original design of the language was not looks like the modern looking,
just been `stopped` at the step like this by accident, but
lack of a complete parser which widely exists 
in many other high-level languages isn't that bad 
because the parentheses style of language 
not only makes the code of program looks consists and clean 
but also enables programmers easy to do conversion between code and data
and have much more freedom to do things looks difficult in normal 
programming languages.
Some people says, the grammar of lisp can be written in only one line:
```
'(' list ')'
```


Dialects
--------

Because of the fact that Lisp only started the style of list with 
parentheses brace around, many people and organizations try to define
what kind of syntax looks like, how many data types have, or how does
the program runs and they create their own copy of Lisp that doesn't 
completely like the original Lisp, these derived version of Lisp also
derives new versions of Lisp, so we call these derived versions of Lisp
`dialects`. Scheme is one of these dialects of Lisp.


Benefits
--------

Learning a new thing takes time, "why do I have to spend my time on
learning a new programming language instead of playing games or
drinking some beer with friends?" Or say, "What do I get from learning
this" may be a frequency asked question.

I personally think we don't have to get something from the progress of
learning, learning itself is interesting, but some reasons can be told
to motivate you.

Different person gets different things, it might be impossible to tell
what you will get explicitly.

For a newbie who begins his trip to the world of programming, Scheme is 
a good start point, it contains less details that requires to know the
computer architectures that have to be deal with in some low-level 
programming language and let coders focus on solving the real world 
problems, and feeling the fun of coding.

For an experienced programmer who has never use Lisp-like things, 
Scheme will provides new thinking ways that inspire better code. 
As a rather simple programming language, it could also be used as a script
languages that extends the function dynamically 
(Like JavaScript in Web browsers).

For a programming language fun and geek, Scheme provides a cool playground
for testing new features without wasting abundant time on writing a 
parser.


How To Read The Tutorial
------------------------

The best way to learn a programming language is to use it. 
Put your hands on the keyboard and type the code with fingers, do not
copy and paste. Run the code, debug it step by step and think about
how it works.

