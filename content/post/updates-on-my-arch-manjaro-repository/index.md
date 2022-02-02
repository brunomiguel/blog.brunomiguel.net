---
title: "Updates on my Arch/Manjaro repository"
date: "2019-03-26"
categories: 
  - "geekices"
tags: 
  - "arch"
  - "aur"
  - "aurto"
  - "gnu-linux"
  - "linux"
  - "manjaro"
  - "repository"
---

Ever since Carlos Silva left a [comment](http://blog.brunomiguel.net/geekices/ive-built-a-manjaro-repository/#comment-1114) on my last post about this repository, I was left wondering if it wouldn't be better to migrate my current _VM_ to _Scaleway_. The price/specs seemed better and for the marginal difference of €1 I would get a dual-core virtual machine with 2GB of _RAM_ and 50Gb of disk space.

After a couple of weeks of reflection, I bought a _“Start1-S” VPS_ for €3,99/month and I've been (successfully) testing _[aurto](https://github.com/alexheretic/aurto/)_ to manage the repository updates. Things have been working out so great that I bought the [userrepository.eu](http://userrepository.eu) domain.

_(I will add a certificate to the website, I promise!)_

The address has all the instructions for you to add it to your system. But in case you can't visit right now, here's what you need to add to the _/etc/pacman.conf_ file:

\[aurto\]  
Server = http://51.15.233.8  
SigLevel = Optional TrustAll 

I remind you, dear reader, that this repo only contains _AUR_ packages.
