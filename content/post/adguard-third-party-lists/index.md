---
title: "Nova versão do AdGuardHome e listas externas de bloqueios"
description: "A compilação da nova versão teve uns contratempos mas foi uma oportunidade para adicionar mais listas de bloqueio"
summary: "A compilação da nova versão teve uns contratempos mas foi uma oportunidade para adicionar mais listas de bloqueio"
author: "Bruno Miguel"
date: "2022-04-13"
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
  - "adblocker"
  - "tracker"
cover:
  image: "post/adguard-third-party-lists/images/adrian-williams-AU07BMLW1NA-unsplash.webp"
  alt: "Nova versão do AdGuardHome e listas externas de bloqueios"
---

A versão 0.107.6 do AdGuardHome foi _tagada_ hoje. Como tenho estado a compilar a aplicação do repositório _git_, aproveitei para compilar a nova versão. Isto não correu muito bem inicialmente mas depois lá se resolveu.

Quando compilei a aplicação da primeira vez, o serviço não corria e os *logs* não mostravam qualquer _output_ que me pudesse ajudar a aferir a causa. Presumo que tenha sido por não ter feito um _reset_ ao repositório antes de compilar e tenha carregado alguns artefactos da compilação anterior. Ou talvez tenha sido a configuração. 🤷

Na segunda compilação, já depois de ter forçado um _hard reset_ ao repositório, não voltei a ter problemas em correr o serviço. O único "problema", que na verdade foi mais um incómodo que outra coisa, foi ter de reconfigurar o AdGuardHome.

Como tive que fazer novamente a configuração, aproveitei a oportunidade para usar algumas listas externas, para além da minha [lista de bloqueio](https://raw.githubusercontent.com/brunomiguel/antinonio/master/antinonio-adguard.txt) para o *Nónio*. Essas listas são:

- [Energized Protection Unified](https://github.com/EnergizedProtection/block)
- [1Hosts Lite](https://github.com/badmojr/1Hosts/)
- [MVPS Hosts](https://winhelp2002.mvps.org/)
- [0131 block list](https://austinhuang.me/0131-block-list/)

Chamo-te a atenção para a primeira lista, _Energized Protection Unified_. Ela tem mais de 670 mil itens bloqueados e ocupa ~18MB. Dado este número enorme de entradas, é bem provável que haja duplicação de bloqueios entre ela e as outras listas, inclusive as que são incluídas no AdGuardHome. Se, por um lado, isto te garante melhor proteção contra _tracking online_, por outro é expectável que alguns sites possam não funcionar corretamente e sejas obrigado a adicionar algumas exceções aos bloqueios. Se achares que a proteção extra não compensa, o ideal é escolheres a lista [_Energized Protection Basic_](https://github.com/EnergizedProtection/block) e talvez alguma das listas de extensão para contextos específicos.

Tal como com a versão anterior, a única exceção que adicionei até agora, mesmo com todas aquelas listas ativas, foi para o Goatcounter. O Goatcounter é um serviço de estatísticas de visitas *open-source* e com uma [política de privacidade](https://www.goatcounter.com/help/privacy) de fazer inveja aos outros serviços do género.

<small>_A [imagem](https://unsplash.com/photos/AU07BMLW1NA) deste post é da autoria de [Adrian Williams](https://unsplash.com/@nairdasemaj) e foi publicada no [Unsplash](https://unsplash.com). A [licença](https://unsplash.com/license) está disponível no site._</small>
