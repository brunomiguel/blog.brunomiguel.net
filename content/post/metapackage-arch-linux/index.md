---
title: "Metapackage for a personal installation of Arch Linux and Arch-based distributions"
date: "2019-10-17"
categories: 
  - "geekices"
tags: 
  - "arch"
  - "arch-linux"
  - "git"
  - "pkgbuild"
---

I've been using Arch or Arch-based distributions for over a year now. In this time testing a few of them, I've always lacked a simple and logical way of installing the same "essential" software. To tackle this, I've created a metapackage with all this software and this is what I've got so far:

\# Maintainer: Bruno Miguel <https://twitter.com/brunomiguel>

pkgname='bruno-essentials'
pkgdesc="A metapackage for some packages I find essential. Requires userrepository.eu repo"
pkgver='0.0.2'
pkgrel=2

url='https://github.com/brunomiguel/base-bruno'
arch=('any')
license=('GPL3')

depends=(
    # base
	'tmux' 'rxvt-unicode' 'urxvt-tabbedex' 'gotop-git' 'pakku' 'inxi' 'brightnessctl-git' 'broot' 'ranger' 'htop' 'git' 'scat' 'scaleway-cli' 'reflector' 'qjournalctl' 'openvpn' 'openssh' 'cpupower' 'bash-completion'
	
	# editors
	'vim' 'micro' 'marktext-bin' 'notable-bin' 'quilter'
	
	# cli utilities
	'terminal-markdown-viewer' 'redshift' 'youtube-dl' 'unrar' 'unzip' 'spicetify-cli' 'pfetch-git' 'profile-cleaner' 'cups'
	
	# multimedia
	'acestream-launcher' 'gimp' 'gimp-plugin-gmic' 'gimp-refocus' 'spotify' 'pavucontrol' 'vlc' 'curseradio-git' 'mpv-acestream' 'jpegoptim' 'optipng' 'acestream-engine' 'trimage' 'pngzop'
	
	# fonts
	'ttf-fira-go' 'ttf-fira-mono-ibx' 'ttf-league-mono' 'ttf-inter-ui' 'interui-otf'
	
	# plasma (somewhat minimal)
	'kvantum-qt5' 'kvantum-theme-materia' 'plasma-desktop' 'konsole' 'ark' 'gwenview' 'kde-gtk-config' 'kdeplasma-addons' 'ksysguard' 'powerdevil' 'user-manager' 'spectacle' 'kio-extras' 'kipi-plugins' 'kcalc' 'kcron' 'okular' 'dolphin' 'dolphin-plugins' 'sweeper' 'kdeconnect' 'oxygen' 'plasma-nm' 'plasma-pa' 'plasma5-applets-redshift-control' 'konsole' 'okular' 'kate' 'print-manager'
	
	# browsers
	'brave-dev-bin' 'firefox' 'firefox-i18n-pt-pt' 'falkon-git' 'librewolf-bin'
	
	# desktop utilities
	'roxterm' 'flameshot' 'libreoffice-fresh' 'filelight'
	
	# security
	'bitwarden-bin'
	
	# i3
	'i3-gaps-rounded-git' 'polybar' 'rofi' 'compton-tryone-git' 'nitrogen'
	
	# themes and icons
	'korla-icon-theme' 'arc-icon-theme' 'boston-icon-theme-git'	
	
	#gamimg
	'steam' 'gamehub'
	
	
)

You can keep up with the changes on [Github](https://github.com/brunomiguel/base-bruno).
