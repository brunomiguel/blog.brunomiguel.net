---
title: "Mudei o tema do blog"
summary: "O blog está de cara lavada, desta vez com um tema com mais funcionalidades"
description: "Voltei a mudar o tema do blog, desta vez para um com mais funcionalidades"
date: 2022-03-17
categories: 
  - "geekices"
tags:
  - "blog"
  - "catppuccin"
  - "fork"
  - "hugo"
  - "palete de cores"
  - "paper"
  - "paperino diddly"
  - "papermod"
  - "template"
cover:
  image: "images/tadeusz-lakota-P6vDUuzL90w-unsplash.webp"
  alt: "tema novo"
---

Num notícia que surpreende zero pessoas, voltei a mudar o tema do *blog*. Até agora, usava um *fork* que criei do *[Paper](https://github.com/nanxiaobei/hugo-paper)* e a que chamei *Paperino Diddly*. A inspiração para o trocadilho com o nome é, como já deves ter percebido (se não percebeste, tens de pensar seriamente no que andas a fazer com a tua vida), o Ned Flanders. O tema está tanto no [*Github*](https://github.com/brunomiguel/blog.brunomiguel.net/) como no [*Codeberg*](https://codeberg.org/brunomiguel/blog.brunomiguel.net), se quiseres usá-lo e/ou dar-lhe uma vista de olhos.

O *Paperino Diddly* tem vários pontos positivos, como a classificação de 100% que consegue no [*PageSpeed*](https://pagespeed.web.dev/) e [*GTmetrix*](https://gtmetrix.com/), o aspeto minimalista e o suporte para imagens de destaque nos *posts* e páginas. Por outro lado, falta-lhe coisas "básicas" como pesquisa e que se estavam a revelar mais complicadas e mentalmente exigentes de implementar do que pensei inicialmente.

O tema novo é o *[PaperMod](https://github.com/adityatelange/hugo-PaperMod/)*, com algumas alterações para acomodar os conteúdos existentes. Este tema é muito mais completo e permite manter o aspeto minimalista _out-of-the-box_. Infelizmente ainda não consegui obter classificações de 100% no *PageSpeed* e no *GTmetrix* com ele, mas estou a trabalhar nisso quando tenho energia mental para o fazer.

A mudança de tema foi também uma ~~desculpa~~ oportunidade para implementar a palete de cores *[Catppuccin](https://github.com/catppuccin/catppuccin)*. Parte das cores são as originais da palete; outras, são versões mais saturadas das padrão, o que faz com que tenham mais destaque e impacto visual.

O código-fonte [está](https://github.com/brunomiguel/blog.brunomiguel.net/) [online](https://codeberg.org/brunomiguel/blog.brunomiguel.net). Desta vez, ao invés de criar um *fork*, decidi usar o original como submódulo *git* e implementar as alterações na raiz do site. O [Hugo](https://gohugo.io/) suporta [isto](https://gohugo.io/templates/lookup-order/), o que é ótimo pois permite-me usar as minhas alterações em cima da última versão do *PaperMod*.

A implementação do tema é muito recente, por isso é possível que encontres algumas inconsistências e erros. Se encontrares, diz-me alguma coisa no *[Twitter](https://twitter.com/brunomiguel)*, para que possa corrigir os _bugs_.

<small>_A [imagem](https://unsplash.com/photos/P6vDUuzL90w) deste post é da autoria de [Tadeusz Lakota](https://unsplash.com/@tadekl) e foi publicada no [Unsplash](https://unsplash.com). A [licença](https://unsplash.com/license) está disponível no site._</small>
