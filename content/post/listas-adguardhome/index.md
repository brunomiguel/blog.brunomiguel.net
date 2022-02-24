---
title: "Listas de bloqueio para o AdGuardHome"
description: "O AdGuardHome vem com vinte e quatro listas de bloqueio incluídas e podes adicionar as tuas também"
author: "Bruno Miguel"
date: "2022-02-24T11:30:00+01:00"
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
featuredImage: "/post/listas-adguardhome/images/adguardhome-filter-list.png"
---

No [*post* anterior](https://blog.brunomiguel.net/post/adguard/), expliquei muito sucintamente como instalar o *AdGuardHome*. O processo é assim tão simples quanto parece e a utilização de recursos é surpreendentemente reduzida.

Após a conclusão da instalação a aplicação, podes pretender ter mais listas de bloqueio ativas que a lista padrão. No momento de escrita deste *post*, são vinte e quatro as listas incluídas, desde listas para bloquear *tracking* a listas para bloquear *malware*. Para adicionares uma ou mais, deves ir `Filters > DNS blocklists`, carregar no botão `Add blocklist` e, na _modal box_ que aparece, optar por uma das seguintes opções:

- `Choose from list` se quiseres usar uma ou mais listas incluídas;
- `Add custom list` para adicionares uma lista externa.

Para adicionares a minha [lista _Antinónio_ adaptada ao _AdGuardHome_](https://raw.githubusercontent.com/brunomiguel/antinonio/master/antinonio-adguard.txt), o botão a pressionar é `Add custom list`. Depois inseres o nome e o link direto para o ficheiro: https://raw.githubusercontent.com/brunomiguel/antinonio/master/antinonio-adguard.txt

Nalgumas situações, como a utilização do *software* numa *VPS* aberta ao mundo, obriga a pelo menos mais dois passos extra: obtenção de um certificado *SSL* e inserção do mesmo no _AdGuardHome_. O mais simples nesta situação é usar um certificado da _Let's Encrypt_, como é [explicado](https://github.com/AdguardTeam/AdGuardHome/wiki/Encryption) na *wiki* do projeto.

<small>_A imagem deste post é um screenshot da minha configuração de listas do AdGuardHome e está disponível sob a licença Creative Commons ([CC-BY-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/))_</small>
