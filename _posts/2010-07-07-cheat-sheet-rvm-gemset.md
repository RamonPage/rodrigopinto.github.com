--- 
layout: post
title: "[Cheat Sheet] RVM +Gemset"
---

Após fazer uma "limpeza" no meu ambiente ruby utilizando o **[RVM](http://rvm.beginrescueend.com/rvm/)** que Ã?Â© um  gerenciador de **rubies**  e a **[Gemset](http://rvm.beginrescueend.com/gemsets/)** que o gerenciador de diretórios de gems do **RVM**. 
Resolvi deixar aqui um cheat sheet para facilitar que for utilizar o  **[RVM + Gemset](http://rvm.beginrescueend.com/)**. 
Então delicie-se com essa maravilha, que só não é 100% porque não faz café. ;p

Para fazer a instalação do **RVM** confira em **[RVM install](http://rvm.beginrescueend.com/rvm/install/)**, após finalizar a instalação divirta-se com as dicas abaixo.

###Instalando uma versão do ruby no RVM

rvm install <versão-ruby>
	
ex: rvm install 1.8.7, ree

###Definindo a versão do ruby

rvm <versão-ruby>
	
ex: rvm ree

###Definindo uma versão default do ruby no RVM

rvm --default <versão-ruby>

ex: rvm --default 1.8.7

###Trocando a versão do ruby do RVM  para o ruby do seu sistema

rvm system

###Listando seus **rubies** instaladas via RVM

rvm list

###Verificando a Gemset atual

rvm gemdir

###Criando uma Gemset

rvm gemset create *<nome>*

ex: rvm gemset create meu_projeto

###Definindo uma versão do ruby e uma Gemset específica para um projeto

**Criar  um arquivo .rvmrc na raiz do projeto**

ex:  touch ~/projetos/meu_projeto/.rmvrc

**Colocar a versão do ruby com a gemset específica**

echo "rvm use ree@meu_projeto" > ~/projects/seu_projeto/.rvmrc


É isso ai,
Abraços;
