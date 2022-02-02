---
title: "Bash: how-to improve history manipulation"
date: "2018-08-10"
categories: 
  - "geekices"
tags: 
  - "bashrc"
  - "bash"
  - "bash-it"
  - "history"
  - "tips"
  - "tools"
---

![](https://i0.wp.com/blog.brunomiguel.net/wp-content/uploads/2018/08/bash.png?fit=1361%2C691)

By default, _up_ and _down_ keys allow you to navigate your _bash_ history. Another option is the _history_ built-in command and _bash expansions_ (ex.: _!2_ runs the second command, oldest to newest, from your bash history).

There are also tools, like _[bash-it](https://github.com/Bash-it/bash-it/)_, that allow for better history manipulation, but this also adds a lot of other stuff, so it might make your _.bashrc_ load slower. It will make your _bash_ look good as hell too.  

Another option for an awesome way to access your _bash_ history is the following snippet, based on _bash-it_'s history plugin:

```
if [ -t 1 ]
then
    bind '"\e[A": history-search-backward'
    bind '"\e[B": history-search-forward'
fi
```

With this, you only need to write part of a command, press the _up_ arrow and it will complete it with the commands in bash history file that match to what you've written.  

I've add it to the end of my _.bashrc_. Together with bash completion, it improves my workflow by a lot.
