---
title: "Updates on userrepository"
date: "2020-07-11"
categories: 
  - "geekices"
tags: 
  - "arch-linux"
  - "manjaro"
  - "userrepository-eu"
---

Since the [last post](https://blog.brunomiguel.net/geekices/some-notes-about-userrepository-performance-with-the-new-provider/) about my _Arch_ (and _Arch_\-compatible distributions) [binary repository](https://userrepository.eu), I've added a few more packages. Some examples are the _Mullvad VPN_ desktop client and _[nimdow](https://github.com/avahe-kellenberger/nimdow)_, a _window manager_ written in the _Nim_ programming language. Or [Emptty](https://blog.brunomiguel.net/geekices/emptty-a-blazing-fast-display-manager/), an amazing _display manager_ that I encourage you to try.

Despite adding more packages, the compilation and compression time only had a small increase and I'm still below the 5 hour mark. And I've kept the _zstd_ "-12" compression level.

Right now, I'm doing a full build to time it again. If it keeps below the 5 hour mark, I'll try to increase the compression level to "-15" to see if the trade-off is worth it. If so, you'll have smaller packages, allowing you to save bandwidth.

I'll keep you updated as soon as I make the change. But that might take a few days, because work and stuff.

One last thing: **[please become a Patron](https://www.patreon.com/brunomiguel)** if you want to support userrepository.eu. Even €1 will help cover the monthly expenses, just over €15. If I get enough patrons, I’ll be able to upgrade the _virtual machine_ to one with better specs, which will allow a higher package compression level, shorter build times and maybe even packaged kernels. Thank you! 🙂
