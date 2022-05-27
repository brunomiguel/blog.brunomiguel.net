---
title: "Gitea e Whoogle"
summary: "Coloquei online uma instância do Gitea para alojar os meus repositórios git, e uma do Whoogle para que possas ter os resultados do Google Search sem o tracking"
description: "Coloquei online uma instância do Gitea para alojar os meus repositórios git, e uma do Whoogle para que possas ter os resultados do Google Search sem o tracking"
date: 2022-05-27
categories:
  - "geekices"
tags:
  - "gitea"
  - "git"
  - "motor de busca"
  - "whoogle"
  - "oracle cloud"
  - "ampere computing"
  - "vps"
  - "sysadmin"
  - "pastebin"
  - "google search"
cover:
  image: "post/gitea-whoogle/images/gitea-whoogle.webp"
  alt: "screenshot do gitea e do whoogle"
---

Há umas semanas, já não sei precisar exatamente quando, criei uma conta na *Oracle Cloud* para usar os recursos gratuitos que oferecem. Queria explorar melhor algumas ferramentas e como não tenho um portátil com *hardware* potente, esta pareceu-me uma excelente alternativa.

O primeiro passo foi explorar a plataforma, o interface hediondo e confuso que eles têm, e a capacidade das máquinas virtuais a correr em servidores da *Ampere Computing*. Nesta fase, criei uma pequena máquina virtual sem ter nada específico em mente, mas deparei-me com dificuldades quando mudei a porta do _daemon_ do _SSH_. Dei voltas e voltas no interface administrativo da plataforma, mas não consegui encontrar o local para abrir a porta de que precisava. Só ao fim de alguns dias é que lá encontrei a opção, escondida no meio de tantas outras, onde posso definir as portas que quero abertas para as máquinas virtuais.

Assim que este obstáculo foi ultrapassado, criei uma máquina virtual _Arm-based_ para alojar uma instância do _[Gitea](https://gitea.io/)_ e outra do _[Whoogle](https://github.com/benbusby/whoogle-search)_. O *Gitea* é uma _software forge_ para _Git_, semelhante ao _Github_ e ao _Gitlab_. O *Whoogle* é um motor de busca que serve de _frontend_ para o _Google_, sem expor o utilizador ao _tracking_ que ele faz.

A instância do _Gitea_ está disponível no endereço [git.brunomiguel.net](https://git.brunomiguel.net/). O intuito é pessoal, ou seja, não é possível criar uma conta lá. Posso abrir uma exceção se tiver um pedido razoável, já que não tenho muito espaço em disco disponível, mas este pedido tem de ser bem fundamentado. Se precisares de uma *software forge* para alojar os teus repositórios _Git_, recomendo-te o *[Codeberg](https://codeberg.org/)*; eu estou a usá-lo como _mirror_ dos meus repositórios _Git_. Já de agora, o _Codeberg_ também utiliza o _Gitea_.

A do _Whoogle_ está no endereço [search.brunomiguel.net](https://search.brunomiguel.net). Como já o usava no meu portátil, achei por bem disponibilizar este motor de busca a qualquer pessoa que quer os resultados do _Google Search_, mas sem o _tracking_. Se quiseres adicionar este motor de busca ao teu _browser_, basta clicares com o botão direito do rato em cima da barra de endereço e clicar na opção para adicionar.

Vais reparar, caso já conheças o _Whoogle_. que as cores são diferentes do original. Eu gosto da palete de cores _[Catppuccin](https://github.com/catppuccin/catppuccin)_, por isso usei-a para personalizar as cores da aplicação e torná-la menos cansativa à vista. Tenho de ver se arranjo energia para fazer algo idêntico com o _Gitea_.

O próximo passo deverá ser colocar um *pastebin* online, caso consiga encontrar um que não permita a criação de contas - para além da minha, claro está - e deixe criar conteúdos efémeros a utilizadores anónimos. O ideal até seria algo idêntico ao _Github Gist_. Tenho de ver e analisar que opções de código aberto existem.
