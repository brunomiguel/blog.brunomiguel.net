---
title: "Userrepository.eu is back (in beta)"
date: "2020-06-01"
categories: 
  - "geekices"
tags: 
  - "arch-linux"
  - "hetzner"
  - "scaleway"
  - "userrepository-eu"
---

After a small forced hiatus, [userrepository.eu](http://userrepository.eu) is back. The Covid-19 pandemic made a hit in my income and the wife's income, so I had to temporarily suspend non-priority expenses. During this period, I had time to consider a few things about the future of the project and decided to change the provider from _Scaleway_ to _Hetzner_, mostly because the _Arch_ image they're using is essentially _abandonware_.

If you're reading this, you'll probably know that _Arch Linux_ changed the default package compression to _ZSTD_. In order to update or install any package, you'll need a _pacman_ version that supports this compression and up-to-date libraries. These requirements aren't met in older _Arch_ images, like the one used by _Scaleway_, so the only two solutions were installing another distribution, _chrooting_ into it and hack an _Arch_ install (the solution presented to me by _Scaleway_ support) or change provider. The second option was the less time-consuming one.

_Hetzner_ doesn't provide _Arch_ by default when creating a virtual manchine, but after creating it the user can boot it in rescue mode and run the _installimage_ script that makes the process almost a breeze. After running the script, I advise you to manually _chroot_ and temporarily allow root logins for the _SSH_ daemon in order to be able to login remotely after booting the _VM_ normally.

The virtual machine configuration I chose has similar specs to the previous one with _Scaleway_: 4vCPUs and 8GB of RAM. In the first few hours of use, I noticed a small improvement in package compile times - but this is just my perception; I have yet to time the build times. But even things like refreshing the repository package list is faster, way faster, and that's really noticeable.

For the time being, I'll consider userrepository.eu in beta state, so use it with some degree of carefulness. The source is the same, but I changed the provider and I'm evaluation the virtual machine and network performance. Let's see how it goes.
