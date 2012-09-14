--- 
layout: post
title: Testando Factories para manter a sanidade
---

Quem usa [FactoryGirl][fg] para testar aplicações, provavelmente já passou pela situação de adicionar uma validação nova em um model e quebrar boa parte do testes, e a primeira reação é FUUUUU!!!. As vezes você atenta e descobre rápido que era uma simples factory que deixou de ser válida, por não está de acordo com a nova validação, mas as vezes não, e você demora a entender e perde um tempo pra resolver isso. 

Para evitar o susto e manter a sanidade, nada mais justo que testar suas factories.<br/>
Como assim? Isso mesmo, adicionar uma spec que teste sua factory, para verificar se a mesma continua válida. 

<script src="https://gist.github.com/3718550.js?file=my_model_spec.rb"></script>

Porém, quando você tem um sistema com muitos models, escrever esse mesmo código para cada um dos seus models gerará duplicação de código e deixará seus testes mais lentos. Uma alternativa é criar uma spec que execute somente os testes  das factories, ou seja, criar uma spec para as testar as factories, ex: __spec/factories_spec.rb__

<script src="https://gist.github.com/3718550.js?file=factories_spec.rb"></script>

Fácil, não? Agora sempre que você rodar seus testes você terá uma spec que verifica se suas factories continuam válidas. 

Outa dica legal é o fail fast. Na situação em que se usa o comando __rake__ para rodar os testes, você pode adicionar uma rake task para rodar a __spec/factories_spec.rb__ antes da sua suíte de teste, e o rake somente irá rodar sua suíte de teste, se a __spec/factories_spec.rb__ estiver passando.

<script src="https://gist.github.com/3718550.js?file=Rakefile"></script>

Interessante, não? Comecei usar essa semana depois que li [esse post][post], e adotarei para todos os projetos.

[fg]: https://github.com/thoughtbot/factory_girl
[post]: http://robots.thoughtbot.com/post/30994874643/testing-your-factories-first
