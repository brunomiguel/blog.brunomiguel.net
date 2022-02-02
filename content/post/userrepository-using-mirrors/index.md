---
title: "Userrepository using mirrors"
date: "2021-10-16"
categories: 
  - "geekices"
tags: 
  - "arch"
  - "arch-linux"
  - "aur"
  - "fosshost"
  - "linux"
  - "package"
  - "repository"
  - "userrepository-eu"
---

For a few months, I considered using the [mirror service](https://docs.fosshost.org/en/home/mirrors-as-a-service) from [Fosshost](https://fosshost.org) in [userrepository.eu](https://userrepository.eu). The service results from a partnership between Fosshost and Fastly, giving projects access to [several PoP's](https://www.fastly.com/network-map) around the globe.

Finally, a few days ago, I enabled the service. I also created a package with the mirror's list, _userrepository-mirrors_, available in my repository and [AUR](https://aur.archlinux.org/packages/userrepository-mirrors/). The package has all the instructions for enabling the mirrors and what to do if you already have userrepository in your `/etc/pacman.conf` configuration.

The mirror service syncs every 4 hours. After each build, partial or full, the updated packages will be pushed to the servers with `rsync`.

If you're wondering why it took me so long, the answer is simple: fibromyalgia and pain 24/7.
