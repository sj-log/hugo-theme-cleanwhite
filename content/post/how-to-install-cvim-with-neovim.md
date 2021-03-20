---
title: "How to Install Cvim With Neovim"
date: 2020-08-28T17:28:58+09:00
hidden: false
draft: true
tags: [C, Neovim, env, C complier]
keywords: [Coding]
description: "simple steps to install c compiler within Neovim."
slug: ""
---

1. Download `cvim.zip`, from https://www.vim.org/scripts/script.php?script_id=213

2. unzip `cvim.zip` into `~/.config/nvim/` where has `autoload` folder (confirm all duplication noticed files)

3. add following two lines into `~/.config/nvim/init.vim`

```
let  g:C_UseTool_cmake    = 'yes'
let  g:C_UseTool_doxygen = 'yes'
```

## result 

![Screenshot from 2020-08-28 17-28-04](https://user-images.githubusercontent.com/35059428/91539452-502ef200-e954-11ea-9d85-36781ea070d8.png)

