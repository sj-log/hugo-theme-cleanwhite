---
title: "Increment Operation & Printf"
date: 2020-10-09T16:22:53+09:00
hidden: false
draft: true
tags: [Increment, operation, C language]
keywords: [C language, format io, printf, TIL]
description: ""
slug: ""
---

yes, the interesting fact here, 
even though printf is just a format output function, the **++ in that argument just change the variable's data permanently.**

## Increasing its value even in Printf()
`i++`, in `printf()`.
They modify it's operand even though it was just a function call of 'printing.'

```
i=1;
printf("%d", i++);
printf("%d",i);
```

`i` will print, 1 in top printf, but will print at second printf.

## increasing its value even in another operating.

even though the `++i` just happened in middle of program, not seperately, but it permanently modify the variable's value.
```
i=5;
j= ++i * 3 -2;
printf("%d %d", i, j); ---- i = 6
```

## Conclusion.

No matter where the increaments or decreament operators, they modify the variable's number value.

