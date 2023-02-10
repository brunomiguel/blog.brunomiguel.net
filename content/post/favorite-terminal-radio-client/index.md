---
title: "My favorite terminal online radio client"
summary: "Curseradio has been my favorite terminal online radio client for several years. Having
been five years without receiving updates, I have to find a new software to replace it."
description: "Curseradio has been my favorite terminal online radio client for several years. Having been five years without receiving updates, I have to find a new software to replace it."
date: 2023-02-10
categories:
  - "geekices"
tags:
  - "radio"
  - "client"
  - "terminal"
  - "curseradio"
  - "pyradio"
  - "ctune"
cover:
  image: "post/favorite-terminal-radio-client/images/ctune-and-pyradio.webp"
  alt: "cTune and PyRadio running side-by-side under Tmux"
---

Most of the music I listen to is from either Spotify or Youtube. Both have enormous music libraries and music that I like, so it's only natural that I use them the most. Yet, I want to listen to online radio, which I've been doing since the early 2000s. Over this time, I found, lost, and forgot a lot of good radio stations, and I still find them relevant to my music consumption.

During the last six or seven years, give or take, my favorite online radio client for the terminal has been [curseradio](https://github.com/chronitis/curseradio). The application runs on the terminal and integrates with TuneIn's online directory. It has some issues though: while you have a lot of stations to browse, you can only access them from the listing menu. No search functionality is available, as there are no bookmarking capabilities. This always bugged me a little, even though it was also an opportunity to find other radios and see if I liked them. Silver linings.

What has bothered me the most is curseradio not receiving updates since the 17th of October, 2017. Five years is too long without updates, and the software rot will eventually set in.

[PyRadio](https://github.com/coderholic/pyradio/blob/master/radio-browser.md) is another online radio client I've used occasionally, mainly as a more up-to-date alternative to curseradio. My experience with it has always fallen short of the latter. My two main gripes were no integration with an online radio directory and a weird way of navigating the application. A couple of weeks ago, they finally integrated RadioBrowser to fetch the audio streams and relevant information. Using the application still feels strange, however.

While continuing to scour for a terminal online radio client on my way to Mordor, I stumbled on [cTune](https://github.com/An7ar35/ctune). Like PyRadio, it uses RadioBrowser's `API` to search and get the stream information, and the interface so far feels slightly better. The search modal, which even lets me search by tag and is easier to reach than with PyRadio, makes it a likely alternative to curseradio. PyRadio, on the other hand, let's me sort the results.

Overall, I still prefer curseradio. However, it's time to find a replacement, and either PyRadio or cTune will replace it. Time to test them for a few weeks each.
