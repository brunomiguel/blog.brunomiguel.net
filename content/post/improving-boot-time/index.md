---
title: "Improving boot time"
date: "2020-04-30"
categories: 
  - "geekices"
tags: 
  - "arch-linux"
  - "boot-times"
  - "endeavouros"
  - "linux"
  - "lz4"
  - "mkinitcpio"
  - "mq-deadline"
  - "systemd"
---

Today, I've decided to try and improve the boot time of my laptop, running _EndeavourOS_. There was no special reason for it other than "Why not?".

The first thing I made was disabling or masking the following _systemd_ services:

- systemd-resolved disabled
- tlp disabled
- NetworkManager-wait-online disabled
- lvm2-monitor masked
- org.cups.cupsd disabled
- packagekit masked
- bluetooth disabled (I rarely use the laptop's bluetooth)
- blueman-mechanism disabled

With this, I was able to save a few milliseconds and decrease the enabled _systemd_ units to 15, but the impact was negligible.

brunomiguel@kepler: ~
└─ $: systemctl list-unit-files --state=enabled --no-pager
UNIT FILE STATE VENDOR PRESET
autovt@.service enabled disabled
avahi-daemon.service enabled disabled
dbus-org.freedesktop.Avahi.service enabled disabled
dbus-org.freedesktop.nm-dispatcher.service enabled disabled
display-manager.service enabled disabled
getty@.service enabled enabled
haveged.service enabled disabled
NetworkManager-dispatcher.service enabled disabled
NetworkManager.service enabled disabled
sddm.service enabled disabled
systemd-swap.service enabled disabled
unbound.service enabled disabled
avahi-daemon.socket enabled disabled
remote-fs.target enabled enabled
roothints.timer enabled disabled

15 unit files listed.

To further improve the boot time, I tested _bfq_, _kyber_ and _mq-deadline_ _I/O schedulers_. From the three, the last one allowed to shave off another few milliseconds to the boot time. Next, and last, I changed the _mkinitcpio_ _ramdisk_ compression to lz4 with the default compression options.

With this changes, I went from 17.040 to 15.511 seconds, decreasing a bit more than one and an half seconds in the boot time.

brunomiguel@kepler: ~  
└─ $: systemd-analyze time  
Startup finished in 10.145s (firmware) + 1.616s (loader) + 2.027s (kernel) + 3.250s (userspace) = 17.040s  
graphical.target reached after 2.934s in userspace  
  
brunomiguel@kepler: ~  
└─ $: systemd-analyze time  
Startup finished in 10.175s (firmware) + 686ms (loader) + 2.041s (kernel) + 2.608s (userspace) = 15.511s  
graphical.target reached after 2.529s in userspace

In the future, I might replace _GRUB2_ with _systemd-boot_, possibly decreasing the boot time even more.

This was tested in a _AMD A9-9420 CPU_ with the _linux-zen_ kernel. Your mileage may vary depending on your hardware.
