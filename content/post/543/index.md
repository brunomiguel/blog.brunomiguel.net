---
title: "Loving the Plasma Desktop"
date: "2018-11-17"
categories: 
  - "geekices"
tags: 
  - "kde"
  - "plasma"
  - "ubuntu"
featuredImage: "/post/543/images/desktop1.jpeg"
---

In the last few weeks, I've been using the **_Plasma Desktop_** full time in **_Ubuntu_** with the **_Kubuntu Backports PPA_** enabled. This way I can get the latest version of this desktop environment on _Ubuntu 18.10_.

The latest _Plasma Desktop_ version is 5.14 and it's really amazing. On my hardware, it uses less resources than **_Gnome Shell_**, although it takes more time to get to the destkop. And the best part is not having the _Gnome Shell_ process eating up more than 1GB or 2GB of _RAM_ (even after the garbage collection patches).

If you want to use the _Kubuntu Backports PPA_ too, one of the ways you can do it is opening your preferred terminal emulator and run the following command:

```
sudo add-apt-repository ppa:kubuntu-ppa/backports -y
```

After that, you can install the full _Plasma Desktop_. Or you can do like me, install only the minimum packages required to run it, plus a minimum of _KDE_ apps. This way you avoid having applications you won't use occupying disk space.

These are the apps I installed:

```
sudo apt install plasma-desktop xorg plasma-nm konsole dolphin plasma-workspace kde-config-gtk-style-preview kdeconnect gtk2-engines-qtcurve kde-style-breeze-qt4 dolphin-plugins systemsettings plasma-widgets-addons plasma-browser-integration plasma-applet-redshift-control plasma-pa plasma-nm kde-config-systemd kde-config-touchpad kde-config-plymouth kde-config-gtk-style kde-config-gtk-style-preview kde-config-cron kwin-addons network-manager-openvpn* plasma-widgets-addons plasma-runners-addons -y
```

That's it.
