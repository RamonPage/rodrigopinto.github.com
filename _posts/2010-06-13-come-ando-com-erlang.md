--- 
layout: post
title: "Começando com Erlang"
date_pt_BR: 13 JUN 2010
---

Na última semana, dei o ponta pé inicial nos estudos sobre **[Erlang][1]**, para ser mais preciso na terça-feira dia 01/06/2010. Faz algum tempo que estou interessado em aprender um pouco sobre **[programação funcional](http://pt.wikipedia.org/wiki/Programa%C3%A7%C3%A3o_funcional )**, porém estava sempre colocando outras  *"prioridades"* em primeiro lugar e não conseguia o tempo necessário para iniciar os estudos. 
Porém, resolvi conseguir este tempo quando o **[Alessandro Martins](http://www.aleuai.com.br/blog/)** e o Vanderson *"Argentino"* Motta decidiram criar um **[ForkinRio](http://groups.google.com.br/group/forkinrio?hl=pt-BR)** **[Erlang][1]**, dado meu prévio interesse de aprender algo novo e diferente para quebrar um pouco o paradigma, me juntei a galera.
Sendo assim, a partir  de hoje vou começar a fazer minhas notas aqui no blog, e você poderá acompanhar e evoluir junto com a turma do **ForkinRio**.

Partindo para o que interessa, vamos começar a falar de **[Erlang][1]**.

**Sobre Erlang ->**

Nasceu de pesquisas dentro da Ericsson para suprir as necessidades na área de telefonia. Sua primeira versão foi feita por Joe Armstrong em 1986 e seu código era proprietário, porém em 1998 teve sua primeira versão liberada como open-source.
**[Erlang](http://www.erlang.org)** foi projetado com foco em "non-stop system"(sistemas de operação contínua como por exemplo, sistemas de telefonia, tráfego aéreo e outros, ou seja, sistemas que não podem sair do ar para que sejam feitas alterações conhecido também como *[Hot-Swapping](http://en.wikipedia.org/wiki/Hot_swapping)*). 
Algumas outras caracteríticas importantes são sintaxe declarativa, concorrência, real-time(tempo real), distribuição, robustez, integração e gerenciamento de memória com *[Garbage Collector](http://pt.wikipedia.org/wiki/Coletor_de_lixo)* em tempo real. 

Agora que já temos uma breve idéia de onde, como e porque surgiu, vamos colocar a mão na massa.

**Instalação ->**

A instalação você pode conferir no próprio site do Erlang, onde você encontrará o necessário para **[UNIX](http://erlang.org/doc/installation_guide/install.html#id2258617)** e tambêm para **[Windows](http://erlang.org/doc/installation_guide/install.html#id2252066)**.

**Matando a curiosidade ->**

Agora vamos ver as coisas funcionando.
Abra o console e digite __*erl*__, ele deverá ter a aparência a seguir:

<script src="http://gist.github.com/436107.js"></script>

Se o seu console se pareceu com este exemplo acima está tudo ok, se alguma coisa deu errado, reveja a instalação.
Para começar, vamos falar sobre pogramação sequêncial, que ê algo básico e ao mesmo tempo importante.

**Programação sequencial ->**

Em Erlang a ordem de declaração das cláusulas tem importância.
Como sou muito criativo, vou usar o exemplo padrão que ê o fatorial. Crie um arquivo chamado factorial.erl, ele terá o seguinte conteÃ?Âºdo:

<script src="http://gist.github.com/436094.js"></script>

Neste exemplo, definimos duas cláusulas para o factorial, *fac(0)* e *fac(N)*, quando a função __*fac* __ for chamada para **1** argumento, as cláusulas serão verificadas sequencialmente, ou seja, a primeira ocorrência no módulo que tiver correspondência com o padrão (**[Pattern Matching](http://en.wikipedia.org/wiki/Pattern_matching)**) chamado, será executada.
Abra o console novamente, copile o código e execute uma chamada para cada a função fatorial com parâmetros diferentes como o exemplo abaixo:

<script src="http://gist.github.com/436108.js"></script>

É importante definir a cláusula **fac(0)** antes de **fac(N)**, pela questão da verificação sequencial, 
senão sempre quer for feita uma chamada a função **fac**, será executada a função **fac(N)**. 
Faça o teste alterando o arquivo para:

<script src="http://gist.github.com/436113.js"></script>

Volte para o console e tente compilar o arquivo, e você terá um *warning* como este a seguir.

<script src="http://gist.github.com/436117.js"></script>

Com está mensagem de alerta que o console nos mostra, fica fácil entender como funciona a programação sequencial!?! 

E com isso fechamos este post inicial sobre **Erlang**, e se você curtiu o aguarde os próximos.

Abraços e até mais.

[2]: http://www.erlang.org