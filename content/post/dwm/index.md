---
title: "DWM"
summary: "O meu window manager preferido é o i3wm, mas o dwm está a ganhar terreno."
description: "O meu window manager preferido é o i3wm, mas o dwm está a ganhar terreno."
date: 2023-02-18
categories:
  - "geekices"
tags:
  - "dwm"
  - "i3wm"
  - "window managers"
draft: false
cover:
  image: "post/dwm/images/dwm-screenshot.webp"
  alt: "Screenshot da minha configuração do dwm"
---

O _i3wm_ (e o _i3-gapps_, antes de ter sido descontinuado) é o meu _window manager_ preferido. É super leve, bastante configurável, a interação com ele dá para fazer quase exclusivamente com o teclado e foi uma adaptação bastante rápida para mim. É por isso que o uso há alguns anos quase a tempo inteiro, com umas passagens por _desktop managers_ como o _Plasma Desktop_.

Apesar de estar muito satisfeito com o _i3wm_ e a configuração que uso nele, o _dwm_ andava a despertar-me interesse há algum tempo. O _dwm_ é outro gestor de janelas, ainda mais leve, mas também tem menos funcionalidades. O número reduzido de funcionalidades pode, no entanto, ser contornado através da aplicação de [_patches_](https://dwm.suckless.org/patches/) ao código-fonte do programa. Claro que isso te obriga a compilar o código-fonte, mas o tempo de compilação demora apenas uns segundos.

Há dois meses, lá decidi testar o _dwm_. O meu objetivo inicial era usá-lo sem _patches_, mas mudei de ideias num instante. Ter suporte para execução automática de aplicações no início da sessão, uma _systray_ e mais umas coisas que não estão incluídas por _default_, faz falta e dá jeito para a minha utilização. Bem, é possível executar aplicações no arranque do _dwm_ de outra forma, mas eu não quero deixar de usar o _emptty_ e passar a usar o [_.xinitrc_](https://wiki.archlinux.org/title/Xinit).

Ao longo deste período, tenho usado o _dwm_ ocasionamente. Como personalizei este _window manager_ para se comportar de forma idêntica ao outro, a experiência tem sido positiva. Uma das coisas que me agrada bastante é o conceito de _tags_ ao invés de _desktops_ virtuais. A diferença entre eles é que é possível ver as janelas de duas ou mais _tags_ em simultâneo, enquanto com _desktops_ virtuais só dá para ver um de cada vez.

Um exemplo disto é o seguinte.

Numa _tag_, tens um emulador de terminal a correr um _multiplexer_ como o _tmux_, onde tens o _neovim_ a correr, um servidor _web_ local, etc, para desenvolveres uma plataforma para a _web_; noutra _tag_, tens o _browser_, onde vês a plataforma que estás a desenvolver. Em vez de colocares tudo na mesma _tag_, podes apenas mostrar essas duas quando necessitas e voltar a mostrar só uma quando não é necessário visualizar as duas. Isto, para mim, permite uma melhor organização.

Claro que nem tudo é positivo. Usar _patches_ vai obrigar-te a lidar com erros quando os tentas aplicar. Também tens de fazer muita coisa manualmente para configurares o _dwm_, como editar o código-fonte para definires as cores e o tipo de letra que queres. Bem, verdade seja dita, o processo é idêntico com o _i3wm_, só que essas configurações são feitas num ficheiro de configuração e não no código-fonte.

No geral, estou contente com o _dwm_, mas não creio que vá substituir o _i3wm_ a curto ou médio prazo.
