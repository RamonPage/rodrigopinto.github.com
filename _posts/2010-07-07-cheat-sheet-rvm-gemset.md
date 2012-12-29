---
layout: post
title: "[Cheat Sheet] RVM +Gemset"
---

Após fazer uma "limpeza" no meu ambiente ruby utilizando o **[RVM](http://rvm.beginrescueend.com/rvm/)** que Ã?Â© um  gerenciador de **rubies**  e a **[Gemset](http://rvm.beginrescueend.com/gemsets/)** que o gerenciador de diretórios de gems do **RVM**.
Resolvi deixar aqui um cheat sheet para facilitar que for utilizar o  **[RVM + Gemset](http://rvm.beginrescueend.com/)**.
Então delicie-se com essa maravilha, que só não é 100% porque não faz café. ;p

Para fazer a instalação do **RVM** confira em **[RVM install](http://rvm.beginrescueend.com/rvm/install/)**, após finalizar a instalação divirta-se com as dicas abaixo.

Instalando uma versão do ruby no RVM

rvm install <versão-ruby>

<pre class="terminal">
$ rvm install 1.8.7, ree
</pre>

Definindo a versão do ruby

rvm <versão-ruby>

<pre class="terminal">
$ rvm ree
</pre>

Definindo uma versão default do ruby no RVM

rvm --default <versão-ruby>

<pre class="terminal">
$ rvm --default 1.8.7
</pre>

Trocando a versão do ruby do RVM  para o ruby do seu sistema

<pre class="terminal">
$ rvm system
</pre>

Listando seus **rubies** instaladas via RVM

<pre class="terminal">
$ rvm list
</pre>

Verificando a Gemset atual

<pre class="terminal">
$ rvm gemdir
</pre>

Criando uma Gemset

rvm gemset create *<nome>*

<pre class="terminal">
$ rvm gemset create meu_projeto
</pre>

Definindo uma versão do ruby e uma Gemset específica para um projeto

**Criar  um arquivo .rvmrc na raiz do projeto**

<pre class="terminal">
$ touch ~/projetos/meu_projeto/.rmvrc
</pre>

**Colocar a versão do ruby com a gemset específica**

<pre class="terminal">
$ echo "rvm use ree@meu_projeto" > ~/projects/seu_projeto/.rvmrc
</pre>

É isso ai, abraços;
