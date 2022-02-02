---
title: "A história de uma ligação à internet que ficou manca das duas pernas, com um braço ao peito e com o outro amputado"
description: "Quando um serviço mau fica ainda pior!"
date: "2020-03-19"
categories: 
  - "geekices"
tags: 
  - "internet"
  - "nos"
  - "traffic-shaping"
featuredImage: "/post/mau-servico-net/images/ETeqCnHWoAA8sHP.jpg"
---

Sou cliente NOS há algum tempo, com um serviço (tarifário de 20MB) que funciona pela rede móvel mas que é comercializado pela operadora como fixo. Recentemente até refidelizei o meu contrato porque, apesar de algumas vezes aplicarem traffic shaping, estava relativamente satisfeito. Vá, estava mais ou menos satisfeito, mas aplicaram-me um desconto de 20% e lá acabei por refidelizar o contrato.

No final de Janeiro, ainda mal se falava da COVID-19, fiquei de baixa por questões de saúde que não estão relacionadas com esta pandemia. Ao passar mais tempo em casa, é natural que use mais a Internet, até porque subscrevo Netflix e Meo Go, e estes serviços têm sido a minha companhia nas muitas noites e dias sem dormir.

Em Fevereiro comecei a notar que, nalguns dias, a velocidade reduzia imenso: num período "bom", estava a pouco mais de 200KB/s, mas normalmente andava pelos 120KB/s e pouco. Acabava por ligar mais vezes a VPN, baseada em WireGuard, mas tudo bem. A ligação, entretanto, lá estabilizava.

Chegamos ao final do mês de Fevereiro - ou terá sido no início de Março? Desculpem, a memória já não é a melhor - e noto que, durante o dia, com sorte consigo velocidades de download de 120KB/s. Tentei acesso com a VPN e ficou a metade: aproximadamente 60KB/s, por vezes a aumentar ligeiramente, outras vezes a diminuir ligeiramente. Até experimentei com Shadowsocks e não houve melhorias.

Como achei isto estranho, reclamei com a operadora no Facebook porque, por motivos que me ultrapassam e para os quais não consigo encontrar uma justificação, o formulário de contacto da área de cliente só permite 700 caracteres. Sim, 700 caracteres. Isto é para cima de estúpido. Adiante...

Entretanto recebo o contacto, falo com um assistente do suporte técnico que me diz que é a PUR (Política de Utilização Responsável). Questiono quais os critérios de aplicabilidade desta PUR, quais os limites máximos para não ser afetado por ela, e só me soube dizer que estou no terceiro nível dela e que ela é aplicada conforme a zona do país. Questiono também quando é que é feito o "reset", mais uma vez não me sabe dizer nada de concreto.

Volto a reclamar, desta vez diretamente na linha, e dizem-me o mesmo. A pool de retenção da operadora diz-me para aguardar, que entretanto a minha ligação há-de voltar ao normal. Pergunto quando, mais uma vez não sabem (ou não podem?) dizer.

Com isto, tenho a minha ligação a 4% da capacidade total. A velocidade máxima que consigo é de 2500KB/s e, neste momento, com sorte, faço um download a 100KB/s. As contas são fáceis de fazer. E de nada adianta VPNs e afins, porque eles apertaram o garrote à séria e assim a minha velocidade ainda fica mais lenta (e não, não é da VPN). E nem sequer vou tocar no atropelo à neutralidade da rede que estão a fazer, ao limitarem ainda mais a velocidade a quem usa VPNs.

