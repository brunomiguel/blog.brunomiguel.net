---
title: "Smug, a tmux session manager"
summary: "Smug helps you manage different tmux sessions with different windows and panes"
description: "Smug helps you manage different tmux sessions with different windows and panes"
date: 2023-04-24
categories:
  - "geekices"
tags:
  - "tmux"
  - "smug"
  - "session"
  - "terminal"
cover:
  image: "post/smug-tmux-session-manager/images/smug.webp"
  alt: "Screenshot of my main smug config"
---

Tmux is a terminal multiplexer. If you've clicked on this post, you are likely to know this. As powerful and useful as it is, this tool doesn't include a way to configure how many windows and panes you want to create when you run it and which applications to start on which panes.

Session managers fill this gap. They allow you to create templates where you specify how many windows and panes you want when you start a Tmux session. If you have to ssh into different machines or want to spin different setups for various purposes, you see the value in this type of tool.

One such tool is [Smug](https://github.com/ivaaaan/smug). The tool describes itself as follows: _"Session manager and task runner for Tmux. Start your development environment within one command."_

The configuration files for Smug are written in YAML. In them, you can:
- create and name as many windows and panes as you want
- define each window's layout
- run commands on some panes but not on others
- define environmental variables
- run commands before a session starts and when it ends

**One particularity about Smug: defining a window in a configuration file automatically creates a pane on that window.** Let's say you want a window with two panes. In this example, you would only need to specify one pane because Smug assumes you're already starting the first pane when creating a window.

Here is an example of that behavior below:

```yaml
windows:
  - name: first-window #this also creates the first pane on this window
    layout: even-horizontal
    panes: #now we only need to create the second pane
      - commands:
            - clear
```

There's no need to specify the clear command. I do it because, in my opinion, it provides a visual cue for better content hierarchy.

I recommend checking the tool git repository and reading the documentation for all the configuration options. But if you want to look at a simple configuration, you can check my main local template below.

```yaml
session: default

root: $HOME

windows:
  - name: principal
    layout: main-vertical
    panes:
      - commands:
          - clear
      - commands:
          - watch -n 2 "sensors | grep -E 'Package|Core|Composite|temp1'"

  - name: música
    commands:
      - pyradio
    layout: even-horizontal
    panes:
      - commands:
          - pipe-viewer --best --player=mpv -n
```

There are other Tmux session managers out there, and you should try them out to see which one works better for you. Smug is the one I found to better fit my needs.
