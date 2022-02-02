---
title: "Emptty, a blazing fast Display Manager"
date: "2020-07-05"
categories: 
  - "geekices"
featuredImage: "/post/emptty-a-blazing-fast-display-manager/images/emptty.jpg"
---

[**Emptty**](https://github.com/tvrzna/emptty) is one of the newest additions to [userrepository.eu](http://userrepository.eu) and already **a favorite of mine**. **This _CLI Display Manager_ is blazing fast and offers a few configuration options.**

One of these options and my personal favorite is setting the [_MOTD_](https://en.wikipedia.org/wiki/Motd_(Unix)), like the one you see on the post image. As far as I can tell, it only supports plain text and _ANSI_ color escape codes. If the possibility for scripts arises, it can allow some really cool stuff.

I'm already picturing it: lolcat all the things! But I drool... I mean, digress.

You can also choose the _TTY_ where it'll run, set auto login, create custom sessions just for _emptty_ and a couple for customization options you can check over at [_Github_](https://github.com/tvrzna/emptty).

And _.xinitrc_ users, _emptty_ has your back.

> .ugb-7a2b41a .ugb-blockquote\_\_quote{opacity:0.6;width:48px !important;height:48px !important}.ugb-7a2b41a .ugb-inner-block{text-align:left}
> 
> **${HOME}./xinitrc**  
> If config `XINITRC_LAUNCH` is set to true, it enables possibility to use .xinitrc script. See [samples](https://github.com/tvrzna/emptty/blob/master/SAMPLES.md#xinitrc)

The package is in version _v0.2.0.r12.44b809d-1_ at the time of publishing of this post. In this version, the package has:

- 745,34Kib of download size
- 1910,79Kib of used disk space after install
- ~6,8Mib of used RAM when running

As you can see, it's really lightweight. At least as important, **it looks really nice and gives a nostalgic vibe.**

If you like efficiency, I think you'll love this _CLI Display Manager_ written in _Go_. To install it, assuming you already have _userrepository_ in your repository list, just run:

sudo pacman -Syuv emptyy-git

One last thing: **[please become a Patron](https://www.patreon.com/brunomiguel)** if you want to support userrepository.eu. Even €1 will help cover the monthly expenses, just over €15. If I get enough patrons, I'll be able to upgrade the _virtual machine_ to one with better specs, which will allow a higher package compression level, shorter build times and maybe even packaged kernels. Thank you :)
