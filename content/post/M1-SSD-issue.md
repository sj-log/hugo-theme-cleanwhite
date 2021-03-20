---
title: "M1 SSD Issue covered by using Apple Silicon Apps"
date: 2021-03-19T12:13:02+09:00
toc: true
tags: [Mac, M1, Macbook Air, Apple Silicon, Journal, Tech]
draft: true
authors : [Sj]
---

# My case

## 9 days usage, but need to use further.

Well, as far as I'm an Apple's big fan, successfully purchased Macbook Air M1 at 10th March.


## How to check the SSD leak

Smartmontools can check the issue by following commands.

```
brew install smartmontools && sudo smartctl --all /dev/disk0
```


<blockquote class="twitter-tweet"><p lang="en" dir="ltr">People with an M1 mac, please run `brew install smartmontools &amp;&amp; sudo smartctl --all /dev/disk0` and report back (and what kind of usage you make of the machine, especially RAM).<br><br>I&#39;m at &lt;600GBW on my MBP, but I don&#39;t use it heavily. <a href="https://t.co/LbhE9p7FiK">https://t.co/LbhE9p7FiK</a></p>&mdash; Hector Martin (@marcan42) <a href="https://twitter.com/marcan42/status/1361151198921826308?ref_src=twsrc%5Etfw">February 15, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## 9 days usage, but 1.24 TB?

When you see that Data Units Read, It seems abnormal for some Macbook M1 Pro or Air. 

<img width="475" alt="Macbook Air M1 abnormal Data Units Read" src="https://user-images.githubusercontent.com/35059428/111728245-d50d3900-88af-11eb-8fe5-b1d37acb145f.png" title="
My Macbook Air has 8 RAM and 258 SSD( Basic Model )
">

## The activities what I've done

Well, I've just used to Chrome, Notion app for note, installed Adobe Indesign and Premiere Pro(But only launched for neary 3 mins).

# Solution : Install Air-Silicon Apps

## Why it happens?

It caused by using the Non-M1 optimized apps.
The apps are not optimized for Rosetta 2 causes the exessive swap usage.

## Then how to solve it?

Need to use M1-optimized applications which named 'Apple Silicon'. Such as following image's **Mac with Apple Chip**

<img width="600" alt="Screen Shot 2021-03-19 at 2 26 36 PM" src="https://user-images.githubusercontent.com/35059428/111735281-1e18b980-88bf-11eb-9f7c-f441ea972dca.png">




## How to check my using apps are optimized for M1 and Rosetta 2?

Please click following link able to check that optimization! https://isapplesiliconready.com/

<img width="700" alt="A website you can check the compativitilies of Rosetta 2 and M1" src="https://user-images.githubusercontent.com/35059428/111733571-8ebdd700-88bb-11eb-9590-ddf716893ba1.png">







