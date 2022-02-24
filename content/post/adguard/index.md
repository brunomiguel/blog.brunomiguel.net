---
title: "Instalar o AdGuardHome"
description: "O AdGuardHome é um DNS resolver local capaz de funcionar também como adblocker e servidor DHCP"
author: "Bruno Miguel"
date: "2022-02-24"
categories: 
  - "geekices"
tags:
  - "AdGuardHome"
  - "DNS"
  - "Git"
  - "Software Livre"
  - "Open-Source"
  - "Código Fonte"
  - "resolver"
  - "unbound"
  - "DNS resolver"
featuredImage: "/post/adguard/images/adguardhome.png"
---

Há mais de um ano que uso o _unbound_ como _DNS resolver_ local. Esta é uma boa forma de poder abstrair a gestão dos servidores de _DNS_ usados no meu portátil, sem ter de passar a vida a editar o `/etc/resolv.conf` ou a lutar contra aplicações como o _systemd-resolvconf_ e o _network-manager_.

A configuração ativa que tenho no _unbound_ é a que se segue:

```yaml
server:
  access-control: 127.0.0.0/8 allow
  access-control: ::1/128 allow
  interface: ::
  interface: 0.0.0.0
        do-ip4: yes
        do-ip6: yes
        do-udp: yes
        do-tcp: yes
  aggressive-nsec: yes
  cache-max-ttl: 14400
  cache-min-ttl: 300
  hide-identity: yes
  hide-version: yes
  minimal-responses: yes
  prefetch: yes
  qname-minimisation: yes
  rrset-roundrobin: yes
  use-caps-for-id: yes
  verbosity: 0
  tls-upstream: yes
  tls-cert-bundle: /etc/ssl/certs/ca-certificates.crt
forward-zone:
   name: "."
   forward-tls-upstream: yes
   forward-first: no # do NOT send direct
   # Quad 9 DNS - default
   forward-addr: 9.9.9.9@853#dns.quad9.net
   forward-addr: 149.112.112.112@853#dns.quad9.net
   forward-addr: 2620:fe::fe@853#dns.quad9.net
   forward-addr: 2620:fe::9@853#dns.quad9.net
   # Quad9 DNS - unfiltered
   #forward-addr: 9.9.9.10@853#quad9.net
   #forward-addr: 149.112.112.10@853#quad9.net
   #forward-addr: 2620:fe::10@853#quad9.net
   #forward-addr: 2620:fe::fe:10@853#quad9.net
   # AdGuard DNS
   #forward-addr: 94.140.14.140@853#dns-unfiltered.adguard.com
   #forward-addr: 94.140.15.15@853#dns-unfiltered.adguard.com
   #forward-addr: 2a10:50c0::1:ff@853#dns-unfiltered.adguard.com
   #forward-addr: 2a10:50c0::2:ff@853#dns-unfiltered.adguard.com
   # Cloudflare DNS
   #forward-addr: 2606:4700:4700::1111@853#cloudflare-dns.com
   #forward-addr: 1.1.1.1@853#cloudflare-dns.com
   #forward-addr: 2606:4700:4700::1001@853#cloudflare-dns.com
   #forward-addr: 1.0.0.1@853#cloudflare-dns.com
```

No entanto, já há algum tempo que tinha curiosidade em testar o _AdGuardHome_. A funcionalidade de _adblocker_ interessou-me bastante e parece-me uma boa forma de impedir que alguns _scripts_ de _tracking_ cheguem, não só ao *browser*, mas às aplicações como o *Discord* e outras potencialmente problemáticas no que toca à privacidade.

Existe também uma funcionalidade que permite usar o _AdGuardHome_ como servidor *DHCP*. Como pretendo utilizá-lo apenas no meu portátil, esta não me interessa. Quem tem um computador ou uma _SoC_ para atribuir *IPs* na rede pode ter interesse nela, ao mesmo tempo que bloqueia algum _tracking_.

# Instalação

## Usar binário pré-compilado

