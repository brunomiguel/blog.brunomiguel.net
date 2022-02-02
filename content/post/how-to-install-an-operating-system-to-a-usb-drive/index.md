---
title: "How to install an operating system to a USB drive"
date: "2018-08-28"
categories: 
  - "geekices"
tags: 
  - "linux"
  - "qemu"
  - "usb"
featuredImage: "/post/how-to-install-an-operating-system-to-a-usb-drive/images/Captura-de-ecrã-de-2018-08-28-22-58-35.png"
---

Sometimes, maybe for maintenance or data rescue reasons, you may want to have a _USB_ thumbdrive with a _GNU/Linux_ distribution installed. I'm not referring to writing a live _ISO_ to a _USB_ drive; I really mean having the distribution installed like it would be on an hard drive. An easy way to achieve this is using the virtualization software _Qemu_. Example:

```
sudo qemu-system-x86_64 -boot d -cdrom void-live-x86_64-20171007.iso -hda /dev/sdb -m 800
```

In this example, the `-hda /dev/sdb` part tells _Qemu_ that the device _/dev/sdb_ (the _USB_ drive) must be used as an hard drive.

If you prefer _Ubuntu_, _Fedora_, _Arch_ or any other distribution, you can install them this way too. There may be a need to adjust _QEMU_ arguments, but in that case _Google_ is your friend.  

This also works with other operating systems that are not _Linux_ based. [_OpenBSD_](https://openbsd.org), version 6.3, can be installed in a _USB_ drive using the same parameters and booted after that.
