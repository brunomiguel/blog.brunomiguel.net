---
title: "First own package on userrepository.eu"
date: "2019-11-13"
categories: 
  - "geekices"
tags: 
  - "arch-linux"
  - "eolie"
  - "free-software"
  - "gtk"
  - "userrepository-eu"
featuredImage: "/post/first-own-package-on-userrepository-eu/images/arch-linux.jpg"
---

Until now, [userrepository.eu](https://userrepository.eu) only used software from _AUR._ Today, to get me distracted from the flu and a respiratory infection I got a few days ago, I've finally created my first package for _Arch Linux_ on my repository. It's for a _GTK_ web browser named [_Eoli_](https://gitlab.gnome.org/World/eolie/) and it builds from the master _git_ branch.

Here's the _PKGBUILD_ at the time of writing:

\# Maintainer: Bruno Miguel <omitted>
​
pkgname=eolie-git
\_gitname=eolie
pkgver=da1899ff
pkgrel=1
pkgdesc="Simple GTK web browser for GNOME"
arch=('x86\_64')
url="https://wiki.gnome.org/Apps/Eolie"
license=('GPL3')
depends=('gtkspell3' 'python-cairo' 'python-dateutil' 'python-gobject' 'webkit2gtk')
makedepends=('git' 'gobject-introspection' 'meson')
optdepends=('python-beautifulsoup4: Import html bookmarks'
            'python-crypto: Firefox Sync support'
            'python-fxa: Firefox Sync support'
            'python-pyopenssl: Show SSL certificates'
            'python-requests-hawk: Firefox Sync support')
source=("git+https://gitlab.gnome.org/World/eolie.git")
sha256sums=('SKIP')
​
pkgver() {
    cd "${\_gitname}"
    ( set -o pipefail
        git describe --long 2>/dev/null | sed 's/\\(\[^-\]\*-g\\)/r\\1/;s/-/./g' ||
        printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
    )
}
​
build() {
    arch-meson "${\_gitname}" build
    ninja -C build
}
​
package() {
    DESTDIR="$pkgdir" meson install -C build
}
​

Every time there's a new commit, it will grab that source and build it. This means you might get a less than stable browser, but also that you'll always get the latest source.

Happy free _softwareing_! :)
