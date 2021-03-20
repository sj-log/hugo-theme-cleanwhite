---
title: "Hard Time"
date: 2020-08-30T20:05:49+09:00
hidden: false
draft: true
tags: [Secure Boot, TIL, Windows, Linux, OS, UEFI, Partition]
keywords: [Coding]
description: "7 hours struggling to install dual OS env. If you don't install window first, you will waste an amount of time. This is the legacy of my struggle."
slug: ""
---



Today, I had to install the windows again.
But, didn't know how to figure out the Dual booting properly.
a number of struggling and errors, just gave up to install Debian, instead of Ubuntu.
Easy thing is right on this super complicating life.

[An article was highly helpful to getting through.](https://itsfoss.com/install-ubuntu-1404-dual-boot-mode-windows-8-81-uefi/)

The point is, 'Window must be installed first'.
I couldn't figure out the reason, but it seems about 'Secure boot'.
didn't confirm whether the boot UEFI goes wrong when installed Linux distribution first.
However, It was too difficult flip over the 'Linux firstly installed system' into consisting env with Windows.

Otherwise, Above link was truly helpful.

## TIL

- To successfully install Linux distributions, there needs 3 partitions. `/root`,`/home`,`/swap`.
- To install Ubuntu, around 20GB on the /root partition is sufficient.
- at /swap partition, the size of storage must be above the double of RAM size.
- at /home partition, we can put just rest of storage as much as we have.
- NTFS is mostly recommended to install Windows, ext4 is for Linux partition.
- Windows has the blocking system which is called 'Secure Booting'. The secure booting mode supposes to discourage of incidents from Firmwares or mal-functioning programs. However, the booting mode kills to Linux distributions booting runs.
- Windows secure booting mode can be turned off by BIOS 'security' menu.
- UEFI booting mode has the same function as 'Secure booting'.
- Legacy mode is automatically functioning 'turning off secure booting mode'.
- So thus, to activate Linux OS booting, must be turned off UEFI or Secure booting Windows.
- Veroy 

## Conclusion

### Wish "Please process faster 'the Windows to linux project'"

This governments got moving on the all OS of government processing from Windows to Linux. but it would be all replaced after 2-3 years from now. It will make a synergy by This government's educational plan that all citizens to encourage the learning Software.

For just using internet bank or identity verification in browser makes me using my time around 6-7 hours to install Windows again and again.
I feel a bit sick of it.

But I learned a lot about the partition as mentioned above.

### Ventoy works great.

As long as I need Windows to survive in S.Korea's public webservice, Switching from Windows to Linux are necessary. 
But the application is helpful so far. Usually USB Booting stick allowed only 1 IOS to cover. But the Ventoy lets multiple ISO could be recognizable.




## Reference


1. [Ventoy](https://www.ventoy.net/en/index.html)
