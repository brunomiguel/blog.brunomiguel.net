---
title: "How to block ZIP and MOV TLDs in uBlock Origin and AdGuardHome"
summary: "The ZIP and MOV TLDs are a godsend for scammers. If you want to know how to block them with uBlock Origin and AdGuardHome, I created a block list for you to use."
description: "The ZIP and MOV TLDs are a godsend for scammers. If you want to know how to block them with uBlock Origin and AdGuardHome, I created a block list for you to use."
date: 2023-05-18
categories:
  - "geekices"
tags:
  - "privacy"
  - "zip"
  - "mov"
  - "tld"
  - "security"
  - "ublock origin"
  - "adguardhome"
cover:
  image: "post/blocking-zip-mov-tlds/images/jose-aragones-81QkOoPGahY-unsplash.webp"
  alt: "Privacy"
---

Google [introduced](https://www.blog.google/products/registry/8-new-top-level-domains-for-dads-grads-tech/) a handful of new Top Level Domains (TLDs). Among them are two that are a godsend for scammers and crooks: .zip and .mov. The cybersecurity community is raising concerns about them, especially the .zip one, and with good reason. If you want to dig into the reasoning, read an [article on Medium](https://medium.com/@bobbyrsec/the-dangers-of-googles-zip-tld-5e1e675e59a5) or this one at [Bleeping Computer](https://www.bleepingcomputer.com/news/security/new-zip-domains-spark-debate-among-cybersecurity-experts/).

When [João](https://masto.pt/@jt_rebelo) tagged me on a Mastodon thread about this, I took the opportunity to create block lists for both uBlock Origin and AdGuardHome. After a boxing match with Regex, I finally _knocked it out_ and published two working lists for the software mentioned above. You can grab them at [Codeberg](https://codeberg.org/brunomiguel/adguardhome-block-zip-tld/) or [Github](https://github.com/brunomiguel/adguardhome-block-zip-tld).

Both lists have the same Regex. However, having one for each software will allow me to make specific changes for any of them if needed.

Not all .zip and .mov TLDs will serve malware, phishing pages, or other sketchy content. I'm aware of that. These lists will keep you safe from them by default, and you can add exceptions to sites you trust. They will also be a good safeguard for those family members and friends that aren't tech-savvy.

<small>_Image from [Unsplash](https://unsplash.com/photos/81QkOoPGahY)_</small>
