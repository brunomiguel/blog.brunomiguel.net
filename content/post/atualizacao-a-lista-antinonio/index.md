---
title: "Atualização à lista AntiNónio"
date: "2019-11-24"
categories: 
  - "geekices"
tags: 
  - "adblock"
  - "antinonio"
  - "nonio"
  - "privacidade"
featuredImage: "/post/atualizacao-a-lista-antinonio/images/3hfg28.jpg"
---

Hoje, graças a ela, que tentou ver um vídeo do Miguel Sousa Tavares no site da _TVI24_, apercebi-me que as páginas com vídeos daquele endereço mostravam o spam do _Nónio_. "Estranho", pensei eu. "Isto devia estar bloqueado".

Uma análise inicial levou-me a pensar que o culpado era um _script_ relacionado com o leitor de vídeo que utilizam, devido à presença da palavra-chave nonio no código. Isto acabou por se revelar errado.

Depois de uma nova vista de olhos nos _scripts_, o que está relacionado com a barra _IOL_ pareceu-me ser o "gato escondido com o rabo de fora". E era. Quase... Na verdade era só o _rabo_. Ao bloquear esse _script_, os vídeos não eram mostrados; a _popup_ do _Nónio_ também não aparecia mas invalidava o acesso ao vídeo.

Quando olhei para o conteúdo dele, apercebi-me que também invoca outros ficheiros _javascript_. Um deles, o _cdn.iol.pt/BarraIOL/dist/main.js_, também contém várias menções àquele incómodo irritante no código fonte.

Bingo! É aquele sacana.

Depois de descoberto, fiz novo _commit_ no repositório e adicionei um bloqueio ao elemento visual relacionado com o _spam_ do _Nónio_, _just in case_.

Para teres a [última versão](https://github.com/brunomiguel/antinonio/), força a atualização das listas no _adblocker_ que usas ou aguarda pela atualização automática.
