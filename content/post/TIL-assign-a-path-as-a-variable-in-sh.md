---
title: "TIL Assign a Path as a Variable in Sh"
date: 2020-08-25T18:09:06+09:00
hidden: false
draft: true
tags: [Shell, Shell Script]
keywords: [Coding]
description: ""
slug: ""
---

I got a number of errors during scripting a shell lines.

right form is below.
```
blogpth=~/coding/hugo-blog
pstpth=~/coding/hugo-blog/content/posts/
```

the right side from `=`, must be not covered with `""` or `''`.

