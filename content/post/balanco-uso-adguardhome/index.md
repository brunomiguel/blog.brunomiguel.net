---
title: "Balanço da utilização do AdGuardHome"
description: "O meu balanço da utilização do AdGuardHome é bastante positivo e recomendo a aplicação"
author: "Bruno Miguel"
date: "2022-03-10"
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
featuredImage: "/post/balanco-uso-adguardhome/images/adguardhome.png"
---

Há mais ou menos um mês que substitui o *Unbound* pelo *[AdGuardHome](https://adguard.com/en/adguard-home/overview.html)* como *DNS resolver* no meu portátil. O _Unbound_ funciona excecionalmente bem, é muito eficiente na utilização dos poucos recursos de que necessita e pode ser configurado para uma enormidade de tipos de redes. Apesar destas capacidades todas - e não são poucas, diga-se de passagem - falta-lhe bloqueio nativo de *trackers* e anúncios. Há algumas ferramentas _third-party_ que podes usar, mas...

É aqui que o *AdGuardHome* entra. Esta aplicação fica aquém da capacidade de configuração do _Unbound_, o que não é necessariamente uma desvantagem numa rede doméstica, mas compensa isso com suporte nativo para bloqueio de anúncios e *trackers*. É como ter um _adblocker_ fora do *browser*, disponível para todas as aplicações do sistema.

Desde que utilizo esta aplicação, só tive de adicionar uma exceção para o *goatcounter* às listas de bloqueio. Sem essa exceção, não consigo ver as estatísticas do *blog*. De resto, não foi necessário mais nada.

Eu uso o *software* como *resolver* local, como mencionei no primeiro parágrafo. Numa *SoC*, por exemplo, daria para fazer coisas bem mais interessantes. Algumas dessas possibilidades são usar o _AdGuardHome_ também como servidor _DHCP_ para todos os equipamentos ligados ao *router*, bloquear o acesso de um dispositivo a um ou mais *sites* enquanto permite que os outros acedam normalmente, ou bloquear o acesso a uma lista pré-definida de sites em todos os dispositivos.

O _AdGuardHome_ é software livre e está disponível para vários sistemas operativos, como *Linux*, *FreeBSD*, *OpenBSD* e *Android*. Até sistemas operativos inferiores, como *Windows* e *macOS*, são suportados. Para além disso, arquiteturas como *MIPS* e *Arm* também são suportadas nalgumas configurações.

Queres fazer o download? Visita o [repositório](https://github.com/AdguardTeam/AdGuardHome/) da aplicação no *Github* e [descarrega](https://github.com/AdguardTeam/AdGuardHome/releases) o ficheiro para o teu sistema operativo.
