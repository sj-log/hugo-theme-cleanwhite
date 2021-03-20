---
title: "Shell Practice by Daily Coding - Linux Course"
date: 2020-08-24T07:05:58+09:00
hidden: false
draft: true
tags: [linux, shell, server, TIL]
keywords: [Coding]
description: ""
slug: ""
---

This is the footage that I practiced my shell script.
It's all the preparation of 42Ecole Course.

#I'll access all the course in Shell script of [Egoing's website.](https://opentutorials.org/course/2598/14199)


# I didn't know that what is exactly `shell`

Shell is an User-Interface. That means, It is the communicator between a computer(or a machine) and a human.
Computer cannot work alone(yet). It does need to some orders to process by outside of the machine(from world). At that time, Human can order a task through this shell.

## A small shell script I made.

Usually making a post in Hugo blog folder in cmd, asks some typing. That has been a bit bugging me. So, It discouraged my working on Blog.






# Study log

## htop

can check system memory usage rate and cpu.
Kill pid, checking which program is over-performing etc.

## `|` pipe can be used 2 times for a command.

When we see an amount of lines from result, we can narrow the result by filtering multiple `|`

## Auto-macro `crontab -e` 
can make automatically schedules a program regularly.

`* 1 * * * ~/coding/kakaotalk-env/kakaotalk.bash restart`, can be done.
Above command can help reboot when the kakaotalk freezes up.


## What is `cat` in Sh?
A. Can make a file which is written a string buffer, print out the file, stdin/out possible.

## What is Unix?
A. [A widely used multiuser operating system.](https://www.google.com/search?q=UNIX+meaning&oq=UNIX+meaning&aqs=chrome..69i57j0l6j69i60.1911j0j7&client=ubuntu&sourceid=chrome&ie=UTF-8)

## What is IO Redirection?
A. Input and Output Redirection Unix process.

Q. What is the standard input in IO Redirection?
a. Standard Input(stdin) usually means 'Keyboard input' in shell.

## What are the differences between `;`, `&`, `&&`?
A1. `;` is just used to call the commands in sequence. Command by command.
A2. `&` is using for a command execution in `Background`.
A3. `&&` is using for when A command succeeded on the execution, then call next command. It related with `echo $?`. When `echo $?` typed, if the previous execution was failed, the number will be 1 or 127.(0 means succeeded on the command execution)

## Daemon?
A. Programs that always 

- `etc/init.d` is the place where all Daemon programs are located.
- All daemon programs have that commands `service <program name> stop/start`
- we can find the daemon program from the `etc/init.d/ $ ls -l`
- `cron` is a daemon.

## `alias`?

A. It does add the shortcut(nickname) on a command. We can just customize the shorter version of command.
e.g. `alias ..="cd.."`

When it combined with `/.bashrc` customization, it will automatically start the `alias`es when the shell starts.

It gives the users a lot of conveniences.


## Multi-tasking in sh

There is a background processing cmd in sh.
I didn't know that, so I had to move out `nvim` by `ZZ`. but, just I had to use `ctrl + z` which makes the current program to go to the background.

Besides, We can make a shell command in background when we call it by `&`.

# Conclusion 

## Shell is super fun.

It makes me doing something great with the cmd!
I like it.
It literally makes me using this computer much more instinctive way.
Sometimes just difficult putting the commends line by line, but there are a ton of way to avoid that repetition. So, would like to keep this course finished.


## Reference

1. [Daily coding - Linux course](https://opentutorials.org/course/2598/14217)

