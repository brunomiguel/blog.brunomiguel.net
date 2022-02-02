---
title: "Ativar a indicação de bateria de headphones Bluetooth no Plasma Desktop"
date: "2022-01-21"
categories: 
  - "geekices"
tags: 
  - "arch-linux"
  - "bluetooth"
  - "endeavouros"
  - "linux"
featuredImage: "/post/ativar-a-indicacao-de-bateria-de-headphones-bluetooth-no-plasma-desktop/images/jason-leung-xR4JHzr69Og-unsplash.jpg"
---

A última vez que atualizei este _blog_ foi há pouco mais de 2 meses. Como não quero que ele fiquei muito tempo sem conteúdo novo, decidi escrever este _post_, uma dica útil para quem usa o _Plasma Desktop_ e _headphones Bluetooth_, e quer ver a percentagem de bateria na _applet_.

Esta dica aplica-se a _EndeavourOS_, _Arch Linux_ e outras distribuições baseadas em _Arch_. Noutras, o _path_ do ficheiro pode ser diferente, por isso terás de ter isso em consideração se pretenderes replicá-a no teu sistema. Para além disso, se usares uma distribuição com outro _init system_, como o _runit_, também terás de ter isso em consideração.

Ativar a visualização da bateria de headphones Bluetooth no Plasma é simples. Abre o ficheiro `/usr/lib/systemd/system/bluetooth.service` com o teu editor de texto preferido e, na linha `ExecStart=/usr/lib/bluetooth/bluetoothd`, adiciona `--experimental` à frente.

Exemplo:

```bash
sudo micro /usr/lib/systemd/system/bluetooth.service
```

```
[Unit]
Description=Bluetooth service
Documentation=man:bluetoothd(8)
ConditionPathIsDirectory=/sys/class/bluetooth

[Service]
Type=dbus
BusName=org.bluez
ExecStart=/usr/lib/bluetooth/bluetoothd --experimental
NotifyAccess=main
#WatchdogSec=10
#Restart=on-failure
CapabilityBoundingSet=CAP_NET_ADMIN CAP_NET_BIND_SERVICE
LimitNPROC=1
ProtectHome=true
ProtectSystem=full

[Install]
WantedBy=bluetooth.target
Alias=dbus-org.bluez.service
```

Posto isto, necessitas de reiniciar o serviço do _bluetooth_ com o comando `sudo systemctl restart bluetooth`, sair da sessão atual do _Plasma_ e fazer _login_ novamente.

Queres ver como fica antes de adicionar a _flag_? Vê o _tweet_ que publiquei sobre isto.

https://twitter.com/brunomiguel/status/1484344633509306368

_foto do [Unsplash](https://unsplash.com/photos/xR4JHzr69Og)_
