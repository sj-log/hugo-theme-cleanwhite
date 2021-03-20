---
title: "Setting Env for C Lang in Ubuntu"
date: 2020-08-21T12:41:45+09:00
hidden: false
draft: true
tags: []
keywords: []
description: ""
slug: ""
---


## So, I had to turn My OS Debian into Ubuntu 20 LTS.
Why? because, I failed to install Debian.
It was super difficult as gave a try to install without any internet but only dualbooting with Window 10. I don't remember how many times should I had to turn on and log in and off.(sigh)

### failed to connect Bluetooth Tethering to having the ethernet.

Since I couldn't find out the proper wifi signal, tried to use 'Tethering' with the public officer offered Mobile Phone, but failed.
Couldn't have to find out any Bluetoothctl connection with the Mobile phone which I got offered for free.

### gave up because of `rfkill`

`rfkill block` had to be used, but In Debian, there is no command as `rfkill`, or another alternative.
So I couldn't unlock the block from bluetooth error. `bluez.blocked`.
Then, I just handed off from it.
It took almost a half of the day.
Yes. I wasn't sure the installation debian without internet deserves to take my time that much.

### Learned some about controlling Bluetooth, Ip configuration in command line. 

However, I've learned during that struggles about `How to turn up/down ip signals`by `ifdown -a`, `ifup <ethernet device name>`, `/etc/systemconf/network` setting, and etc.
That was almost the journey of problems then ended up 'hands off' but, It gave me above rewards.
because I didn't know at all how to control bluetooth and ethernet on cmd before.



## Of course Installing Ubuntu is easier than Debian.

Anyway, I keep required to install a Linux env.
As I wanna get used with 42ecole studying env.
So, kept installing any of linux. Ubuntu is the easiest and well shaped without any amount of time wasting.
I can feel the Ubuntu team works really hard.
Last time, 18.** versions were not stable but, this 20 LTS version is quite good to go :). The GUI is a kind of sexy as well.
I love their design :)
Well since last a few months of usage Debian, it made me used with Linux how to handle it, so It might be slightly affected to feel something easier about Ubuntu, but Yes That is true so many people try to use that Ubuntu, Especially in my Country.

## 42Ecole requires to study with C language.

As, It's the really good method to understand about the basic concept of computing. Ram, Memory, Variable, Address, Points, etc. Those concepts should have to be mastered during the 42 curriculum, Obviously.
So, I should have to install C lang in this Ubuntu.

### this is the stages to install C language coding environment.

#### Needs

1. C Compiler
- [llvm-project's C compiler](https://jdhao.github.io/2020/04/19/nvim_cpp_and_c_completion/)
2. IDE(Intergrated Development Environment)
        - vi- for 42 students
        - for me, I chosen Neovim, as it's a mostly satisfied ide in Vi series.

           

### How?

```
$ git clone https://github.com/llvm/llvm-project.git
$ cd llvm-project
$ mkdir build && cd build
$ sudo apt-get update && sudo apt-get install build-essential
$ cmake -DLLVM_ENABLE_PROJECTS=clang -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release  ../llvm
$ cmake -build .
```

but It got an error as 


```
collect2: fatal error: ld terminated with signal 9 [Killed]
compilation terminated.
```

[and tried to find out what is the errors meaning.](https://groups.google.com/g/llvm-dev/c/KH3DHQo0A38?pli=1)


so retried with 
`$ cmake -DCMAKE_BUILD_TYPE=Release -build .`



