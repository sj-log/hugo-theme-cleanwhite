---
title: "Short circuit in Logical Expression"
date: 2020-10-10T14:38:17+09:00
hidden: false
draft: true
tags: [TIL, Short-circuit evaluation, side effect, right operand, C langauge]
keywords: [C language]
description: ""
slug: ""
---


in C language,

`a > b && c < d`

`c < d`(Left operand) ***part will not work*** if `a > b`(right operand) goes false.

(but I wonder why they made that side effect.
Is that for decreasing unnecessary compiler interaction?)

## p.s

I thought this side effect a simple thing, but it wasn't but generally awared in C language users.

It's been called also 'Short Circuit Evaluation'.

## Relevant quiz.

```
i=1; j=1; k=1;
printf("%d ", ++i || ++j && ++k);
printf("%d %d %d", i, j, k);
```
The result becomes, 2 1 1.
So I wondered why?
Most of stackoverflow answered Short circuit and precedences with each operators.

By the operation precedences, the code executed in below.
1. ++
2. || 
and so on.

### Explanation
but I couldn't understand why || firstly executed when || couldn't operate first than && even though [the && has higher precedence.](https://en.cppreference.com/w/c/language/operator_precedence)
because, && and || has left-to-right association, but we can see the reason when we do more zoom in.
++i firstly occured, so +2 is built.
then nextly compiler touches the ||. then by the Short-circuit evaluation, compiler does recognize just it doesn't need to check the second operands.(Short circuit evaluation)
Because in ||(or) operation, when an arguments go 'True', then the entire result automatically 'True' without checking further proceeding.
Yes, so just ++i does math, and touch ||, then just goes next line with skipping the second arguments which made us confusing.


## Why does Short Circuit Evaluation existed?

Referred [here.](
https://en.wikipedia.org/wiki/Short-circuit_evaluation#Common_use)
To prevent an error or a problematic execution, It does hang a logical operator in between two arguments.

