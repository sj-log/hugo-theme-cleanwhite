---
title: "Made a Shell to Automatically Install Dictionary in Linux"
date: 2020-08-26T12:07:07+09:00
hidden: false
draft: true
tags: [Shell, Script, Dictionary, Linux]
keywords: [Coding]
description: "Maybe this will be useful when I change my laptop or new env of dev."
slug: ""
---

While I've studied the C Programming language, needed to look up a word on the book.
[This was the solution to add in flexible way, and able to use underbar of Vim env.](
https://askubuntu.com/questions/191125/is-there-an-offline-command-line-dictionary#answer-191268)

but the procedures to download and to install the files look better if there would be a shell script to simplify the installation.
so, I've wrote some lines.

```
#!/bin/bash

# tarball links of dicts
tcide=https://web.archive.org/web/20140917131745/http://abloz.com/huzheng/stardict-dic/dict.org/stardict-dictd_www.dict.org_gcide-2.4.2.tar.bz2
jargon=https://web.archive.org/web/20140917131745/http://abloz.com/huzheng/stardict-dic/dict.org/stardict-dictd-jargon-2.4.2.tar.bz2
foldc=https://web.archive.org/web/20140917131745/http://abloz.com/huzheng/stardict-dic/dict.org/stardict-dictd_www.dict.org_foldoc-2.4.2.tar.bz2
merrian=https://web.archive.org/web/20140917131745/http://abloz.com/huzheng/stardict-dic/dict.org/stardict-merrianwebster-2.4.2.tar.bz2

dictpath=/usr/share/stardict/dic
i=1
filecnt=$(ls *.bz2 | wc -l)

# sh
# 1. download check
if [ `ls *.bz2 | wc -l` -gt 0 ];
then 
	echo "already downloaded"
else
	sudo apt-get install sdcv
	sudo wget -N "$tcide" "$jargon" "$foldc" "$merrian"
	sudo mkdir -p "$dictpath"
fi

until [ $i -gt "$filecnt" ];
do
	echo i: $i
	filename=$(ls *.bz2 | sed -n "$i"p)
	sudo tar -xvjf $filename -C $dictpath
	((i=i+1))
done

```
