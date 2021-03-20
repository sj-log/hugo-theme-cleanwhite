---
title: "Regex in Find"
date: 2020-10-13T08:58:33+09:00
hidden: false
draft: true
tags: [TIL, coding]
keywords: [regex, find, piscine, 42seoul]
description: ""
slug: ""
---

The regex expressions are tricky for me.
Well, a some part of the reason difficulty on the regex is because of my lack of comprehension on English words.

1. meaning of 'Preceding'.
I couldn't understand 'preceding' means correctly.
but, as * means check specific names which have any preceding charactor more than 0 or more occurences.


2. \ for meta regex

had to find a file which starts with `#`. but `#` is a special charactor has many other functions in cmd.
but when we use \#, we can use the `#` as a charactor, not as a functional charactor. yes we can ignore it.

[this website](https://docs.trendmicro.com/all/smb/wfbs-a/v7.0/en-us/wfbs-a_7.0_olh/WFBS/Managing_the_Messaging_Security_Agent/About_Regular_Expressions.htm) is neat and clear about that functions.

