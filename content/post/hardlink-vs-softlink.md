---
title: "Hardlink vs Softlink"
date: 2020-10-13T18:23:38+09:00
hidden: false
draft: true
tags: [TIL, coding]
keywords: [hardlink, softlink, file, shell]
description: ""
slug: ""
---

So, Those are creatable as 'shortcut'.
They look like that manage files easily.

## Hardlink
- Hardlink is possible to modify the original by editing hardlinked file.

- because an Original file and hardlinked file point to same memory.
- **hence when we modify a hardlinked file, the original file change as same file!**

- We can use as as to have a sharing seeds folder for torrent, you can put a file's hardlinks into that sharing folder until you want to share. When you feel it's enough to share, you can just 'disconnect those seeds' by deleting the original files contained folder.

- but, hardlink cannot cross another volumes.

## Softlink
- Softlink seems a shortcut indicates the original file.
- However, as a shortcut file It doesn't work when remove the original file.
- It does show up the mark `--->` when we print a containing directory with `ls -l`.


