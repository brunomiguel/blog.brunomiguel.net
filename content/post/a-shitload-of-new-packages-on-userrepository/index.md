---
title: "A shitload of new packages on userrepository"
date: "2021-03-03"
categories: 
  - "geekices"
tags: 
  - "arch-linux"
  - "endeavouros"
  - "manjaro"
  - "packages"
  - "userrepository"
  - "userrepository-eu"
---

Since the 24th of January, the date of the last blog post, I've added a shitload of new packages to [userrepository.eu](https://userrepository.eu). Some highlights are _sonobus_, _media-downloader-git_, _baru_, _dotgit_, _timeshift_, _filmulator_ and _tramp_.

Expect more packages, as I'm adding new ones frequently. The focus on new packages will probably be scientific tools and maybe a kernel. With that, I'll probably have to increase the full build frequency from 8h to at least 9 hours.

Below is the diff (`git log -p --after="2021-01-24" | grep "+\[submodule" -A2`) from 24/01/2021 up to today, for your diff p0rn pleasure:

+\[submodule "pkgbuild/sonobus"\]
+       path = pkgbuild/sonobus
+       url = https://aur.archlinux.org/sonobus
+\[submodule "pkgbuild/openfortigui"\]
+       path = pkgbuild/openfortigui
+       url = https://aur.archlinux.org/openfortigui
+\[submodule "pkgbuild/blue"\]
+       path = pkgbuild/blue
+       url = https://aur.archlinux.org/blue
+\[submodule "pkgbuild/metar"\]
+       path = pkgbuild/metar
+       url = https://aur.archlinux.org/metar
+\[submodule "pkgbuild/baru"\]
+       path = pkgbuild/baru
+       url = https://aur.archlinux.org/baru
+\[submodule "pkgbuild/media-downloader-git"\]
+       path = pkgbuild/media-downloader-git
+       url = https://aur.archlinux.org/media-downloader-git
+\[submodule "pkgbuild/athens-git"\]
+       path = pkgbuild/athens-git
+       url = https://aur.archlinux.org/athens-git
+\[submodule "pkgbuild/novelwriter-git"\]
+       path = pkgbuild/novelwriter-git
+       url = https://aur.archlinux.org/novelwriter-git
+\[submodule "pkgbuild/gvolwheel"\]
+       path = pkgbuild/gvolwheel
+       url = https://aur.archlinux.org/gvolwheel
+\[submodule "pkgbuild/gomu"\]
+       path = pkgbuild/gomu
+       url = https://aur.archlinux.org/gomu
+\[submodule "pkgbuild/gphotos-uploader-cli"\]
+       path = pkgbuild/gphotos-uploader-cli
+       url = https://aur.archlinux.org/gphotos-uploader-cli
+\[submodule "pkgbuild/tunnelto"\]
+       path = pkgbuild/tunnelto
+       url = https://aur.archlinux.org/tunnelto
+\[submodule "pkgbuild/pacom"\]
+       path = pkgbuild/pacom
+       url = https://aur.archlinux.org/pacom
+\[submodule "pkgbuild/git-machete"\]
+       path = pkgbuild/git-machete
+       url = https://aur.archlinux.org/git-machete
+\[submodule "pkgbuild/dotgit"\]
+       path = pkgbuild/dotgit
+       url = https://aur.archlinux.org/dotgit
+\[submodule "pkgbuild/reddio-git"\]
+       path = pkgbuild/reddio-git
+       url = https://aur.archlinux.org/reddio-git
+\[submodule "pkgbuild/tarry-git"\]
+       path = pkgbuild/tarry-git
+       url = https://aur.archlinux.org/tarry-git
+\[submodule "pkgbuild/opensurge"\]
+       path = pkgbuild/opensurge
+       url = https://aur.archlinux.org/opensurge
+\[submodule "pkgbuild/lightly-qt"\]
+       path = pkgbuild/lightly-qt
+       url = https://aur.archlinux.org/lightly-qt
+\[submodule "pkgbuild/rudo"\]
+       path = pkgbuild/rudo
+       url = https://aur.archlinux.org/rudo
+\[submodule "pkgbuild/python-pulsectl"\]
+       path = pkgbuild/python-pulsectl
+       url = https://aur.archlinux.org/python-pulsectl
+\[submodule "pkgbuild/teaiso"\]
+       path = pkgbuild/teaiso
+       url = https://aur.archlinux.org/teaiso
+\[submodule "pkgbuild/gtk-theme-arc-gruvbox-git"\]
+       path = pkgbuild/gtk-theme-arc-gruvbox-git
+       url = https://aur.archlinux.org/gtk-theme-arc-gruvbox-git
+\[submodule "pkgbuild/limine"\]
+       path = pkgbuild/limine
+       url = https://aur.archlinux.org/limine
+\[submodule "pkgbuild/kaidan"\]
+       path = pkgbuild/kaidan
+       url = https://aur.archlinux.org/kaidan
+\[submodule "pkgbuild/vt-cli"\]
+       path = pkgbuild/vt-cli
+       url = https://aur.archlinux.org/vt-cli
+\[submodule "pkgbuild/xwinwrap-git"\]
+       path = pkgbuild/xwinwrap-git
+       url = https://aur.archlinux.org/xwinwrap-git
+\[submodule "pkgbuild/httpdirfs"\]
+       path = pkgbuild/httpdirfs
+       url = https://aur.archlinux.org/httpdirfs
+\[submodule "pkgbuild/go-tuner-git"\]
+       path = pkgbuild/go-tuner-git
+       url = https://aur.archlinux.org/go-tuner-git
+\[submodule "pkgbuild/pacroller"\]
+       path = pkgbuild/pacroller
+       url = https://aur.archlinux.org/pacroller
+\[submodule "pkgbuild/plasmasur-dark-kde-theme-git"\]
+       path = pkgbuild/plasmasur-dark-kde-theme-git
+       url = https://aur.archlinux.org/plasmasur-dark-kde-theme-git
+\[submodule "pkgbuild/whitesur-kde-theme-git"\]
+       path = pkgbuild/whitesur-kde-theme-git
+       url = https://aur.archlinux.org/whitesur-kde-theme-git
+\[submodule "pkgbuild/readability-cli"\]
+       path = pkgbuild/readability-cli
+       url = https://aur.archlinux.org/readability-cli
+\[submodule "pkgbuild/flipclock"\]
+       path = pkgbuild/flipclock
+       url = https://aur.archlinux.org/flipclock
+\[submodule "pkgbuild/uivonim-git"\]
+       path = pkgbuild/uivonim-git
+       url = https://aur.archlinux.org/uivonim-git
+\[submodule "pkgbuild/tramp"\]
+       path = pkgbuild/tramp
+       url = https://aur.archlinux.org/tramp
+\[submodule "pkgbuild/emacs-yaml-mode"\]
+       path = pkgbuild/emacs-yaml-mode
+       url = https://aur.archlinux.org/emacs-yaml-mode
+\[submodule "pkgbuild/cask"\]
+       path = pkgbuild/cask
+       url = https://aur.archlinux.org/cask
+\[submodule "pkgbuild/nord-emacs"\]
+       path = pkgbuild/nord-emacs
+       url = https://aur.archlinux.org/nord-emacs
+\[submodule "pkgbuild/emms"\]
+       path = pkgbuild/emms
+       url = https://aur.archlinux.org/emms
+\[submodule "pkgbuild/qemacs"\]
+       path = pkgbuild/qemacs
+       url = https://aur.archlinux.org/qemacs
+\[submodule "pkgbuild/elfeed"\]
+       path = pkgbuild/elfeed
+       url = https://aur.archlinux.org/elfeed
+\[submodule "pkgbuild/emacs-libvterm-git"\]
+       path = pkgbuild/emacs-libvterm-git
+       url = https://aur.archlinux.org/emacs-libvterm-git
+\[submodule "pkgbuild/emacs-projectile"\]
+       path = pkgbuild/emacs-projectile
+       url = https://aur.archlinux.org/emacs-projectile
+\[submodule "pkgbuild/emacs-smart-mode-line"\]
+       path = pkgbuild/emacs-smart-mode-line
+       url = https://aur.archlinux.org/emacs-smart-mode-line
+\[submodule "pkgbuild/emacs-pos-tip-git"\]
+       path = pkgbuild/emacs-pos-tip-git
+       url = https://aur.archlinux.org/emacs-pos-tip-git
+\[submodule "pkgbuild/emacs-magit"\]
+       path = pkgbuild/emacs-magit
+       url = https://aur.archlinux.org/emacs-magit
+\[submodule "pkgbuild/oh-my-zsh-git"\]
+       path = pkgbuild/oh-my-zsh-git
+       url = https://aur.archlinux.org/oh-my-zsh-git
+\[submodule "pkgbuild/zsh-theme-powerlevel10k-git"\]
+       path = pkgbuild/zsh-theme-powerlevel10k-git
+       url = https://aur.archlinux.org/zsh-theme-powerlevel10k-git
+\[submodule "pkgbuild/ttf-meslo-nerd-font-powerlevel10k"\]
+       path = pkgbuild/ttf-meslo-nerd-font-powerlevel10k
+       url = https://aur.archlinux.org/ttf-meslo-nerd-font-powerlevel10k
+\[submodule "pkgbuild/timeshift"\]
+       path = pkgbuild/timeshift
+       url = https://aur.archlinux.org/timeshift
+\[submodule "pkgbuild/timeshift-autosnap"\]
+       path = pkgbuild/timeshift-autosnap
+       url = https://aur.archlinux.org/timeshift-autosnap
+\[submodule "pkgbuild/dimport"\]
+       path = pkgbuild/dimport
+       url = https://aur.archlinux.org/dimport
+\[submodule "pkgbuild/crema"\]
+       path = pkgbuild/crema
+       url = https://aur.archlinux.org/crema
+\[submodule "pkgbuild/lensfun-git"\]
+       path = pkgbuild/lensfun-git
+       url = https://aur.archlinux.org/lensfun-git
+\[submodule "pkgbuild/librtprocess"\]
+       path = pkgbuild/librtprocess
+       url = https://aur.archlinux.org/librtprocess
+\[submodule "pkgbuild/filmulator"\]
+       path = pkgbuild/filmulator
+       url = https://aur.archlinux.org/filmulator
+\[submodule "pkgbuild/rooster"\]
+       path = pkgbuild/rooster
+       url = https://aur.archlinux.org/rooster
+\[submodule "pkgbuild/heroic-games-launcher-bin"\]
+       path = pkgbuild/heroic-games-launcher-bin
+       url = https://aur.archlinux.org/heroic-games-launcher-bin
+\[submodule "pkgbuild/keep"\]
+       path = pkgbuild/keep
+       url = https://aur.archlinux.org/keep
+\[submodule "pkgbuild/python-cachelib"\]
+       path = pkgbuild/python-cachelib
+       url = https://aur.archlinux.org/python-cachelib
+\[submodule "pkgbuild/ipscan"\]
+       path = pkgbuild/ipscan
+       url = https://aur.archlinux.org/ipscan
+\[submodule "pkgbuild/otoclone"\]
+       path = pkgbuild/otoclone
+       url = https://aur.archlinux.org/otoclone
+\[submodule "pkgbuild/sfwbar"\]
+       path = pkgbuild/sfwbar
+       url = https://aur.archlinux.org/sfwbar
+\[submodule "pkgbuild/mediad"\]
+       path = pkgbuild/mediad
+       url = https://aur.archlinux.org/mediad
+\[submodule "pkgbuild/novelwriter"\]
+       path = pkgbuild/novelwriter
+       url = https://aur.archlinux.org/novelwriter
+\[submodule "pkgbuild/aur-update"\]
+       path = pkgbuild/aur-update
+       url = https://aur.archlinux.org/aur-update
