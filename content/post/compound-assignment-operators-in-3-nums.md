---
title: "Compound Assignment Operators in 3 Nums"
date: 2020-10-09T15:40:32+09:00
hidden: false
draft: false
tags: [C language, TIL]
keywords: [C language, tips, operating]
description: ""
slug: ""
---

`i += j += k;`

This assignment seems tricky.
but Knking's book say, there is a tip.

`i += (j += k);`

so, `j+=k` becomes (j=j+k), hence operated first.
at here, K never has any operating without only its initialization.
if `k = 3;` k becomes just 3.

j becomes j+3.

and,

`i = i+ (j+3).`

That's it!





