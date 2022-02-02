---
title: "Lista antinonio atualizada"
date: "2020-06-24"
categories: 
  - "geekices"
tags: 
  - "antinonio"
  - "nonio"
featuredImage: "/post/lista-antinonio-atualizada/images/3hfg28.jpg"
---

Há alguns meses que não atualizava a minha [lista](https://github.com/brunomiguel/antinonio/) de bloqueio, para _adblockers_, à merda do _Nónio_. Ela não me estava a dar problemas, por isso não senti necessidade de a rever.

No dia 21 de junho, no entanto, um dos _developers_ do _uBlock Origin_ abriu um [bug](https://github.com/brunomiguel/antinonio/issues/24) por causa dos tipos de regras usadas, _bug_ esse que está relacionado com [outro](https://github.com/uBlockOrigin/uBlock-issues/issues/1118) reportado no repositório deste _adblocker_. TL;DR: estava a misturar filtros estáticos com regras dinâmicas.

Enquanto corrigia o problema, aproveitei por fazer duas pequenas atualizações na lista. A primeira, sugerida num comentário do _bug report_, é a remoção d'_O Público_ da lista, uma vez que [já não faz parte](https://www.publico.pt/2019/12/03/tecnologia/noticia/publico-sai-plataforma-nonio-1896067) da rede _Nónio_.

A outra alteração foi a remoção do domínio windows.net da lista, uma vez que o [_MEO GO_](https://meogo.meo.pt) está a usar este domínio para algum tipo de validação relacionado com o _Widevine_ e os utilizadores da minha lista não vão conseguir utilizar o serviço da _MEO_ se a tiverem ativa. Dá sempre para permitir este domínio quando se visita o site do _MEO GO_, mas para isso têm que primeiro detetar o problema e mais vale facilitar a vida aos utilizadores do que os fazer andar atrás do problema.

Para terem a nova versão da lista basta aguardarem pela atualização automática, que acontece a cada 3 horas. Se quiserem acelerar o processo, podem sempre forçar a atualização dentro das opções do _uBlock Origin_.

Se não sabes o que é o [_Nónio_](https://nonio.pt/), este site, criado pelo [@tomahock](twitter.com/tomahock/), explica o que é e porque é mau.
