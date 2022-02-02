---
title: "Things to do after installing Fedora"
date: "2018-10-07"
categories: 
  - "geekices"
---

WARNING

Third-party repositories will be enabled and it was only tested on _Fedora 28_. This could have an impact on your system ranging from none to destroying all cat videos on the internet. You have been warned.

### Disable annoying _AMD iommu_ warnings on boot

##### Only for some _AMD CPUs_, like mine, an _AMD A9-9420_  

Edit the _/etc/default/grub_ file and append the following to the _GRUB\_CMDLINE\_LINUX_ line:  

```
iommu=soft amd_iommu=off
```

Full example:

```
GRUB_CMDLINE_LINUX="resume=/dev/mapper/fedora_localhost--live-swap rd.lvm.lv=fedora_localhost-live/root rd.lvm.lv=fedora_localhost-live/swap rhgb quiet iommu=soft amd_iommu=off"
```

Finally, generate the new _GRUB_ configuration to take effect on your next reboot and any kernel update thereafter:

```
sudo grub2-mkconfig -o /boot/efi/EFI/fedora/grub.cfg
```

### Enable _Negativo17_ multimedia repository

##### _Negativo17 has more repositories. You can use them to install Steam, Spotify and more apps. Check their [website](https://negativo17.org/) for more info._

This repositories contains codecs and multimedia software (HandBrake and Blender with CUDA support, for example). A must have.

```
sudo dnf config-manager --add-repo=https://negativo17.org/repos/fedora-multimedia.repo -y
```

### Enable third-party repositories "supported" by Fedora

Refer to the [Fedora Wiki](https://fedoraproject.org/wiki/Workstation/Third_Party_Software_Repositories) for more info.

### Enable Visual Studio Code repository

```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc

sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
```

### Install all codecs

```
sudo dnf install gstreamer1-{plugin-crystalhd,ffmpeg,plugins-{good,ugly,bad{,-free,-nonfree,-freeworld,-extras}{,-extras}}} libmpg123 lame-libs --setopt=strict=0 -y
```

### Apps to install with _DNF_

##### _Needs Negativo17 repos enabled (not only the multimedia one)_  

```
sudo dnf install -y snapd gnome-tweaks dconf-editor mpv gnome-mpv vlc dnfdragora gimp gimpfx-foundry gimp-luminosity-masks gimp-fourier-plugin gimp-focusblur-plugin gmic gmic-gimp inkscape flameshot vokoscreen kodi jpegoptim optipng micro steam qemu-system-x86 youtube-dl mplayer qbittorrent spotify steam pycharm-community pycharm-community-plugins code
```

### Apps to install with _Flatpak_

##### First, enable _flathub_ repo for _Flatpak_

```
sudo flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

##### Then install the apps

```
sudo flatpak install flathub io.github.wereturtle.ghostwrhiter com.github.marktext.marktext io.github.Pithos
```

### Blacklist _radeon_ driver

For some reason, the system completely freezes randomly if I don't blacklist the radeon _driver_. Maybe it interferes with the _amdgpu_ driver that is needed by my _GPUs_ or maybe it's something related to [_Prime_](https://wiki.archlinux.org/index.php/PRIME), but this are just guesses.

```
echo 'blacklist radeon' | sudo tee --append /etc/modules.d/blacklist.conf
```

### (Optional) Install minimal _Plasma Desktop Environment_

```
sudo dnf install @critical-path-kde plasma-workspace plasma-workspace-wayland kde-settings kde-settings-plasma kde-settings-pulseaudio plasma-nm plasma-nm-openvpn plasma-nm-ssh plasma-applet-redshift-control plasma-browser-integration kde-l10n-pt kde-gtk-config dolphin konsole gwenview plasma-workspace kate-plugins kate konsole5 kde-gtk-config ksysguard -y
```

Thanks, [/u/jflory7](https://www.reddit.com/user/jflory7), for the tips to improve this "guide".
