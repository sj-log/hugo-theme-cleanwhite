---
title: "C-language-character-in-Write()"
date: 2020-08-31T20:21:50+09:00
hidden: false
draft: true
tags: [Char, Integer, write(), ASCII]
keywords: [C language]
description: ""
slug: ""
---


C language has proceeded differently with Char and Integer in `write()`.


`Write()` is a kind of low level function.
So, we should have to define how many letters would show up by 3rd arguments bytes numbers.

ASCII code would be printed in 1 byte.

So, `write(1, &c, 1);` does work without any error message.

However, when we write a character which is non ASCII char, must have 2 bytes at least.


## Start from 47 in increment loop.

C language compiles a character as Decimal numbers as ASCII code.
[ASCII codes has decimal system of it.](https://www.google.com/search?q=ascii+table&newwindow=1&safe=strict&sxsrf=ALeKk03MLOE22WLVyhlvFHbe1qJF03QT4w:1603075918626&tbm=isch&source=iu&ictx=1&fir=Gcjw1cCFnJ60BM%252CW0bMX2lmb8aQuM%252C%252Fm%252F0hb8&vet=1&usg=AI4_-kRROeZUVbgv2d9EBV0zqwth94gq6g&sa=X&ved=2ahUKEwi6urWV07_sAhWTc3AKHR-NAKwQ_B16BAgqEAM#imgrc=5T2rVZ00Y2uxNM)

`0 ~ 9` does match with ASCII nums 48 ~ 57.
So, when we want to iterate an integer number in increment scale  or to loop from 0 number, the first variable should be 47.

```
int i;
while(++i<57){ some function() }
```
would make it work.

