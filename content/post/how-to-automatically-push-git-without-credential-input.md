---
title: "How to Automatically Push Git Without Credential Input"
date: 2020-07-28T05:17:08+08:00
hidden: false
draft: false
tags: [git, push, credential, automatic]
keywords: [coding]
description: "Isn't it so disturbing that you have to input all the time that your user id and password for pushing?"
slug: "How-to-Automatically-push-git-without-credential-input"
---

## The problem
So, the problem was that I had to keep writing down my credential info for pushing onto git repo.

## Solution

1. `git config credential.helper store`

2. `git push <repo>`

3. `git config --global credential.helper "cache --timeout 7200"`
        This setting will expire your cached credential info for 2 hours later.


## Conclusion

- `git config credential.helper store` commands order to store the git user info (pw, id) in local env
        - It can raise security issue.
- so, `git config --global credential.helper "cache --timeout 7200"` can be the solution to prevent the security issue before it happening.


## Ref

[git docs - credentials](https://git-scm.com/docs/gitcredentials)

[Stackoverflow - answer](https://stackoverflow.com/questions/11403407/git-asks-for-username-every-time-i-push#answer-28562735)
