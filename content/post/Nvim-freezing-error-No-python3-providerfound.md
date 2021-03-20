---
title: "Nvim Freezing Error No Python3 Providerfound"
date: 2020-08-06T16:36:35+08:00
hidden: false
draft: true
tags: [nvim, error]
keywords: [Coding]
description: "Error solution"
slug: ""
---

## Solution
simply 

`let g:python3_host_prog = $GLOBALINSTALLDIR . "/apps/nvim-py3/bin/python3"`

adding on `init.vim` was the solution.



## Reference

[Can g:python3_host_prog support environment variables?](https://github.com/neovim/neovim/issues/12234)
