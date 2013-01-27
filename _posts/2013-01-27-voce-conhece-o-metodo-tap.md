---
layout: post
title: "Você conhece o método tap?"
date_pt_BR: 27 Jan 2013
categories:
---

O Ruby 2.0 está para sair do forno, em fevereiro, mas ainda tem muita gente que não conhece o método _[Object#tap][tap]_ introduzido no ruby 1.9.

O método _[Object#tap][tap]_ recebe um bloco por parâmetro e passa o objeto _corrente_ para dentro do bloco, e assim que o bloco finalizar a execução, o método retornará o objeto.

<script src="https://gist.github.com/4650576.js"></script>

Você também pode conferir com um exemplo de um array, onde usamo o método tap para executar o cálculo do _quadrado_ dos valores do array e ainda sim martermos o array com os valores originais.

<script src="https://gist.github.com/4650596.js"></script>

[tap]: http://ruby-doc.org/core-1.9.3/Object.html#method-i-tap