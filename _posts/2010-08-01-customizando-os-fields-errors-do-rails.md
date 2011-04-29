--- 
layout: post
title: Customizando os Fields Errors do Rails
categories: rubyonrails, dica, ruby, rails
enki_id: 6
---

Quem desenvolve com **[Ruby on Rails](http://rubyonrails.org/)**, sabe que esta é uma ferramenta muito poderosa para desenvolvimento web. Mas como todo framework, que te fornece uma estrutura básica, e a partir dai faz as customizações necessárias, que por sinal é tão simples como o uso do framework.

Uma necessidade comum é adaptar o formato de saída das mensagens de erro das validações de formulários, para o estilo de cada projeto.

O padrão gerado pelo **Rails** é como o a seguir:

<img src="http://farm5.static.flickr.com/4125/4846589232_64d788ea98.jpg" width="435" height="402" alt="Default error message" title="default error message" />

Porém, é necessério adaptá-lo para um formato que atenda a necessidade do seu projeto e isto é muito muito simples, veja no exemplo abaixo já alterado.

<img src="http://farm5.static.flickr.com/4145/4846589304_dfd006acec.jpg" width="500" height="333" alt="custom error message" title="custom error message"/>

Interessante não?
A mensagem é exibida ao lado do *label* do campo, e a borda do campo fica marca na cor vermelha. E o melhor de tudo é que é muito simples de se fazer esta alteração. 
No arquivo **config/enviroment.rb**, vá até o final do arquivo e adicione este trecho de código.

<script src="http://gist.github.com/479961.js"> </script> 

Para que tudo funcione corretamente, você precisa da gem **[Hpricot](http://github.com/hpricot/hpricot)** que é um parser **html**, que utilizaremos para fazer a busca no **html** gerado pelo rails para inserir dinâmicamente o css.

Já o css fica por sua conta, eu mantive os gerados pelo **Rails**.

**[UPDATE]**

Como o **[Caike](http://twitter.com/caike)** falou no comentário, uma outra forma de customizar os Fields Errors, é herdando o **ActionView::Helpers::FormBuilder**, assim você tem acesso ao model em questão para verificar a existência de erros e fazer as adaptações necessárias.
Mediante esta dica, resolvi fazer esta implementação para comparar as diferenças, vejamos então.

No diretório **lib** da sua aplicação crie um arquivo ruby, eu o chamei de **lib/customized_error_form_builder.rb**, e adicione o código a seguir:

<script src="http://gist.github.com/503552.js"> </script>

O próximo passo é fazer o seu form usar o **FormBuilder** customizado, e para isso existem duas formas.

Uma delas é adicionando ao seu  **config/enviroment.rb**  o código a seguir, e notem que eu comentei as linhas anteriormente adicionadas.

<script src="http://gist.github.com/503566.js"> </script>

Fazendo da forma acima todos os formulários da aplicação farão uso do seu **FormBuilder** customizado, porém se quiser que apenas um formulário específico faça uso dele, desconsidere o código acima e apenas adicione ao seu **form_for** o builder, veja como ficaria seu form:

<script src="http://gist.github.com/503571.js"> </script>

Após executar a aplicação é possível reparar que o resultado é o mesmo da primeira custimozação feita neste post, porém a quantidade de código escrito é muito maior e não cobre todas as situações, se repararmos no nosso arquivo **lib/customized_error_form_builder.rb** ele implementa apenas os método para label e text_field, não cobrindo outros campos do **form_for**.

Particularmente **e** para este tipo de situação eu utilizaria a primeira implementação, porém, é importante conhecer melhor sobre **ActionView::Helpers::FormBuilder**, pois pode ser útil para seus projetos ou da sua empresa, no caso de ter uma implementação própria para os formulários dos seus projetos. A gem **[formtastic](http://github.com/justinfrench/formtastic)** é um exemplo de onde a herança do  **ActionView::Helpers::FormBuilder** foi aplicada para ter um melhor resultado.


Até, mais e abraços;
