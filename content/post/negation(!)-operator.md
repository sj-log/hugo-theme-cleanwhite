---
title: "Negation(!) Operator"
date: 2020-10-10T12:39:56+09:00
hidden: false
draft: true
tags: [logical operator, C language]
keywords: [Logical operator, C language, TIL]
description: ""
slug: ""
---

So I wondered why 

```
i=10;
printf("%d", !i==0);
```
above logic returns 1?

1 means true.
so, the above result means, !i==0 is true.
then, why !i does return false value?
because i is already true?

i is non zero number which is 10.
[and non zero numbers are treated as 'true'.](https://www.cs.uic.edu/~jbell/CourseNotes/C_Programming/Decisions.html)

        Yes, Non zero numbers when it met !(negation operator), 
        it return `false`, because non zero numbers treat as `true`.


