---
title: "Testing Neovim for my writing needs"
summary: "I've started to use Neovim for writing text but also for putting up the occasional script"
description: "I've started to use Neovim for writing text but also for putting up the occasional script"
date: 2023-02-01
categories:
    - "geekices"
tags:
    - "neovim"
    - "cli"
    - "command line"
    - "tools"
cover:
    image: "post/neovim/images/neovim.webp"
    alt: "Screenshot for my Neovim setup"
---

Most of my writing has been done on Typora, a multi-platform proprietary markdown editor. The software lets you live-preview as you type, supports themes, allows exporting markdown files to a bunch of other formats, and looks very good overall. My only issue with it is being proprietary. It may be just one issue, but it's a big one.

For a while, I've looked for alternatives. I tried Ghostwriter, even gave Logseq a short for this (it's a fantastic piece of software, but it leaves a bit to desire when writing blog posts with frontmatter information on them), and a handful of other tools I can't remember as I type this post. None of them quite offer what I liked about Typora.

Some time passed, and tonight, after another pain-induced insomnia, I decided to try Neovim. I've been meaning to do it for a while. What better time than when I can't sleep because I'm in too much pain and my brain is completely messed up because of that?! "It was the best of times, it was the worst of times, it was [...]" another night with too much pain and a need to pass the time and not give in to despair.

Two main things got my attention in Neovim (and VIM, too): the amount of customization that can be done and the beautiful configurations I've seen online. All of this is easier than with Emacs, a tool I tried to use in the past but failed because it has a big learning curve. By the way, I'm not implying this is an issue with the software; I know this is an issue with me, my habits, and my knowledge.

Between one and two in the morning (three to four hours before starting to write this blog post), I started hacking an `init.vim` config, setting up options, plugins, keybindings, etc. About two hours later, I began rewriting my configuration to Lua because of a single plugin, Glow. True story! I'll stick with the Lua configuration because it is the road Neovim is heading.

As the configuration grew, I switched from a monolithic configuration to a modular one. The Neovim options are in `init.lua`, and all the rest (keybindings, plugins, and custom modes) gets their own config file under `$XDG_CONFIG_HOME/.nvim/lua` to keep things sane for me. Other Neovim and VIM users appear to do it this way too.

I'll stick with Neovim in the coming weeks to see if I can adapt to it. I've been using it to edit configuration files for weeks, which will help with the transition and adaptation period.

The trialing period will also serve to learn and get used to more default Neovim keybindings and commands, like `dd` for deleting a line in normal mode or `3dd` for deleting three lines. I guess `:help vimtutor` will be my friend during this period.

<small>_The screenshot was taken by me and is under the [CC0
License](https://creativecommons.org/share-your-work/public-domain/cc0/)._</small>
