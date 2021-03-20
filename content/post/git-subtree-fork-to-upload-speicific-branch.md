---
title: "Fork app subtree was the solution to upload specific folder"
date: 2020-07-19T15:41:04+08:00
slug: "Fork app-subtree-was-the-solution-to-upload-specific-folder"
description: "한참을 걸려 완성시킨 git subtree 이해"
keywords: [Coding]
draft: false
tags: [coding, subtree, git, Fork]
math: false
toc: true
---


## Git was super difficult for me.

but it took the time to get used with, inevitably.

The matter of fact is that I needed to upload `public` folder which is the projection for this hugo blog.

When I just able to upload the `public`folder to the `gh-pages` only, during wrapping up all git changes, I was the only way to seperately manage the hugo blog well.

## the right way was `subtree`.

The git's `subtree` function is the way to control over specific folder with specific branch.

<img width="352" alt="Screen Shot 2020-07-19 at 15 48 09" src="https://user-images.githubusercontent.com/35059428/87870074-428e6000-c9d7-11ea-87bf-90fed710d502.png">

`subtree` can be used for the specific folder to specific branch alone within all marked by git.

[This website' guide was mostly helpful.](https://www.assertnotmagic.com/2018/03/08/publish-directories-to-github-pages/)

### How to use

`git subtree push --prefix public <repo url> <branch>`


## [Fork was good choice on Mac, to git GUI managing.](https://git-fork.com/)

And another thing that I mention, `Fork` app on Mac os, was useful to manage them.
When I don't understand about git how it works, the `fork` app reduces all burdens and time wasting.

Lovely.



## conclusion

- Git is difficult when I don't know how exactly work with.
- Need to understand each command how exactly it functions.
- Googling and [mindmapping](https://drive.google.com/file/d/1rFwMdiyg9vL9TWNT_xOyQ9KcKNUCydWZ/view?usp=sharing) each question marks are good way to get used with a new thing.
