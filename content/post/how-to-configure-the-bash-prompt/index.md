---
title: "How-to customize the Bash prompt"
date: "2018-09-21"
categories: 
  - "geekices"
tags: 
  - "bash"
  - "debian"
  - "git"
  - "promp"
  - "tips"
---

In order to adapt a bit more my _Debian Stable_ installation to my workflow, I've been tweaking the _bash_ prompt. Simplicity and small line width are key here, because I often have _tmux_ running with several panes in the same window and small panes with large one-liner prompts suck a lot! Everything feels crammed and hard to read. Just take a look at the image below to get an idea.  

![crammed bash prompt](https://i2.wp.com/blog.brunomiguel.net/wp-content/uploads/2018/09/crammed.png?fit=1366%2C734)

After running a few commands in each pane with this prompt configuration, everything gets really crowded and confuse. For sanity safeguarding reasons and workflow improvement, the only thing to do is customize the prompt.

The _Debian Stable_ bash prompt, shown on the image above, default value is:

if \[ "$color\_prompt" = yes \]; then
    PS1='${debian\_chroot:+($debian\_chroot)}\\\[\\033\[01;32m\\\]\\u@\\h\\\[\\033\[00m\\\]:\\\[\\033\[01;34m\\\]\\w\\\[\\033\[00m\\\]\\$ '
else
    PS1='${debian\_chroot:+($debian\_chroot)}\\u@\\h:\\w\\$ '
fi
unset color\_prompt force\_color\_prompt

To make it more useful, I changed the second line to this:

PS1="\[\\033\[00;32m\]\\u@\\h\[\\033\[00m\]:\\w\[\\033\[00m\]\\n└─ \[$(tput bold)\]\\$(\_\_git\_ps1 '\[%s\] ')\\$: \[$(tput sgr0)\]"

All put together:

if \[ "$color\_prompt" = yes \]; then
		PS1="\\\[\\033\[00;32m\\\]\\u@\\h\\\[\\033\[00m\\\]:\\w\\\[\\033\[00m\\\]\\n└─ \\\[$(tput bold)\\\]\\$(\_\_git\_ps1 '\[%s\] ')\\$: \\\[$(tput sgr0)\\\]"
else
    PS1='${debian\_chroot:+($debian\_chroot)}\\u@\\h:\\w\\$ '
fi
unset color\_prompt force\_color\_prompt

And this is the result:

![readable bash prompt](https://i2.wp.com/blog.brunomiguel.net/wp-content/uploads/2018/09/readable.png?fit=1366%2C735)

Not only I get a more readable prompt (and with "more room to breathe", if you may), but I get the name of the current branch if I'm in a _Git_ repository folder. This is a convenient feature to have if you work with this version control system.

There are a lot more ways one can configure the prompt. Both [_How-To Geek_](https://www.howtogeek.com/307701/how-to-customize-and-colorize-your-bash-prompt/) and [_Boolean World_](https://www.booleanworld.com/customizing-coloring-bash-prompt/) websites have nice introductory guides to get you started. The _Arch Linux_ [wiki entry](https://wiki.archlinux.org/index.php/Bash/Prompt_customization) about this is also a good read. Oh, and [_RTFM_](http://tldp.org/HOWTO/Bash-Prompt-HOWTO/bash-prompt-escape-sequences.html) (Read The ... Fine ... Manual).
