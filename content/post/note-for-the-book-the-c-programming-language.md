---
title: "Note for the Book the C Programming Language"
date: 2020-08-26T08:14:02+09:00
hidden: false
draft: true
tags: [TIL, C language, Book, Review]
keywords: [Coding]
description: ""
slug: ""
---

## Notes

- C langauge is the Unix operating system's original language.
- ANSI Standard?
- `pointer` is the ***central*** to C programming.
- **Implementers? Programmers?** What are those differences in between?
- C wears well as one's experience with it grows.
- C is a general-purpose programming language with features economy of expression, modern flow control and data structures and a rich set of operators.
- C langauge's absence of restrictions and it's generality make it more convenient and effective for many tasks than supposedly more powerful languages.
- A funcion contains `statements` that specify the computing operations to be done and variables store values used during the computation.

- first line of the program such as `#include <stdio.h>` tells **the compiler** to include information about the __standard input/output library.__

### `Main()`

- `main()` function is special. Your program begins executing at the beginning of main. **This means that every program must have a main somewhere.**
- `main()` will usually call other functions to help perform its job, some that you wrote, and others from libraries that are provided for you.
- `main()` expects no arguemnts which is indicated by the empty list of args.



- braces mean `{}`. It shows `statements` of that function.
- "Hello world" is a ***character string or String constant***. (What is the meaning of the Constant?)
- all ***Variables*** must be declared before they are used, usually at the beginning of the function before any executable statements.

## Pointer

- ***a pointer is a variable that holds the address of a variable.***
- Pointer will be uninitialized until assign an address of a variable to a pointer.
- When a pointer variable holds the  address of another variable, it ***essentially points to that variable.***

- Pointer points to the ***start*** address from the charged memory. This is why a pointer variable has to have 'type(integer, double, character, etc)'. Int type does charge 4 bytes in memory, then computer can figure out the variable how much it charges with the memory end point.
- Pointer leads to more compact and efficient code than can be optained in other ways.
- Pointers and arrays are closely related.
- `void`? completely empty.
- what is `void pointer?` ***has no associated data type with it. It can hold a blank data.***

- so It seems like, the pointer can make a call of a specific data without generating another variable. Then, Memory will save its storage. In the opposite case, normally, to call a same value but different variable can waste by its duplication.

### Pointer with Memory.

- Pointers only way to get to heap memory.

### * dereferencing 
- defines a pointer. e.g. `int *pA;`
- 'dereferencing' : To follow the pointer.
- `*` is for declaration a pointer value.
- `*` exists only to tell C that the variable is a pointer.
- e.g `int *ip;`, `double *dp;`, `char *cp`;
- They will point to the data that their data-type is matching, and address value initialized.
- So, thus the mandatory is the matching with address value by `&variable` e.g `p=&a;`.
- `Pointer variable` has an address as it is a variable itself. However, until it's combined with another `&` variable, It doesn't have the address itself yet.(?)

### &
- produce an address to a pointer.
- `&` initializes the pointer variable which is delcared by `*`. e.g `p=&a;`. It's linking a pointer with 3rd variable's address. It makes a pointer points 3rd variable's address. so `p` can call the `a`'s data value. e.g `printf("%d \n", p);`
- `&` makes to a pointer points to a 3rd variable's address. e.g `p= &a;` which means, variable P has the address of `a`. so thus, p has the value(data) of `a` checks the address.

### Calling a data with Pointer

- can call a variable value by calling the variable's name, and dereferencing the pointer.

`printf("%d \n", *p);`

### Const

- Constant : Never changing variable
- can be a good compound with pointer. How?


### Array with Pointer

- an array is a special kind of pointer. how?
- pointer notation to get array values, array notation to get to pointed-at values.
- Array names are known an **pointer constants.**
- 
