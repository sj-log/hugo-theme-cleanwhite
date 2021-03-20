---
title: "How to Solve Killed Git Error in Homebrew Mac"
date: 2021-03-20T20:09:00+09:00
draft: false
tags: [Mac, Brew, Xcode, Coding, Git]
---

## Error occured during Git installation without xcode

```
$ git

zsh: killed     git
```

What I have was only `brew`.
Didn't want to install `xcode`

## Check

```
$ brew config

HOMEBREW_VERSION: >=2.5.0 (shallow or no git repository)
ORIGIN: (none)
HEAD: (none)
Last commit: never
Core tap ORIGIN: (none)
Core tap HEAD: (none)
Core tap last commit: never
Core tap branch: (none)
HOMEBREW_PREFIX: /opt/homebrew
HOMEBREW_CASK_OPTS: []
HOMEBREW_MAKE_JOBS: 8
Homebrew Ruby: 2.6.3 => /System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/bin/ruby
CPU: octa-core 64-bit arm_firestorm_icestorm
Clang: 12.0 build 1200
Git: N/A
Curl: 7.64.1 => /usr/bin/curl
macOS: 11.2.3-arm64
CLT: 12.4.0.0.1.1610135815
Xcode: N/A
Rosetta 2: false
```

confirmed `Git : N/A`


## Fix

1. `brew uninstall git`
2. `rm -rf /opt/homebrew/etc/gitconfig`


