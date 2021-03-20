---
title: "Caution : Scanf"
date: 2020-10-08T13:36:31+09:00
hidden: false
draft: true
tags: [Scanf, C langauge, TIL]
keywords: [TIL]
description: ""
slug: ""
---

Scanf seems unrecommendable in C language.
because of a few reasons.

1. More than 1 line of buffer, It crashes. So can be replaced by `fget`.
2. In arithmetic overflow happens, no way to securely protect it.

## Features

1. Reading user input until a white space.
2. When a buffer meets a white space, recognition will be terminated.
3. A white space means below (Space, Tab, Newline, etc) 

    [isspace()](https://www.man7.org/linux/man-pages/man3/scanf.3.html)
              checks for white-space characters.  In the "C" and "POSIX"
              locales, these are: space, form-feed ('\f'), newline ('\n'),
              carriage return ('\r'), horizontal tab ('\t'), and vertical
              tab ('\v').

## Cautions

1. check near `printf()` functions has `\n` at the end, before `scanf()`.

`\n` before scanf ***can be recognized as `a white space` at the first of scanf's argument.*** So It would risk its malfunctioning(stopped).

```
printf("%d, %d \n", &i, *j); /* WRONG */
scanf("%d ,%d")
```

2. the arguments have to be address types with `&`.

```
scanf("%d", &variable);
```
