---
title: "Some statistics for Userrepository"
date: "2020-08-14"
categories: 
  - "geekices"
tags: 
  - "arch-linux"
  - "ddos"
  - "userrepository-eu"
---

You might have noticed that [_Userrepository_](https://userrepository.eu) uses _Cloudflare_. I chose it for two main reasons: their ability to help mitigate _(D)DoS_ attacks and to help _hiding_ the _IP_ address for the _VM_ from script kiddies.

It's not that I think _Userrepository_ will ever be a target for a _(D)DoS_ attack, but better safe than sorry. Also, I have more than enough automated failed _SSH_ authentication attempts without revealing the _IP_: 441 blocked _IP_s and counting for one _fail2ban ssh_ rule and 2 for another _fail2ban ssh_ rule. I intend to tighten these rules in the near future.

A third (lesser) reason is their analytics. This allows me to evaluate, from time to time, if the repository is of interest for _Arch_ and _Arch_\-based Linux distribution users.

Although the analytics part is not the best-in-breed, it lets me take a look at the stats for the last 30 days. For example, in this time frame, at the time of writing of this blog post, I had 1486 unique visitors and 17622 total requests to _[userrepository.eu](https://userrepository.eu)_. I honestly expected around half that number at best.

Most of these unique visitors (and hopefully users), from first to last, come from France, Germany, Italy and USA. My country, Portugal, still hasn't reached the 500 unique requests.

In terms of bandwidth statistics, the numbers are low: 10.14GB in the last 30 days, with only 878.35kB of cached content. This is expected because I doubt they would cache compressed files, but they're probably caching the [01-README.txt](https://userrepository.eu/01-README.txt) file with the instructions to add the repository to your `/etc/pacman.conf` file.

The numbers, I must admit, are not what I wanted but they are more than I expected and that's a strong motivation to keep the project running, hoping it will help other users.

One last thing: **[please become a Patron](https://www.patreon.com/brunomiguel)** if you want to support userrepository.eu. Even €1 will help cover the monthly expenses, just over €15. If I get enough patrons, I’ll be able to upgrade the _virtual machine_ to one with better specs, which will allow a higher package compression level, shorter build times and maybe even packaged kernels. Thank you!
