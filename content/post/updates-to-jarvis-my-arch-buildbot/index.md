---
title: "Updates to Jarvis, my Arch buildbot"
date: "2019-12-04"
categories: 
  - "geekices"
tags: 
  - "arch"
  - "arch-linux"
  - "bash"
  - "jarvis"
  - "userrepository-eu"
featuredImage: "/post/updates-to-jarvis-my-arch-buildbot/images/jarvis.jpg"
---

My _Arch_ buildbot, [Jarvis](https://github.com/brunomiguel/userrepository), received an update today in the options logic. Now, it can receive an argument in the add (-a) and delete (-d) options, so the user can specify the package to add or delete.

The option to add a package, for now, only works for _AUR_. If you want to add a package that's not in _AUR_, you'll need to manually add the submodule. In the future, _Jarvis_ will allow you to use a _git_ repository with a _PKGBUILD_ file.

Tony Stark would be jealous. ;)
