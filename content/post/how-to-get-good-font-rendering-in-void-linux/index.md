---
title: "How to get good font rendering in Void Linux"
date: "2018-07-24"
categories: 
  - "geekices"
tags: 
  - "font-rendering"
  - "howto"
  - "tips"
  - "truetype"
  - "void-linux"
---

This post lacks an example image because I've recovered it from a backup (with only text and no image) and I'm not using Void Linux at the moment. If you follow this guide and decide to share an image, I'll gladly use it here and give you credit.

This guide assumes you are using [Void Linux](http://voidlinux.eu/) (you can probably replicate it in other distributions; just check the paths), have _Freetype_ installed and using some sort of _Window Manager_ or _Desktop Environment_. If you don't, _sudo xi_ them. After that, fire up a terminal and create a symbolic link, from the following files in _/usr/share/fontconfig/conf.avail/,_ to _/etc/fonts/conf.d_:

- 10-hinting-slight.conf
- 10-scale-bitmap-fonts.conf
- 10-sub-pixel-rgb.conf
- 11-lcdfilter-default.conf
- 20-unhint-small-vera.conf
- 21-cantarell-hinting.conf
- 30-metric-aliases.conf
- 30-urw-aliases.conf
- 31-cantarell.conf
- 40-nonlatin.conf
- 42-luxi-mono.conf
- 45-latin.conf
- 49-sansserif.conf
- 50-user.conf
- 51-local.conf
- 57-dejavu-sans-mono.conf
- 57-dejavu-sans.conf
- 57-dejavu-serif.conf
- 60-latin.conf
- 65-fonts-persian.conf
- 65-nonlatin.conf
- 69-unifont.conf
- 70-no-bitmaps.conf
- 80-delicious.conf
- 90-synthetic.conf  
    

I've also symlinked these files (again, from /usr/share/fontconfig/conf.avail/) to ~/.config/fontconfig/conf.d/:

- 10-hinting-slight.conf
- 10-sub-pixel-rgb.conf
- 50-user.conf (using it to default Helvetica, Arial and Verdana to Clear Sans)
- 60-latin.conf
- 70-no-bitmaps.conf

My _.Xresources_ file:

Xft.autohint: 1  
Xft.antialias: 1  
Xft.hinting: true  
Xft.hintstyle: hintslight  
Xft.rgba: rgb  
Xft.lcdfilter: lcddefault

Also, I''ve created the _/etc/profile.d/freetype2.sh_ file with this content:

\# Subpixel hinting mode can be chosen by setting the right TrueType interpreter  
\# version. The available settings are:  
#  
\# truetype:interpreter-version=35 # Classic mode (default in 2.6)  
\# truetype:interpreter-version=38 # Infinality mode  
\# truetype:interpreter-version=40 # Minimal mode (default in 2.7)  
#  
\# There are more properties that can be set, separated by whitespace. Please  
\# refer to the FreeType documentation for details.  
  
\# Uncomment and configure below  
  
export FREETYPE\_PROPERTIES="truetype:interpreter-version=38"

Have an happy GNU Experience :)
