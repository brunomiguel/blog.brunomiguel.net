---
title: "Finding a new Tmux session manager"
summary: "I was using Tmuxinator, but I was having issues compiling newer versions because it required a newer version of Ruby not available in Arch Linux at the time of writing"
description: "I was using Tmuxinator, but I was having issues compiling newer versions because it required a newer version of Ruby not available in Arch Linux at the time of writing"
date: 2023-02-27
categories:
  - "geekices"
tags:
  - "tmux"
  - "tmuxinator"
  - "tmuxp"
  - "smug"
cover:
  image: "post/finding-new-tmux-session-manager/images/smug.webp"
  alt: "Foto do Chico no parapeito da janela da varanda"
---

Since my repository went offline, I've had to build the AUR packages I use locally. No issue here. Well, except for Tmuxinator, a Tmux session manager I was using, required a newer Ruby version than the one available in Arch Linux repositories at the time of writing. The update to Ruby will eventually come, but I don't want to wait, so I went to look for a new session manager for Tmux.

The first one I tried was Tmuxp, present in the Arch Linux repositories and written in Python. The configuration is similar to the one Tmuxinator uses, written in YAML, but it also supports JSON. Almost everything worked well, except for one very annoying issue in the way it dealt with the way I like to have the panes in my first window. I use three panes for the first window: one vertical (the main one) and two horizontal. For whatever reason, the first one was displayed with the width of the block character. I can resize it, but having that minuscule width isn't very pleasant! I looked at the documentation, but there's only mention to the height of a pane, not the width.

Since Tmuxp was a bust due to that weird and annoying behavior, I looked at AUR for another one. That's where I found Smug, a Tmux session manager written in Go. Like Tmuxp, the configuration is written in YAML and is similar to the one from Tmuxinator. Smug deals smoothly with my first window pane display configuration, but it took me a couple of minutes to realize a particular behavior: when defining a window, it automatically creates a pane. In other words, if you set up two panes in a window, you get three pains because specifying a window automatically creates a pane. If you're confused, you're not the only one: I only realized this after playing with different configurations.

Smug will be my Tmux session manager going forward unless something funky happens to it. It works similarly to Tmuxinator, so I'll adapt quickly to it.
