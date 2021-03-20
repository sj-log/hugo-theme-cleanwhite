---
title: "Shell C Tricky Point"
date: 2020-10-10T10:38:24+09:00
hidden: false
draft: true
tags: [TIL, Clarify, C language, Equality, operator, Shell]
keywords: [Tricky part, C language, Shell script]
description: ""
slug: ""
---

C has the equality return values.
When we compare 2 values whether they are same or different,
the boolean values returned by 0, 1.

1 means the values are each other equal Which mean, 'same'.
0 means the values are different, not same.
So, 0 can be interpreted as True in equality, 1 can be false in meaning.

But this fact seems tricky when we use Shell script as well.
Shell has an exit code when they execute the script at the end of processing.
When the processing successfully done, then 0 return.

How to make sure of that tricky point?
In equality, 0 means, there is nothing in common, 0 amounts. Hence it can be recognized 'false'(ahha!). In opposite, if there is a common feature or equality existed, that means 1, yes, there is something common aspect existed in between two objects.

In shell script, we can put in this way similarly.
If Shell script does work well, it means there is no error, even 1, so it returns 0, as there is Zero problem(no problem). so the meaning of 0 indicates 'it executes without any problem'. and oppositely, 1 can means there is an error to need to check up.

Existing or not do make the difference in between C language's equality result and shell script exit code.