Hoje, soube que têm uma [página](https://www.nos.pt/particulares/Pages/covid-19.aspx) no site onde, no momento de publicação deste post, está o seguinte:

> • Privilegie sempre o uso da internet fixa em casa (wi-fi) quer seja no telemóvel, computador, tablet ou consola.
> 
> • Evite fazer download ou enviar vídeos, filmes, séries ou descarregar jogos de grande dimensão/qualidade. Se o fizer, mais uma vez, privilegie a utilização da internet fixa (wi-fi).
> 
> • Evite ver vídeos, filmes, séries online, na qualidade máxima dos conteúdos (HD, 4K) e ter vários equipamentos em simultâneo com este tipo de utilização.
> 
> • Sempre que possível, utilize o modo offline e privilegie a utilização da rede intensiva para o horário pós-laboral (18h00 - 9h00).

Já que a NOS me está a pedir que evite utilizar a internet entre as 9h e as 18h, gostava que me descontassem esses períodos na fatura.

Já que me estão a pedir para usar a internet que eles me venderam como fixa, era bom ter a velocidade a mais de 4% da capacidade total. Nem peço muito, só 500KB/s, porque percebo que há necessidade de garantir o acesso a todos os clientes.

Já que tenho a esposa a trabalhar a partir de casa, era bom ela não ter de usar os dados móveis para fazer videochamadas de trabalho porque a ligação de casa não dá para merda nenhuma. Estive quase 10h para descarregar um ISO do Ubuntu. 10h!

Já que não querem que use o Netflix e o Meo Go, vão reembolsar-me das mensalidades que estou a pagar?

A justificação da operadora é sempre a gestão da qualidade da rede. Contudo, se na minha zona não têm infraestrutura suficiente para os clientes que já tinham, porque não me informaram quando contratei o serviço e, depois, quando o refidelizei? Não pode ser só angariar clientes e o resto que se foda.

Entretanto descobri pelo Reddit que [não sou o único](https://www.reddit.com/r/portugal/comments/fl8yhk/s%C3%A9rio_traffic_shaping_da_nos_em_tempos_de_covid19/) a ter este problema.

Isto fez-me pesquisar as regras da ANACOM para estes tarifários ilimitados (mas sempre com limites) e encontrei [isto](https://www.anacom-consumidor.pt/velocidade-da-internet):

> No que respeita à Internet fixa, o seu contrato deve prever informação sobre:
> 
> • **velocidade mínima:** valor mínimo garantido pelo operador no contrato, o que significa que a velocidade medida em qualquer momento nunca pode ser inferior a este valor, exceto em caso de falha completa do serviço de acesso à Internet;
> 
> • **velocidade normalmente disponível:** valor que o utilizador pode esperar, a maioria das vezes (a indicar em percentagem, indicando o período de tempo tomado como referência para o seu cálculo), quando utiliza o serviço de acesso à Internet;
> 
> • **velocidade máxima:** valor máximo definido no contrato que o utilizador pode esperar pelo menos num determinado período do dia (que deve ser especificado), tecnicamente obtido em condições específicas de utilização/medição do serviço de acesso à Internet contratado; e
> 
> • **velocidade anunciada:** valor associado pelo operador às respetivas ofertas que abrangem serviço de acesso à Internet e que consta das suas comunicações comerciais, nomeadamente de natureza publicitária ou de _marketing_.
> 
> No que respeita à Internet móvel, o contrato deve indicar uma estimativa sobre:
> 
> • **velocidade máxima:** velocidade máxima realisticamente atingível no âmbito do contrato, dependendo do local de utilização, do equipamento terminal utilizado e da tecnologia de suporte; e
> 
> • **velocidade anunciada:** velocidade que a empresa está realisticamente em condições de disponibilizar aos utilizadores.

Como comercializam o serviço como fixo, assumo que se apliquem as regras dos serviços fixos. Já pedi esclarecimentos à ANACOM. Vamos lá ver se respondem.

Nota #1: o [Carlos Martins](https://twitter.com/ptnik) também publicou um [artigo](https://abertoatedemadrugada.com/2020/03/nos-limita-velocidade-de-netflix-e.html) sobre isto no AADM (a imagem do artigo é uma das que publiquei no Twitter e a que estou a usar aqui)

Nota #2: entretanto já encaminhei reclamação para a ANACOM

Nota #3: hoje, estranhamente, consegui ver dois filmes na Netflix sem ter que estar a aguardar pelo buffering. Nem vi a qualidade do stream, porque estava demasiado contente por conseguir utilizar o serviço, mas não parecia HD

Nota #4: desde ontem, 20/03, que a velocidade parece ter normalizado.Vamos lá ver durante quanto tempo isto se mantém
