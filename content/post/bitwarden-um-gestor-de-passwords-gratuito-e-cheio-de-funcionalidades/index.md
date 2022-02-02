---
title: "Bitwarden, um gestor de passwords gratuito e cheio de funcionalidades"
date: "2018-09-03"
categories: 
  - "geekices"
---

**As _passwords_ são tão importantes quanto são difíceis de gerir.** Este é um dos motivos que nos leva a utilizar as mesmas palavras-passe repetidamente e a descartamos a complexidade em favor do facilitismos quando escolhemos/criamos uma.

**As _passwords_ também são difíceis de escolher.** As regras recomendadas há uns tempos atrás, em que nos diziam para combinar maiúsculas com números e caracteres especiais (o # ou o _\__ sendo dois exemplos), já não são párias para um pequeno _cluster_ de placas gráficas a processar informação para o [_hashcat_](https://hashcat.net/hashcat/).

E os _pins_ dos cartões? Centenas e centenas de balões…

https://www.youtube.com/watch?v=IgQE7545LHs

…quer dizer, dois ou três cartões, pelo menos, com _pins_ diferentes. Já nem falo do _Cartão de Cidadão_, que tem não sei quantos códigos diferentes.

### Memória de peixe

Caro leitor, quanto a ti não sei, mas eu não tenho [memória eidética](https://pt.wikipedia.org/wiki/Mem%C3%B3ria_eid%C3%A9tica). Até gostava de ser assim uma espécie de _Sheldon Cooper_, da série **_A Teoria do Big Bang_**, e ter a vulgarmente conhecida como “memória fotográfica”, para poder finalmente dizer à minha namorada: “Lembras-te quando fizeste/disseste/whatever blá blá blá blá blá”. Não podem ser sempre elas a ter este discurso, pá…!

Infelizmente não tenho e continua a ser só ela a ter estas conversas. Por não ter sido agraciado com esses genes, chega a uma altura em que preciso de algo que me ajude a gerir as _passwords_ e _pins_.

Esse algo tem que me permitir inserir a informação sem me preocupar com a realização de backups e cumprir os seguintes requisitos obrigatórios:  

- aplicação para _desktop_;
- integração com o _browser_;
- aplicação para _smartphone_;
- sincronização entre dispositivos;
- encriptação (preferencialmente antes da informação ser enviada para sincronização);
- conta gratuita com as funcionalidades acima disponíveis.

Existem algumas opções populares dentro dos gestores de _passwords_. O **_Lastpass_** e o **_Dashlane_** são talvez as mais conhecidas. As funcionalidades das contas gratuitas deixam, no entanto, muito a desejar no que toca ao cumprimento dos requisitos. Por exemplo, nenhum deles sincroniza entre dispositivos nas contas gratuitas, nem estas podem sequer ser usadas em mais que um equipamento.

O juiz decidiu, está decidido. Nenhuma destas opções serve para o pretendido.

### Uma viagem longa até ao destino  

Tendo em conta a oferta atual, encontrar um gestor de _passwords_ com as características que enumerei acima não é fácil. Mas não ser fácil não significa impossível. Pode é significar demorado e foi o que aconteceu: demorei até o encontrar, mas finalmente cheguei ao [**_Bitwarden_**](https://bitwarden.com/).

O _Bitwarden_ é uma aplicação de código aberto e pode ser usada de duas formas. A primeira, dada a sua natureza _opensource_, é a possibilidade de a instalar num servidor próprio e usar as aplicações para _desktop_ e sistemas operativos móveis para inserir os dados que se querem guardar. A outra forma é a criação de uma conta de utilizador no site, como com qualquer outro serviço.

Se optares pela segunda opção, terás algumas limitações na conta gratuita. Só poderás, por exemplo, ter duas coleções, que são uma espécie de pastas que podes partilhar com outros utilizadores, e só poderás partilhar com dois utilizadores. Como eu só quero guardar mas minhas palavras-passe e _pins_, estas limitações passam-me ao lado e arrisco a dizer que será o mesmo no teu caso, car@ leitor@.

O importante – encriptação, aplicações para _desktop_ e _smartphone_, sincronização e integração com o _browser_ – estão disponíveis a custo zero. A cereja no topo do bolo é que não há limite para o número de _passwords_ que podemos guardar.

Também importantes, mas já num nível mais secundário quando comparadas com as outras características, são a facilidade de utilização e a organização da informação. E aqui, novamente, o _Bitwarden_ não desilude.

### O serviço  

O interface permite criar pastas e organizar os _logins_ dessa forma. Para além dos _logins_, existem outros tipos de informação que podem ser guardados: cartões, identidades e notas.

Cada um destes tipos de informação tem campos próprios para preencher e ainda é possível criar campos personalizados de diferentes tipos. Os campos onde se escrevem as _passwords_ permitem gerar uma palavra-passe com forte entropia e ainda confirmar se a que escrevemos foi exposta em algum ataque informático.

As imagens que se seguem dão-te uma ideia de como tudo está organizado e o que o serviço permite fazer.

[![bitwarden](https://i1.wp.com/espalhafactos.com/wp-content/uploads/2018/09/bitwarden.jpg?resize=1156%2C548&ssl=1)](https://i1.wp.com/espalhafactos.com/wp-content/uploads/2018/09/bitwarden.jpg?ssl=1)

Lista de _logins_ e _pins_

[![bitwarden](https://i2.wp.com/espalhafactos.com/wp-content/uploads/2018/09/bitwarden2.png?resize=1200%2C675&ssl=1)](https://i2.wp.com/espalhafactos.com/wp-content/uploads/2018/09/bitwarden2.png?ssl=1)

Ecrã para registo de _logins_

O serviço está longe de ser perfeito. Se lidas com chaves criptográficas, vais reparar que falta uma forma simples de as guardar no _Bitwarden_. Dá sempre para copiar o conteúdo das chaves e colar nas notas ou em campos personalizados - é uma forma de resolver a questão, mas não é prática.

Fora estes pequenos “espinhos”, o _Bitwarden_ é um ótimo serviço para gestão de _passwords_ e que apresenta poucos limites para as contas gratuitas.
