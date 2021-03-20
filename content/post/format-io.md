---
title: "Format IO"
date: 2020-10-08T17:06:43+09:00
hidden: false
draft: true
tags: [Minimum Width, Precision, Printf, Scanf, float, decimal, integer]
keywords: [Format I/O, C Language, TIL]
description: ""
slug: ""
---

# Format I/O ( input / output )
in C langauge, conversion type is sensetive.

`%m.pX` is the form in print-in and out.

## Minimum width

`m` means the 'Minimum width'. ***Minimum width defines about how much the value will charge some spaces in output.***

Left justification, Right justification we can specify with `m`.

`-m` does left justification as it adds spaces *behind*.
`+m` does right justification as it adds spaces .
eg.

        %-6d : N.....
        %6d : .....N

## Precision

`p` means the zero amounts specifier. It means 'Precision'. 'Accuratly, how many do you want appear its accuracy?'.

When we want to add a specific amount of zero, `p` is the determinator.

eg.

        %.4d : Express an integer in 4 digits.
        %.3f : Express the decimal digits maximum 3.


`X` means the type of conversion. `%f %e %g` can be used to `float` data types.

        %f : fixed float.
        %e : Exponential float.
        %g : Globally expressing float. Very long and very small numbers spontaneously expressible.


## with Scanf 

1. when we want to scanf only 1 digit, the code is below.

        ```
        scanf("%1d", &i);
        scanf("%.1d", &i);  /* Wrong */

        ```



