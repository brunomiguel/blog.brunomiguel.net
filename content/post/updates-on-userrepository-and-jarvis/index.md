---
title: "Updates on Userrepository and Jarvis"
date: "2020-09-12"
categories: 
  - "geekices"
tags: 
  - "aur"
  - "endeavouros"
  - "manjaro"
  - "userrepository"
featuredImage: "/post/updates-on-userrepository-and-jarvis/images/jarvis.jpg"
---

Lately, I've been having some problems when building `picom-ibhagwan-git` and `picom-tryone-git`. The first one would build OK, but not the second one.

After a bit of debugging, I found out that it was a problem related to the way _makepkg_ and _git_ handle the cache when building these forks. This would also happen when adding the `picom-git` package: it would build because it's the first package in alphabetical order and Jarvis builds the packages that way, but not the other two.

To fix this, the `build()` function no longer uses _pushd_ and _popd_, allowing the script to work outside the package directory it's building and delete some parts of the cache folder **_Jarvis_** uses.

This has the upside of allowing a better cache cleaning when building the packages. In a future commit, it will clean after itself better, up to a point it cleans every cache and artifact generated during a build.

And yes, `$HOME/.npm` and `$HOME/.cargo` I'm looking at you both.

There will be an exception, though: the `makepkg.log` file in every _submodule_ folder because I use it as a log file for the package build.

Unrelated to this issue is the removal of the `onivim2-git` package. It takes some time to build and lately it would ask human intervention to confirm some steps, which is not compatible with the way _Jarvis_ builds the packages and because the script is meant to be a tool to build the packages in an automated way.

One last thing: **[please become a Patron](https://www.patreon.com/brunomiguel)** if you want to support userrepository.eu. Even €1 will help cover the monthly expenses, just over €15. If I get enough patrons, I’ll be able to upgrade the _virtual machine_ to one with better specs, which will allow a higher package compression level, shorter build times and maybe even packaged kernels. Thank you!
