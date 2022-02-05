---
title: "Migrar de Wordpress para Hugo"
date: "2022-02-04"
description: "Durante muitos anos, este blog usou Wordpress. Agora, usa o static site generator Hugo e tem melhor performance."
categories:
  - "geekices"
tags:
  - "wordpress"
  - "hugo"
  - "blog"
  - "migração"
  - "static site generator"
featuredImage: "/post/migrar-wordpress-hugo/images/chris-briggs-CG8lOT5dUew-unsplash.jpg"
---

Migrar este *blog* de *Wordpress* para um _static site generator_ é algo que pretendia fazer há algum tempo. A fase de planeamento começou no início do segundo trimestre de 2020. Pouco tempo depois, a fibromialgia surgiu na minha vida e fui obrigado a arrumar a ideia numa gaveta. A vontade de o fazer, contudo, nunca desapareceu; só faltava a energia e a concentração para passar à ação e para a realização do trabalho.

Em novembro do ano passado, aborrecido com a minha saúde e desejoso de arranjar algo para me ajudar a distrair das dores, comecei a preparar a migração. Vi algumas opções para _static site generator_ e acabei por escolher o *Hugo*. De todos os que vi, foi o que me pareceu mais simples de usar sem sacrificar funcionalidades e com várias boas opções de *templates* como base para desenvolver o meu. A experiência a criar o *blog* sobre fibromialgia também ajudou nesta decisão - se bem que, nesse, escolhi um *template* em que praticamente não fiz modificações.

## A migração

A parte inicial da migração foi a leitura da documentação do *Hugo* e a análise de alguns *templates* (sempre há um lado positivo em ter problemas em dormir por causa das dores: fica-se com tempo livre a mais). Este passo facilitou bastante os seguintes porque me muniu de conhecimento suficiente para começar a trabalhar o *template* que escolhi como base a uma velocidade aceitável, dentro das muitas limitações que a fibromialgia me trouxe - como a dificuldade de concentração, por exemplo.

Assim que aquilo que entendi como mínimo necessário para o _template_ estava feito, tive de arranjar forma de migrar o conteúdo para ficheiros *markdown*. Fazê-lo manualmente era impensável, pois era algo que ia demorar imenso tempo. A solução passava claramente pela automatização.

Encontrar uma ferramenta para fazer a conversão automaticamente não foi fácil. A documentação do _Hugo_ menciona algumas aplicações, mas nenhuma delas conseguiu produzir resultados minimamente desejáveis. Só depois de uma pesquisa num motor de busca é que encontrei uma que gera resultados satisfatórios, quando cheguei a este [post](https://loganmarchione.com/2021/02/migrating-from-wordpress-to-hugo/). A aplicação chama-se [wordpress-export-to-markdown](https://github.com/lonekorean/wordpress-export-to-markdown) e faz praticamente tudo bem na exportação menos gerar o _path_ para a imagem de destaque conforme a implementação que fiz no _template_. Para resolver isso, bastou realizar umas pequenas alterações ao código-fonte, alterações essas que irei publicar eventualmente.

Resolvido este problema, surgiu outro: corrigir a formatação de alguns *posts*. Este é um _work in progress_ e será feito conforme a energia que vou tendo para isso. Sim, quer dizer que pode demorar algum tempo.

## O _template_

Por forma a ter bons tempos de carregamento e uma base sólida fácil de alterar, escolhi o [*Paper*](https://github.com/nanxiaobei/hugo-paper) como *template* base. Este é um dos mais conhecidos e usados para *Hugo*, o que significa boa documentação, manutenção e também, em teoria, menos dores de cabeça para mim. Para dores de cabeça, já me bastam a fibromialgia e a sinusite. 😮‍💨

A base é boa, mas nem tudo é perfeito: por exemplo, o tema não suporta imagens de destaque. Para adicionar a funcionalidade, tive de usar a mesma implementação feita no _template_ do *blog* sobre fibromialgia, e adaptar a *metadata* do _Opengraph_ e _Twitter cards_ a essa implementação. Assim não há risco da imagem de destaque de um _post_ não aparecer quando é partilhado nas redes sociais.

Esta não foi a única alteração que fiz. Algumas delas foram estéticas, como uma palete de cores diferente ou a forma como a navegação entre páginas e _posts_ aparece. O _overflow_ da imagem de destaque, que também pode ser aplicado às imagens dentro do _post_ com a classe *CSS* _.full-width_, foi mais uma mudança que fiz ao original. Estas alterações aproximam o _template_ do que usava em _Wordpress_ e do qual gostava bastante.

Outras das alterações que fiz foram, por exemplo, a criação de um *shortcode* para conteúdos do *Spotify*, regras de _Cache-Control_ e ativação da compressão *gzip* na maioria dos conteúdos. Estas duas últimas alterações permitiram-me conseguir uma classificação de 100% para a página inicial no _PageSpeed Insights_.

## Repositório _git_

O conteúdo e o *template* estão disponíveis num repositório no _[Github](https://github.com/brunomiguel/blog.brunomiguel.net/)_. Este repositório, no entanto, é temporário: quando tiver a migração mais avançada, vou colocar o *template* num e o conteúdo noutro. Enquanto isso não acontece, podes ver o que tenho feito até agora, incluindo os disparates, no histórico de *commits*. Algum do histórico de alterações não está lá porque só criei o repositório uns tempos depois de ter começado a trabalhar na migração. Ainda assim, dá para teres uma ideia do fiz até agora E podes submeter *pull-requests* e reportar *bugs*, que eu agradeço.

Agora despeço-me com amizade. Até ao próximo *post*.

<small>_A [imagem](https://unsplash.com/photos/CG8lOT5dUew) deste post é da autoria de [Chris Briggs](https://unsplash.com/@cgbriggs19) e foi publicada no Unsplash. A [licença](https://unsplash.com/license) está disponível no site._</small>
