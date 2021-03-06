---
title: "Some changes to userrepository"
date: "2021-01-24"
categories: 
  - "geekices"
tags: 
  - "archlinux"
  - "git"
  - "userrepository"
  - "userrepository-eu"
featuredImage: "/post/some-changes-to-userrepository/images/laptop-2588606_1920.jpg"
---

Hello, folks. It has been a [while](https://blog.brunomiguel.net/geekices/updates-on-userrepository-and-jarvis/) since I last wrote about my AUR-based Arch Linux [repository](https://userrepository.eu). To be precise, four months and twelve days.

A lot has happened since then. One of the main changes was the removal of several packages no longer present in AUR or really outdated. Some examples are peafox, marp and gimp-dbp.

Another important change was the addition of several new packages, as usual. If I find it may be useful for someone, I add it.

Also, I created three metapackages for a minimal — and opinionated — Plasma Desktop, GNOME and XFCE installation. You can install them by choosing one of the following:

- gnome-minimal
- plasma-minimal
- xfce-minimal

More, for Mate, Cinnamon and other desktop environments or window managers might be released soon.

Sadly still, no kernels, although I would love to add one. I have jarvis — the build bot — doing a full build every 8 hours, so adding a kernel will likely force me to increase this time span. As of now, I would like to avoid it, but that might change in the future. Let's see how it goes.

If you want to take a detailed look at the changes, you can see the last 10 ones below:

```
commit 9704c81ad0c7c09a93f42d1c62489c3cf2637fbc
Author: Bruno Miguel <omitted>
Date:   Sun Jan 24 03:11:14 2021 +0000

    new packages; submodules updates

diff --git a/.gitmodules b/.gitmodules
index 1b59c51..49f1149 100644
--- a/.gitmodules
+++ b/.gitmodules
@@ -1768,3 +1768,21 @@
 \[submodule "pkgbuild/pilgo"\]
 	path = pkgbuild/pilgo
 	url = https://aur.archlinux.org/pilgo
+\[submodule "pkgbuild/ipscan"\]
+	path = pkgbuild/ipscan
+	url = https://aur.archlinux.org/ipscan
+\[submodule "pkgbuild/otoclone"\]
+	path = pkgbuild/otoclone
+	url = https://aur.archlinux.org/otoclone
+\[submodule "pkgbuild/sfwbar"\]
+	path = pkgbuild/sfwbar
+	url = https://aur.archlinux.org/sfwbar
+\[submodule "pkgbuild/mediad"\]
+	path = pkgbuild/mediad
+	url = https://aur.archlinux.org/mediad
+\[submodule "pkgbuild/novelwriter"\]
+	path = pkgbuild/novelwriter
+	url = https://aur.archlinux.org/novelwriter
+\[submodule "pkgbuild/aur-update"\]
+	path = pkgbuild/aur-update
+	url = https://aur.archlinux.org/aur-update
diff --git a/pkgbuild/android-messages-desktop-bin b/pkgbuild/android-messages-desktop-bin
index 526eee3..2d9433d 160000
--- a/pkgbuild/android-messages-desktop-bin
+++ b/pkgbuild/android-messages-desktop-bin
@@ -1 +1 @@
-Subproject commit 526eee3e86581dc2c5c35d03f5819e4d0c4eceda
+Subproject commit 2d9433de0a9c3723e12f24d6f62b660ef022c025
diff --git a/pkgbuild/aur-update b/pkgbuild/aur-update
new file mode 160000
index 0000000..7a6ac3e
--- /dev/null
+++ b/pkgbuild/aur-update
@@ -0,0 +1 @@
+Subproject commit 7a6ac3e2f5f2aaa7840c2e55fe91290f2ad19dc2
diff --git a/pkgbuild/autenticacao-gov-pt b/pkgbuild/autenticacao-gov-pt
index 1d8510f..a4beb0e 160000
--- a/pkgbuild/autenticacao-gov-pt
+++ b/pkgbuild/autenticacao-gov-pt
@@ -1 +1 @@
-Subproject commit 1d8510f74ea2108a36a9105a1e30f2c29a02a9b0
+Subproject commit a4beb0e69fcabd06aa39a4098d19e5a0a2c23977
diff --git a/pkgbuild/blightmud b/pkgbuild/blightmud
index 5928526..d54bca4 160000
--- a/pkgbuild/blightmud
+++ b/pkgbuild/blightmud
@@ -1 +1 @@
-Subproject commit 592852676b8c99092adceb7df582d32d929f490b
+Subproject commit d54bca412cf6fe45d97b066789e54d6f26261cfc
diff --git a/pkgbuild/boostchanger-git b/pkgbuild/boostchanger-git
index 9af0dc7..d2d03a7 160000
--- a/pkgbuild/boostchanger-git
+++ b/pkgbuild/boostchanger-git
@@ -1 +1 @@
-Subproject commit 9af0dc7eee3a84a715435fc5a0069067b714efe2
+Subproject commit d2d03a7b8bece51d25e2fcd855540b46942c3ef5
diff --git a/pkgbuild/bottles-git b/pkgbuild/bottles-git
index 0958ead..267dcf2 160000
--- a/pkgbuild/bottles-git
+++ b/pkgbuild/bottles-git
@@ -1 +1 @@
-Subproject commit 0958eadb44691f08bff29a9a1472489e4687b774
+Subproject commit 267dcf274cbd5757763d5118fb355933f9a57a24
diff --git a/pkgbuild/brave-dev-bin b/pkgbuild/brave-dev-bin
index 7d7cd68..b0606a0 160000
--- a/pkgbuild/brave-dev-bin
+++ b/pkgbuild/brave-dev-bin
@@ -1 +1 @@
-Subproject commit 7d7cd68a8361bbb8329070387ef827c20c930866
+Subproject commit b0606a0c6dc61dbcc51963f63259b61fedba8039
diff --git a/pkgbuild/cagebreak b/pkgbuild/cagebreak
index d67d925..247ded9 160000
--- a/pkgbuild/cagebreak
+++ b/pkgbuild/cagebreak
@@ -1 +1 @@
-Subproject commit d67d9259b0ac2eeec2c23854de341e0908ccd957
+Subproject commit 247ded9c1e501ea9ebf476d383aa3a7ce226cb31
diff --git a/pkgbuild/console\_sudoku b/pkgbuild/console\_sudoku
index f2dc442..e1b3570 160000
--- a/pkgbuild/console\_sudoku
+++ b/pkgbuild/console\_sudoku
@@ -1 +1 @@
-Subproject commit f2dc4425507982d6047183eb815bf30ec8825914
+Subproject commit e1b357047a27a6c753ae41ef04afdb088661b0de
diff --git a/pkgbuild/dimport b/pkgbuild/dimport
index 9f9ed61..5124863 160000
--- a/pkgbuild/dimport
+++ b/pkgbuild/dimport
@@ -1 +1 @@
-Subproject commit 9f9ed61cfb6aeaf8e6a7759980fd95e6fdb826c5
+Subproject commit 51248638338960f0bab96f9de819ea6a35c51d31
diff --git a/pkgbuild/dotter-rs-bin b/pkgbuild/dotter-rs-bin
index d4162be..3fdd5c1 160000
--- a/pkgbuild/dotter-rs-bin
+++ b/pkgbuild/dotter-rs-bin
@@ -1 +1 @@
-Subproject commit d4162be612334f444c29b8cc9818ac812ba62a0d
+Subproject commit 3fdd5c1fcd91eb5cad04b66636466d664428fc94
diff --git a/pkgbuild/dvc b/pkgbuild/dvc
index 04cc5cf..5c6da7c 160000
--- a/pkgbuild/dvc
+++ b/pkgbuild/dvc
@@ -1 +1 @@
-Subproject commit 04cc5cf8b8862caddf1a4d818a2f992f1f20a4fc
+Subproject commit 5c6da7c2fabb2b440647a553d0b2e7358727b9c8
diff --git a/pkgbuild/exiftool b/pkgbuild/exiftool
index e9952fb..eb3cb4e 160000
--- a/pkgbuild/exiftool
+++ b/pkgbuild/exiftool
@@ -1 +1 @@
-Subproject commit e9952fbf26b131b08f7f35bc2fa165ecdeb2b1e4
+Subproject commit eb3cb4e25be59001ae022d676006ca966a1696b4
diff --git a/pkgbuild/f3 b/pkgbuild/f3
index a0b0f7d..bd3bd4b 160000
--- a/pkgbuild/f3
+++ b/pkgbuild/f3
@@ -1 +1 @@
-Subproject commit a0b0f7df66aad50129515d1e8dc1734475d3ca44
+Subproject commit bd3bd4b8c59199fa8235e6ffca9ba67c26646757
diff --git a/pkgbuild/firefox-beta-bin b/pkgbuild/firefox-beta-bin
index 87867e9..a59669c 160000
--- a/pkgbuild/firefox-beta-bin
+++ b/pkgbuild/firefox-beta-bin
@@ -1 +1 @@
-Subproject commit 87867e912df42f5a8fca6b0182615cf75256c9f6
+Subproject commit a59669c3d723616778f4bc8790f6f77231cc9339
diff --git a/pkgbuild/firefox-kde-opensuse-bin b/pkgbuild/firefox-kde-opensuse-bin
index 4d835d6..9c59ece 160000
--- a/pkgbuild/firefox-kde-opensuse-bin
+++ b/pkgbuild/firefox-kde-opensuse-bin
@@ -1 +1 @@
-Subproject commit 4d835d6f4b3adaa76bd9b6a48326769b665cd914
+Subproject commit 9c59eceac601cf479f4e6b1cc65b40f481113fe9
diff --git a/pkgbuild/gaiasky b/pkgbuild/gaiasky
index cb7bcd0..d3c4641 160000
--- a/pkgbuild/gaiasky
+++ b/pkgbuild/gaiasky
@@ -1 +1 @@
-Subproject commit cb7bcd0be81dab92fc656fb94cd5ab396988bc2a
+Subproject commit d3c46413257a7f4f0d43d65706a27333359517da
diff --git a/pkgbuild/gdu b/pkgbuild/gdu
index 119d499..ffc026f 160000
--- a/pkgbuild/gdu
+++ b/pkgbuild/gdu
@@ -1 +1 @@
-Subproject commit 119d499f5600cefb3df6c72769c6f5296a798fec
+Subproject commit ffc026f76d51e3d16d866697dd0f615dc12fb48d
diff --git a/pkgbuild/git-cola b/pkgbuild/git-cola
index f65d845..b5aa449 160000
--- a/pkgbuild/git-cola
+++ b/pkgbuild/git-cola
@@ -1 +1 @@
-Subproject commit f65d845cdd2c186866fcdbe08e21a6cc4a607c77
+Subproject commit b5aa449e4741fa36e66d4f19f4d9b6316ab35f26
diff --git a/pkgbuild/git-delta b/pkgbuild/git-delta
index 821d257..6c80d8c 160000
--- a/pkgbuild/git-delta
+++ b/pkgbuild/git-delta
@@ -1 +1 @@
-Subproject commit 821d257556f9880b6fb1d7f96fb3d231fa4d2e41
+Subproject commit 6c80d8c8b2e27313ddea56e76c6dbfbb72a8909a
diff --git a/pkgbuild/gitleaks b/pkgbuild/gitleaks
index c9356e3..2a24029 160000
--- a/pkgbuild/gitleaks
+++ b/pkgbuild/gitleaks
@@ -1 +1 @@
-Subproject commit c9356e31899acaa34a58515cde8b3392a44a4bae
+Subproject commit 2a24029d02ef551620935c1e7f3b3659be0084dc
diff --git a/pkgbuild/gitui-git b/pkgbuild/gitui-git
index 7cbf09f..7d26997 160000
--- a/pkgbuild/gitui-git
+++ b/pkgbuild/gitui-git
@@ -1 +1 @@
-Subproject commit 7cbf09f4dbeacedcd8b0914b05ee10b40f9075cc
+Subproject commit 7d269976ec63bf02e5149f00a2a07b1395ec4035
diff --git a/pkgbuild/graviton-bin b/pkgbuild/graviton-bin
index 8175fde..3f5c01e 160000
--- a/pkgbuild/graviton-bin
+++ b/pkgbuild/graviton-bin
@@ -1 +1 @@
-Subproject commit 8175fdefd253d473887fa3f8dc6a89c66bacc0e7
+Subproject commit 3f5c01e42755c06d7021c559c9ece837acb5491b
diff --git a/pkgbuild/growlight b/pkgbuild/growlight
index 9a198e3..f269da7 160000
--- a/pkgbuild/growlight
+++ b/pkgbuild/growlight
@@ -1 +1 @@
-Subproject commit 9a198e3703596b29dfa8a3bac41f1bb8914693b2
+Subproject commit f269da70e1df95ac5af7d4d3bf7c8fbec0ffd19e
diff --git a/pkgbuild/guiscrcpy b/pkgbuild/guiscrcpy
index b767402..f453abf 160000
--- a/pkgbuild/guiscrcpy
+++ b/pkgbuild/guiscrcpy
@@ -1 +1 @@
-Subproject commit b7674020c22980aa86e2ddc994bf52447d8b1090
+Subproject commit f453abfc8d448ff722433ada6f6efd3928101fb6
diff --git a/pkgbuild/iicalc b/pkgbuild/iicalc
index af6d8c9..f9ae120 160000
--- a/pkgbuild/iicalc
+++ b/pkgbuild/iicalc
@@ -1 +1 @@
-Subproject commit af6d8c96d4edc38d434e2c88fb8d524a2f78b802
+Subproject commit f9ae1206cca102c00ebbcd6b7000b0f785897056
diff --git a/pkgbuild/ipscan b/pkgbuild/ipscan
new file mode 160000
index 0000000..a3eba06
--- /dev/null
+++ b/pkgbuild/ipscan
@@ -0,0 +1 @@
+Subproject commit a3eba06a9abbc55c838b165f596e9151f4ecee11
diff --git a/pkgbuild/joplin-appimage b/pkgbuild/joplin-appimage
index a22ca2d..a49aa01 160000
--- a/pkgbuild/joplin-appimage
+++ b/pkgbuild/joplin-appimage
@@ -1 +1 @@
-Subproject commit a22ca2d348b339874132a23a1c71c3412159640e
+Subproject commit a49aa01f049cecdb962ba0bc5c25f353c80fcb6c
diff --git a/pkgbuild/komikku b/pkgbuild/komikku
index e178b3a..2cf015b 160000
--- a/pkgbuild/komikku
+++ b/pkgbuild/komikku
@@ -1 +1 @@
-Subproject commit e178b3aa90cb465c94f39cf40cd0db2410f090a0
+Subproject commit 2cf015b7fadb6a6699cfa77a5cbc06955f727ed5
diff --git a/pkgbuild/librewolf-bin b/pkgbuild/librewolf-bin
index 0cc6d92..f0381ad 160000
--- a/pkgbuild/librewolf-bin
+++ b/pkgbuild/librewolf-bin
@@ -1 +1 @@
-Subproject commit 0cc6d92999ced9b47880283c73b5d07e73a47526
+Subproject commit f0381adc83d462ac711db782ccb5691d26fc632c
diff --git a/pkgbuild/linux-wifi-hotspot b/pkgbuild/linux-wifi-hotspot
index 1f5eaa4..1859ed9 160000
--- a/pkgbuild/linux-wifi-hotspot
+++ b/pkgbuild/linux-wifi-hotspot
@@ -1 +1 @@
-Subproject commit 1f5eaa4a0622524d52f6f925ac35410ef0f02a1c
+Subproject commit 1859ed94d69c8df85460a4553476a046de157832
diff --git a/pkgbuild/lollypop-stable-git b/pkgbuild/lollypop-stable-git
index bbc33c0..87a3467 160000
--- a/pkgbuild/lollypop-stable-git
+++ b/pkgbuild/lollypop-stable-git
@@ -1 +1 @@
-Subproject commit bbc33c0a25b89b0ac891027b56198d899d6343b4
+Subproject commit 87a346710ea540aad4f04cd2d21ef7283324ef71
diff --git a/pkgbuild/mediad b/pkgbuild/mediad
new file mode 160000
index 0000000..b0d468d
--- /dev/null
+++ b/pkgbuild/mediad
@@ -0,0 +1 @@
+Subproject commit b0d468d4f3e8e63445f6f8aecd4e7bd88d0c040b
diff --git a/pkgbuild/metadata-cleaner b/pkgbuild/metadata-cleaner
index 2d851e7..aa3ba7f 160000
--- a/pkgbuild/metadata-cleaner
+++ b/pkgbuild/metadata-cleaner
@@ -1 +1 @@
-Subproject commit 2d851e712455cbf592c6e8e64d0b2d4c2a0aea8a
+Subproject commit aa3ba7ff3c5762b4961c844dda4f9f5ab6aaa056
diff --git a/pkgbuild/minify b/pkgbuild/minify
index 6c18b92..c9e184c 160000
--- a/pkgbuild/minify
+++ b/pkgbuild/minify
@@ -1 +1 @@
-Subproject commit 6c18b9271aa4d8544b78d83201a805e66cfaef2b
+Subproject commit c9e184cef058cc8c0dd402d3118e8f83a1dbec66
diff --git a/pkgbuild/navi b/pkgbuild/navi
index a7d8d38..c2cc099 160000
--- a/pkgbuild/navi
+++ b/pkgbuild/navi
@@ -1 +1 @@
-Subproject commit a7d8d3894edb87cacb3ddd03a42824fb49fd141f
+Subproject commit c2cc0997dd2e14b3322c393fca04659108cd8775
diff --git a/pkgbuild/novelwriter b/pkgbuild/novelwriter
new file mode 160000
index 0000000..c556ba4
--- /dev/null
+++ b/pkgbuild/novelwriter
@@ -0,0 +1 @@
+Subproject commit c556ba4504b3daba455c9d4f18b98931a2d7af5c
diff --git a/pkgbuild/otoclone b/pkgbuild/otoclone
new file mode 160000
index 0000000..621bc4a
--- /dev/null
+++ b/pkgbuild/otoclone
@@ -0,0 +1 @@
+Subproject commit 621bc4a4484eb4a9c19ceb5aecc3431fa4e0344d
diff --git a/pkgbuild/sfwbar b/pkgbuild/sfwbar
new file mode 160000
index 0000000..e37ce3c
--- /dev/null
+++ b/pkgbuild/sfwbar
@@ -0,0 +1 @@
+Subproject commit e37ce3c08300bb19830451a5411906b3d16f1e4b
diff --git a/pkgbuild/silos b/pkgbuild/silos
index 19d819c..c197e3c 160000
--- a/pkgbuild/silos
+++ b/pkgbuild/silos
@@ -1 +1 @@
-Subproject commit 19d819cbd9dad8c7b8e4de1954e8611726d85843
+Subproject commit c197e3c18f8bba4df65df88089175b1d767ceb9a
diff --git a/pkgbuild/st-musiyenko-git b/pkgbuild/st-musiyenko-git
index 4e92b05..5b0fdc8 160000
--- a/pkgbuild/st-musiyenko-git
+++ b/pkgbuild/st-musiyenko-git
@@ -1 +1 @@
-Subproject commit 4e92b0556e8b387de1b1d499a8980580c67f8128
+Subproject commit 5b0fdc844a760640d00b6eb8f90bdf4d67b00d33
diff --git a/pkgbuild/tab-rs b/pkgbuild/tab-rs
index 8eca849..1eb1f5e 160000
--- a/pkgbuild/tab-rs
+++ b/pkgbuild/tab-rs
@@ -1 +1 @@
-Subproject commit 8eca84949c9af5e9f1d154a18acb742d7c3deefd
+Subproject commit 1eb1f5ea7a013b7062882ea12986ec06ab46c992
diff --git a/pkgbuild/tauon-music-box b/pkgbuild/tauon-music-box
index b4902a1..07a2850 160000
--- a/pkgbuild/tauon-music-box
+++ b/pkgbuild/tauon-music-box
@@ -1 +1 @@
-Subproject commit b4902a153b6e86473b17fe0b05c4597f9ae9f7bd
+Subproject commit 07a2850d7816209c9bf55b41ca410cc4995918ff
diff --git a/pkgbuild/ventoy-bin b/pkgbuild/ventoy-bin
index e5217a3..ca341ee 160000
--- a/pkgbuild/ventoy-bin
+++ b/pkgbuild/ventoy-bin
@@ -1 +1 @@
-Subproject commit e5217a3a76d62e20c08130f09a360a8b541bc1a1
+Subproject commit ca341ee2a4b3da2f1a9a2551e07cc51589f03463
diff --git a/pkgbuild/whatip b/pkgbuild/whatip
index 4390865..840000d 160000
--- a/pkgbuild/whatip
+++ b/pkgbuild/whatip
@@ -1 +1 @@
-Subproject commit 4390865b1f6cc1a8731ba764a94097eda114a925
+Subproject commit 840000decd99337b5b975b7a6ce8a23eed012800

commit b3f7a4a76d6e259a6cfd90a7aba73b616cff16e7
Author: Bruno Miguel <omitted>
Date:   Thu Jan 21 15:33:30 2021 +0000

    new packages; submodules updates

diff --git a/.gitmodules b/.gitmodules
index e992d3c..1b59c51 100644
--- a/.gitmodules
+++ b/.gitmodules
@@ -1762,3 +1762,9 @@
 \[submodule "pkgbuild/sslyze"\]
 	path = pkgbuild/sslyze
 	url = https://aur.archlinux.org/sslyze
+\[submodule "pkgbuild/flat-remix"\]
+	path = pkgbuild/flat-remix
+	url = https://aur.archlinux.org/flat-remix
+\[submodule "pkgbuild/pilgo"\]
+	path = pkgbuild/pilgo
+	url = https://aur.archlinux.org/pilgo
diff --git a/pkgbuild/flat-remix b/pkgbuild/flat-remix
new file mode 160000
index 0000000..68eaf8c
--- /dev/null
+++ b/pkgbuild/flat-remix
@@ -0,0 +1 @@
+Subproject commit 68eaf8c2bb15b84a8da88569f8ad48cafe41be3c
diff --git a/pkgbuild/pilgo b/pkgbuild/pilgo
new file mode 160000
index 0000000..aa3789a
--- /dev/null
+++ b/pkgbuild/pilgo
@@ -0,0 +1 @@
+Subproject commit aa3789ad83dba965756d9e83ccd2e063852b8c6f
diff --git a/pkgbuild/standardnotes-bin b/pkgbuild/standardnotes-bin
index 3b1dba9..e051ce7 160000
--- a/pkgbuild/standardnotes-bin
+++ b/pkgbuild/standardnotes-bin
@@ -1 +1 @@
-Subproject commit 3b1dba9c981968b92b7fa84011d8a58d8a88fb82
+Subproject commit e051ce7ab89109b8259cee1a0d5b2e3c216764fd
diff --git a/pkgbuild/tixati b/pkgbuild/tixati
index 4f9716e..ffd7162 160000
--- a/pkgbuild/tixati
+++ b/pkgbuild/tixati
@@ -1 +1 @@
-Subproject commit 4f9716e7a41c7d98095c3e384d7f4f663310453c
+Subproject commit ffd71623834120c51009383a459678b772dcda15
diff --git a/pkgbuild/vorta b/pkgbuild/vorta
index 2bf7e07..773f4bd 160000
--- a/pkgbuild/vorta
+++ b/pkgbuild/vorta
@@ -1 +1 @@
-Subproject commit 2bf7e07756a077f72bb1d9a6db99a3b620a86eb3
+Subproject commit 773f4bd09367370d1564a280062cc10007ad3aef

commit a8d4b3043bb03b7fb307a1c945b382b6f102479f
Author: Bruno Miguel <omitted>
Date:   Wed Jan 20 13:21:26 2021 +0000

    new packages; submodules updates

diff --git a/.gitmodules b/.gitmodules
index 533a9f6..e992d3c 100644
--- a/.gitmodules
+++ b/.gitmodules
@@ -306,7 +306,7 @@
 	url = https://aur.archlinux.org/rofimoji-git.git
 \[submodule "pkgbuild/scaleway-cli"\]
 	path = pkgbuild/scaleway-cli
-	url = https://aur.archlinux.org/scaleway-cli.git
+	url = https://aur.archlinux.org/scaleway-cli
 \[submodule "pkgbuild/scat"\]
 	path = pkgbuild/scat
 	url = https://aur.archlinux.org/scat.git
@@ -1750,3 +1750,15 @@
 \[submodule "pkgbuild/speedread-git"\]
 	path = pkgbuild/speedread-git
 	url = https://aur.archlinux.org/speedread-git
+\[submodule "pkgbuild/haruna"\]
+	path = pkgbuild/haruna
+	url = https://aur.archlinux.org/haruna
+\[submodule "pkgbuild/plotinus"\]
+	path = pkgbuild/plotinus
+	url = https://aur.archlinux.org/plotinus
+\[submodule "pkgbuild/howdoi"\]
+	path = pkgbuild/howdoi
+	url = https://aur.archlinux.org/howdoi
+\[submodule "pkgbuild/sslyze"\]
+	path = pkgbuild/sslyze
+	url = https://aur.archlinux.org/sslyze
diff --git a/pkgbuild/airgeddon-git b/pkgbuild/airgeddon-git
index 9578841..16a8aa2 160000
--- a/pkgbuild/airgeddon-git
+++ b/pkgbuild/airgeddon-git
@@ -1 +1 @@
-Subproject commit 95788417ab198bf436ff83d4b104a587009e5cbe
+Subproject commit 16a8aa27e6bc0bf148ca6bf104c43d1057c4ba6d
diff --git a/pkgbuild/haruna b/pkgbuild/haruna
new file mode 160000
index 0000000..2e4d40b
--- /dev/null
+++ b/pkgbuild/haruna
@@ -0,0 +1 @@
+Subproject commit 2e4d40b5156e0d732711b4a6b4755958bfa62d46
diff --git a/pkgbuild/howdoi b/pkgbuild/howdoi
new file mode 160000
index 0000000..c7dd9d7
--- /dev/null
+++ b/pkgbuild/howdoi
@@ -0,0 +1 @@
+Subproject commit c7dd9d79d8bde5363c3b87b125bb6d702963ef0f
diff --git a/pkgbuild/plotinus b/pkgbuild/plotinus
new file mode 160000
index 0000000..784745c
--- /dev/null
+++ b/pkgbuild/plotinus
@@ -0,0 +1 @@
+Subproject commit 784745c4b7e86f54c27efd7e8dd6d05a249f8897
diff --git a/pkgbuild/sslyze b/pkgbuild/sslyze
new file mode 160000
index 0000000..046fffb
--- /dev/null
+++ b/pkgbuild/sslyze
@@ -0,0 +1 @@
+Subproject commit 046fffb463a5e61edd21cd88d09086798ac8a866

commit d99699c007183f060b9ba2c14caf7279f2884df1
Author: Bruno Miguel <omitted>
Date:   Mon Jan 18 23:10:47 2021 +0000

    removed gimp-dbp, no longer exists in AUR

diff --git a/.gitmodules b/.gitmodules
index 108024d..533a9f6 100644
--- a/.gitmodules
+++ b/.gitmodules
@@ -850,9 +850,6 @@
 \[submodule "pkgbuild/gimp-plugin-lqr"\]
 	path = pkgbuild/gimp-plugin-lqr
 	url = https://aur.archlinux.org/gimp-plugin-lqr
-\[submodule "pkgbuild/gimp-dbp"\]
-	path = pkgbuild/gimp-dbp
-	url = https://aur.archlinux.org/gimp-dbp
 \[submodule "pkgbuild/giti-git"\]
 	path = pkgbuild/giti-git
 	url = https://aur.archlinux.org/giti-git

commit ea9dc882b673b078b9c87d1b8123737f66efd509
Author: Bruno Miguel <omitted>
Date:   Mon Jan 18 23:10:46 2021 +0000

    Removed gimp-dbp submodule

diff --git a/pkgbuild/gimp-dbp b/pkgbuild/gimp-dbp
deleted file mode 160000
index a26fe6e..0000000
--- a/pkgbuild/gimp-dbp
+++ /dev/null
@@ -1 +0,0 @@
-Subproject commit a26fe6ea5885cfe4f65fde30db4ad11aeab56e7f

commit 10cfd15b81879bd37a47523ca06f44f6dd45d904
Author: Bruno Miguel <omitted>
Date:   Mon Jan 18 23:09:02 2021 +0000

    removed peafox, no longer exists in AUR

diff --git a/.gitmodules b/.gitmodules
index 2d9cf96..108024d 100644
--- a/.gitmodules
+++ b/.gitmodules
@@ -1144,9 +1144,6 @@
 \[submodule "pkgbuild/scrotpush"\]
 	path = pkgbuild/scrotpush
 	url = https://aur.archlinux.org/scrotpush
-\[submodule "pkgbuild/peafox"\]
-	path = pkgbuild/peafox
-	url = https://aur.archlinux.org/peafox
 \[submodule "pkgbuild/cowspeak"\]
 	path = pkgbuild/cowspeak
 	url = https://aur.archlinux.org/cowspeak

commit e8f0476fb65f502c1aea3d6b93cab03cb559bbd9
Author: Bruno Miguel <omitted>
Date:   Mon Jan 18 23:09:00 2021 +0000

    Removed peafox submodule

diff --git a/pkgbuild/peafox b/pkgbuild/peafox
deleted file mode 160000
index 4bfb2d6..0000000
--- a/pkgbuild/peafox
+++ /dev/null
@@ -1 +0,0 @@
-Subproject commit 4bfb2d67c2264df7205b90d162a7a6d137cb7089

commit 5cf6d6c9cb93143ba48c3a0c5829efc937b2b51a
Author: Bruno Miguel <omitted>
Date:   Mon Jan 18 23:08:01 2021 +0000

    removed karma, no longer exists in AUR

diff --git a/.gitmodules b/.gitmodules
index ffff862..2d9cf96 100644
--- a/.gitmodules
+++ b/.gitmodules
@@ -634,9 +634,6 @@
 \[submodule "pkgbuild/dnsproxy-adguard"\]
 	path = pkgbuild/dnsproxy-adguard
 	url = https://aur.archlinux.org/dnsproxy-adguard
-\[submodule "pkgbuild/karma"\]
-	path = pkgbuild/karma
-	url = https://aur.archlinux.org/karma
 \[submodule "pkgbuild/gedit-plugin-markdown\_preview-git"\]
 	path = pkgbuild/gedit-plugin-markdown\_preview-git
 	url = https://aur.archlinux.org/gedit-plugin-markdown\_preview-git

commit 0aff7b7362388c1ba9119a1fb58d214ed31cc73b
Author: Bruno Miguel <omitted>
Date:   Mon Jan 18 23:07:59 2021 +0000

    Removed karma submodule

diff --git a/pkgbuild/karma b/pkgbuild/karma
deleted file mode 160000
index 925f2d5..0000000
--- a/pkgbuild/karma
+++ /dev/null
@@ -1 +0,0 @@
-Subproject commit 925f2d5f4f04e63d01f0e18eb0176e84187dd518

commit 7b2d5e4f7f75beaf4fb6afc8bab99eda3755acb7
Author: Bruno Miguel <omitted>
Date:   Mon Jan 18 23:05:21 2021 +0000

    removed marp because it no longer exists in aur; new packages; submodules updates

diff --git a/.gitmodules b/.gitmodules
index bac6ed8..ffff862 100644
--- a/.gitmodules
+++ b/.gitmodules
@@ -196,9 +196,6 @@
 \[submodule "pkgbuild/marktext-bin"\]
 	path = pkgbuild/marktext-bin
 	url = https://aur.archlinux.org/marktext-bin.git
-\[submodule "pkgbuild/marp"\]
-	path = pkgbuild/marp
-	url = https://aur.archlinux.org/marp.git
 \[submodule "pkgbuild/micro"\]
 	path = pkgbuild/micro
 	url = https://aur.archlinux.org/micro.git
diff --git a/pkgbuild/yambar b/pkgbuild/yambar
index 5f91793..7aeb39f 160000
--- a/pkgbuild/yambar
+++ b/pkgbuild/yambar
@@ -1 +1 @@
-Subproject commit 5f91793cd4870ded1930f45fadb60e1b37e90397
+Subproject commit 7aeb39f388dbe02b88642901484620944d08f102
diff --git a/pkgbuild/zettlr-bin b/pkgbuild/zettlr-bin
index cec0e3f..d82bb69 160000
--- a/pkgbuild/zettlr-bin
+++ b/pkgbuild/zettlr-bin
@@ -1 +1 @@
-Subproject commit cec0e3fcee8c305a301d6ceec8a75821940d1395
+Subproject commit d82bb69aef406046ccf5126ae433373ffc2ee281		
```

Image from [Pixabay](https://pixabay.com/photos/laptop-apple-keyboard-technology-2588606/), by [StockSnap](https://pixabay.com/users/stocksnap-894430/).
