This is all about how to see the assembler complied result with C langauge.

## Learned from 'rush' in 42

well, Mr. `doby` taught us in our first rush project. 
Yes we can learn something from the collectors during rush evaluation.

Rush means the evaluation activity in 42ecole system.
Every weekend, participants(pisciners) should have to join and to access 1 group project with randomly chosen 2 people.

## How to check complier result.

`gcc -S filename.c`. then we can see the assembler's result how the C program complied.
The test through assembler showen definite way how to ++i and i++ are differently procceeded.

Both `++` does firstly complied earlier than `i`.


<img width="2133" alt="스크린샷 2020-10-21 오전 9 53 27" src="httpimages.githubusercontent.com/35059428/96659974-5a350600-1383-11eb-933e-ad9cbf905ee7.png">

## figure out two differents.

`gcc -S filename1.c filename2.c`

we can check those 2 files result which is passed by assembler processing.

`diff filename1 filename2 > filename.diff`

then we can check those differences in two files.

## [EAX in assembler langauge?](https://www.cs.virginia.edu/~evans/cs216/guides/x86.html)

```
Arithmetic and Logic Instructions

add — Integer Addition
The add instruction adds together its two operands, storing the result in its first operand. Note, whereas both operands may be registers, at most one operand may be a memory location.

Syntax
add <reg>,<reg>
add <reg>,<mem>
add <mem>,<reg>
add <reg>,<con>
add <mem>,<con>

Examples
add eax, 10 — EAX ← EAX + 10
add BYTE PTR [var], 10 — add 10 to the single byte stored at memory address var
```


## conclusion

++, increments operator does firstly proceeded by assembler. 
we can check it from `gcc -S` commands in obvious result. `addl $1, %[eax](https://www.cs.virginia.edu/~evans/cs216/guides/x86.html)` firstly came out from the list.
