---
title: "I've built a Manjaro repository"
date: "2019-02-11"
categories: 
  - "geekices"
tags: 
  - "arcan1s"
  - "aur"
  - "linux"
  - "manjaro"
  - "packages"
  - "repository"
  - "vps"
featuredImage: "/post/ive-built-a-manjaro-repository/images/manjaro-repo.jpg"
---

Due to my own dumbness (I mistakenly deleted my _Ubuntu_ partition), I installed _Manjaro_, using the _Manjaro Architect_ release, on my laptop. I'd been thinking about doing it for a while and finally made it because I was too stupid to read the instructions from _cfdisk_. The shit you create yourself because you're in a hurry…

Anyway, after installing _Manjaro_, I started reading a bit about this _distro_ packaging and how I could leverage _AUR_ and binary packages. Inspired by the work of Arcan1s, I bought a cheap _VPS_ from _OVH_ \[almost €3/month\] and built my repository using [Arcan1s scripts](https://github.com/arcan1s/repo-scripts/). It took a bit of fiddling around the config file and the scripts to customize it to the _VPS_ low raw power, but I eventually got it.

One thing you'll notice is the packages are not signed. I do intend to start signing them but I don't have a time frame for that just yet.

If you want to try out my repository, made from _AUR_ packages, add this to your _/etc/pacman.conf_ file:

```
[bruno]
Server = http://51.77.244.118/$arch
SigLevel = Optional TrustAll
```

The server checks for updates for the packages every 6 hours. This is mainly due to the fact that the _VPS_ is low end - only 1vCPU @2GHz, 2GB of RAM and 20GB of disk space.
