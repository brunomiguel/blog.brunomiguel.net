---
title: "How to disable a D-Bus service"
date: "2021-09-16"
categories: 
  - "geekices"
tags: 
  - "dbus"
  - "dunst"
  - "linux"
  - "notification-daemon"
  - "plasma-desktop"
  - "tips"
featuredImage: "/post/how-to-disable-a-d-bus-service/images/on-off.jpg"
---

In some situations, you might want to disable a D-Bus service. One of those is, for example, when you use Dunst (a notification daemon) with a window manager. Still, you don't want it to replace the notification daemon from your desktop environment.

To disable it, you just need to add `.disabled` to the end of the target file name. Example:

```
sudo mv /usr/share/dbus-1/services/org.knopwob.dunst.service /usr/share/dbus-1/services/org.knopwob.dunst.service.disabled
```

In the above example, Dunst will no longer replace Plasma Desktop notification daemon when using that amazing desktop environment, and all will be good with the world again. Victory! :)