O projeto tem *releases* binárias para além do código-fonte no _Github_. Sempre que uma nova versão é _tagada_, os binários para diferentes sistemas operativos e arquiteturas de _hardware_ são colocados na [secção de _releases_ do repositório](https://github.com/AdguardTeam/AdGuardHome/releases). A forma mais simples de usar o _AdGuardHome_ é descarregar uma destas _releases_, descompactar e correr a aplicação como _root_.

```shell
sudo ./AdGuardHome
```

Usar estes binários não torna a ativação persistente. Para isso é necessário abrir um terminal, ir até à pasta onde está o binário e usar o comando `sudo ./AdGuardHome -s install`. Ao fazeres isto, o binário é colocado em `/var/lib/adguardhome`, o serviço do _systemd_ é instalado e o seu estado passa a poder ser controlado pelo `systemctl` se preferires este interface.

Sempre que sair uma versão nova, tens de a descarregar e voltar a correr o comando de instalação `sudo ./AdGuardHome -s install`.

## Compilar o código-fonte

A compilação do _AdGuardHome_ pode ser feita de duas formas: usando o código-fonte de uma *[release](https://github.com/AdguardTeam/AdGuardHome/releases)* específica ou a *brach master* do repositório *git*. Qualquer que seja a tua opção, deves garantir que todas as dependências estão instaladas. Tudo o que é necessário está no [_README.md_](https://github.com/AdguardTeam/AdGuardHome#how-to-build).

Posto isto, basta apenas executar o `make` na pasta do código-fonte.

Caso pretendas compilar apenas o binário para o teu sistema operativo e arquitetura específica, podes complementar o `make` da seguinte forma:

```shell
make GOOS='linux' GOARCH='amd64'
```

No exemplo acima, o binário vai ser compilado para *Linux* e processadores _x86_64_. Se tiveres um *rPI* ou uma _SoC_ idêntica, podes trocar `amd64` por `arm64` ou `arm7`, por exemplo. O _[scripts/make/build-release.sh](scripts/make/build-release.sh)_ tem a listagem dos sistemas operativos e arquiteturas de _hadware_ suportadas. Se quiseres dar uma vista de olhos, aquele é o ficheiro a consultar obrigatoriamente.

O binário criado fica na raiz da pasta com o código-fonte. Para o tornar persistente, tal como na opção anterior, é necessário usares o comando `sudo ./AdGuardHome -s install`. Como no exemplo anterior, o binário é colocado em `/var/lib/adguardhome`, o serviço do _systemd_ é instalado e o seu estado passa a poder ser controlado pelo `systemctl` se preferires este interface.

Sempre que atualizares o repositório para um _commit_ mais recente, tens de recompilar e correr novamente o comando de instalação `sudo ./AdGuardHome -s install`.

# Configuração

A configuração do _AdGuardHome_ é simples. Quando o abres pela primeira vez, dá-te o endereço para abrires no *browser* e mostra um assistente de configuração simples. Basta seguires os poucos passos do processo e ficas com os *defaults*, que deverão ser suficientes.

Se pretenderes mais listas de bloqueio, o *interface web* permite escolher várias pré-definidas e adicionar externas. Eu fiz um pequeno *[port](https://raw.githubusercontent.com/brunomiguel/antinonio/master/antinonio-adguard.txt)* da minha lista *Antinónio* para o *AdGuardHome*, se estiveres interessado.

É possível, contúdo, que tenhas de adicionar exceções à lista de bloqueios através do _interface web_ da aplicação. Eu só fui forçado a fazê-lo uma vez depois de adicionar mais listas, apenas para não ter acesso bloqueado ao endereço das estatísticas deste *blog*, o *goatcounter.com*. A lista que contém o bloqueio barra tudo desse domínio.

# Conclusão

Isto é uma introdução muito simples ao processo de instalação do _AdGuardHome_ e assume que estás minimamente à vontade com um terminal. Se não for o teu caso, é melhor leres a [documentação](https://github.com/AdguardTeam/AdGuardHome/wiki) do projeto.
