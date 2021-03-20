---
title: "Ssh Add Issue for Git Push"
date: 2020-08-08T09:23:12+08:00
hidden: false
draft: false
tags: [git, vim-fugitive, ssh]
keywords: [Coding]
description: ""
slug: ""
---

Struggled with pushing Vim-fugitive.
The main issue was happening whenever I tried to `push` on Vim-fugitive.

## Problem

1. load Username failed
```
fatal: could not read Username for 'https://github.com': No such device or address
```

2. ssh-askpass error
```
ssh_askpass: exec(/usr/bin/ssh-askpass): No such file or directory debian
```
## Cause

The message meant that I wasn't verified with my own SSH.

## Solution

1. had to install `ssh-add`, through `sudo apt-get install ssh-add`.
2. firstly made sure whether do I have the keygen existed by `ls -al ~/.ssh`.
3. found there was no lists shown up.
[ then execute to generate a new ssh key through `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
5. enter enter...
6. check again with proc number 2.
7. then add the new generated ssh key by this [ proc of copying from Terminal. ](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
8. to the Github account SSH 
