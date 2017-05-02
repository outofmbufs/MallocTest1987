# MallocTest1987
30 year old code, from FF#066 Amiga, presented for amusement.

File mtest.c is the unadulterated malloc test program as published in 1987.

On my mac the original file will generate a bazillion warnings about incorrect library function declarations and similar such problems, and one fatal error because there is an int function that does not return a value. It should have been declared void -- and the reason it most likely wasn't is that this is how we did that back then in the time before "void" existed as a type on many compilers.

So I made a two line change to declare "add_to_events()" as a void function, and now the program compiles and runs (at least on my mac). The source with the change is contained in the mtest2017.c file.

I am under no illusions that this program is good, easily understood, or even useful. I will note that it helped me find a bug in a malloc/free implementation on some platform in 1987. The only reason I know that is because I said so in a net.sources posting back in 1987:

```
Article 574 of net.sources:
Path: mcdsun!noao!hao!nbires!seismo!husc6!necntc!encore!vaxine!nw
From: nw@vaxine.UUCP (Neil Webber)
Newsgroups: net.sources
Subject: malloc/free test program
Message-ID: <417@vaxine.UUCP>
Date: 16 Feb 87 20:49:49 GMT
Organization: Automatix, Inc., Billerica, MA
Lines: 460

A while back I asked the net if anyone had a malloc/free test program that
would allocate and free randomly sized pieces of memory with random lifetimes
(and fill them with patterns that would be checked for corruption).  I got
a number of useful suggestions (best one: use the "diff" program as a
malloc test ... it's brutal).  Eventually, I wound up writing my own
test program, which actually helped me find a bug.

On the assumption that it might be useful to someone else, here it is.
Please note:

       - No documentation (read the code to find out what it does).
       - Could be extended in zillions of ways to make it more useful.
       - No makefile, just compile "cc mtest.c"


```

Oh we could write a whole essay on the history elements contained in a posting like that. Starting with: Bang path email addresses!

Anyhow - To compile this program just do:
```
cc mtest2017.c
```

This works on my mac. Your mileage may vary, and you may wish to make additional modifications to squelch the rest of the warnings.

The most interesting thing about this is the notion that something written in a programming language 30 years ago can still be compiled, and run!
