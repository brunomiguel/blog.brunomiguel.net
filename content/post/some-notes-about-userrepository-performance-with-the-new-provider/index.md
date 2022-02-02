---
title: "Some notes about userrepository performance with the new provider"
date: "2020-06-04"
categories: 
  - "geekices"
tags: 
  - "userrepository-eu"
featuredImage: "/post/some-notes-about-userrepository-performance-with-the-new-provider/images/race.jpg"
---

In the previous post, I wrote about how I changed the virtual machine provider from _Scaleway_ to _Hetzner_. In the days following the transition, I timed how much it took to build all the packages and sync them to the webserver, so I could compare the new provider with the previous one.

The specs are very similar: 4 _vCPUs_ and 8GB of _RAM_. There is one difference, however: with _Scaleway_, the _vCPUs_ were some _Intel_ low-end ones (although they've upgraded to _AMD EPYC_ very recently) and with _Hetzer_ they are _AMD EPYC_. And what a difference this makes.

Previously, 250 and something packages took almost 5 hours to complete the build and sync them to the webserver. Now, it takes around 4 hours and 12 minutes to build and sync 328 packages. That's a huge difference.

I've only been using _Hetzer_ for _[userrepository](https://userrepository.eu)_ for about a week, but so far it feels like an improvement. But I've yet to test the network performance.
