---
title: "Status on userrepository changes"
date: "2020-08-13"
categories: 
  - "geekices"
tags: 
  - "arch"
  - "arch-linux"
  - "linux"
  - "manjaro"
  - "pacman"
  - "userrepository-eu"
---

It took me a while to update you about the latest changes to my _Arch_ and _Arch_\-compatible _Linux_ distributions repository. But first, let me apologize for the delay: work, personal life and, for about 3 weeks now, a horrible back pain (that just doesn't stop, even with an handful of medication) have kept me from doing this in the time frame I expected.

First on the "agenda", I experimented with increasing the _zstd_ compression level for the packages like I said I would do in my [last post about the repository](https://blog.brunomiguel.net/geekices/updates-on-userrepository/). The trade-off was not worth it: the increase in packaging time was far superior to the small decrease in package size. So, I'll keep the _zstd_ compression level to "-12" in the foreseeable future.

Also, up to a few days ago, I would manually update the packages and, from time to time, do a full build. Now, I'm using a _cron job_ and [_pueue_](https://github.com/Nukesor/pueue) to manage the tasks and it always does a full build.

If you don't know _pueue_, this application is a command-line task management tool for sequential and parallel execution of long-running tasks. Besides adding tasks, you can watch the logs for them, the exit codes and even follow what the task is doing (just like using "`tail -f /destination/file`"). But _pueue_ can do much more. Go [check it out](https://github.com/Nukesor/pueue) at Github.

[Userrepository.eu](http://userrepository.eu) also has a few more packages. For example: _vimtips_, _wego_, _wttr_, _plymouth_ and _performance-tweaks_. All of them are at _AUR_ and at the [_Git_ repository](https://github.com/brunomiguel/userrepository/commits/master) where I have _userrepository.eu_ sources, if you want to take a look at the commits (just ignore some of the commit messages, because I can be lazy with them at times ^^').

One last thing: **[please become a Patron](https://www.patreon.com/brunomiguel)** if you want to support userrepository.eu. Even €1 will help cover the monthly expenses, just over €15. If I get enough patrons, I’ll be able to upgrade the _virtual machine_ to one with better specs, which will allow a higher package compression level, shorter build times and maybe even packaged kernels. Thank you!
