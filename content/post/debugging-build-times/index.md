---
title: "Debugging build times"
date: "2020-04-17"
categories: 
  - "geekices"
tags: 
  - "jarvis"
  - "packages"
  - "repository"
  - "userrepository-eu"
featuredImage: "/post/debugging-build-times/images/jarvis-news.jpg"
---

**Lately, the repository has been taking +10 hours to compile all the packages.** I think that's a lot for **a little more than 250 packages**, most of them small utilities and/or `_-bin_` files from _AUR_, built in a _DEV1-L_ (4 cores, 8 Gb _RAM_) virtual machine from _Scaleway_.

After investigating the matter, I found out that **12 of the packages took four hours and sixteen minutes to build.**

| Pkg | Hours | Minutes |
| --- | --- | --- |
| ./pueue/makepkg.log | 0 | 12 |
| ./ffsend/makepkg.log | 0 | 15 |
| ./joplin/makepkg.log | 0 | 15 |
| ./bandwhich/makepkg.log | 0 | 16 |
| ./session-desktop/makepkg.log | 0 | 17 |
| ./mindforger/makepkg.log | 0 | 17 |
| ./giada-git/makepkg.log | 0 | 17 |
| ./brackets/makepkg.log | 0 | 21 |
| ./newbreeze-git/makepkg.log | 0 | 24 |
| ./falkon-git/makepkg.log | 0 | 24 |
| ./newsflash-git/makepkg.log | 0 | 31 |
| ./firefox-kde-opensuse/makepkg.log | 0 | 47 |
|  |  | 256 |

I decided to give it a go at reducing the packages build time. The first set of changes I made were:

- remove _newsflash-git_;
- remove _newbreeze-git_;
- remove _giada-git_;
- replace _firefox-kde-opensuse_ with _firefox-kde-opensuse-rpm_;
- _session-desktop_ with _session-desktop-bin_.

.ugb-8f198eb .ugb-cta\_\_item{background-color:#fff3ef !important}.ugb-8f198eb .ugb-cta\_\_item:before{background-color:#fff3ef !important}.ugb-8f198eb .ugb-cta\_\_title{color:#e36d60}

#### If you used any of the packages I removed, please let me know and I'll add it again

Next, I inserted the `_MAKEFLAGS="-j4"_` environment variable in the `_config_` file, so that compilers use the four cores when possible.

| Pkg | Hours | Minutes |
| --- | --- | --- |
| ./brackets/makepkg.log | 0 | 20 |
| ./bamr/makepkg.log | 0 | 19 |
| ./falkon-git/makepkg.log | 0 | 19 |
| ./joplin/makepkg.log | 0 | 15 |
| ./ffsend/makepkg.log | 0 | 15 |
| ./mindforger/makepkg.log | 0 | 13 |
| ./pueue/makepkg.log | 0 | 12 |
| ./broot/makepkg.log | 0 | 7 |
| ./navi/makepkg.log | 0 | 7 |
| ./boostnote-bin/makepkg.log | 0 | 7 |
| ./qownnotes/makepkg.log | 0 | 7 |
| ./kitematic-git/makepkg.log | 0 | 6 |
|  |  | 147 |

**With the above changes, the twelve "worst offenders" decrease to almost two and an half hours.** The total build time is likely to decrease a little more after I take a look at what packages `_[userrepository](https://userrepository.eu/)_` shares with `_[chaotic-aur](https://lonewolf.pedrohlc.com/chaotic-aur/)_` and decide which, if any, I should remove.

In the _TODO_ list are also some tests to be made to the _zstd_ compression level. The current level is _10_, with the default being _3_. I intend to see if the trade-off between the increase in package creation time and the reduction in package size is worth increasing the level to somewhere between _15_ and _19_, the highest preset level.

Eventually, I'll begin to sign the packages. For now, enjoy the latest batch and **[become a patron](https://www.patreon.com/bePatron?u=31667183&redirect_uri=https%3A%2F%2Fuserrepository.eu%2F&utm_medium=widget).**
