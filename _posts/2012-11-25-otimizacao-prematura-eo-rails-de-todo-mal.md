---
layout: post
title: Otimização prematura é o "Rails" de todo mal
---

Ontem o [DHH][dhh] fez [um tweet][1] criticanto [um post][2] do David Briant, onde ele propõe alguns refactorings usando o conceito de [Single Responsability Principle][srp]. O tweet do [DHH][dhh] gerou uma [série][3] de [tweets][4] e [discussões][6] em [resposta][5]. As discussões são pertinentes e certamente  serão cada vez mais comums na comunidade Rails esse tipo de discussão, principalmente se levarmos em consideração que somos uma comunidade crescente em aplicações e profissionais.

Entretanto discussões sobre [SOLID][solid], patterns de apresentação, [fast rails tests][7], e outras discussões técnicas, estão em evidência nos últimos tempos na comunidade e fazendo uma relação desses assuntos e o post do David Briant coloquei o título do post com uma alusão a famosa frase do [Donald Kuth][dk] que diz:

<blockquote>
  We should forget about small efficiencies, say about 97% of the time: <b>premature optimization is the root of all evil</b>. Yet we should not pass up our opportunities in that critical 3%. A good programmer will not be lulled into complacency by such reasoning, he will be wise to look carefully at the critical code; but only after that code has been identified.</blockquote>

Como falei, esses não são assuntos novos na nossa comunidade, pois sempre se falou de patterns, conceitos de [SOLID][solid] e outros assuntos como decorators, basta você procurar no google e verá artigos datados de 2007, 2008, até mesmo datas anteriores, a diferença é que existiam menos aplicações e menos profissionais escrevendo códigos em rails.

Acredito que David Briant tenha sido apenas infeliz no exemplo que ele usou, ou talvez teve a intensão de ser polêmico, mas na realidade são esses tipos de discussões que fazem a comunidade crescer e a justificativa do David é válida, pois quando ele cita a palestra do [@tenderlove][tl] e ele argumenta o seguinte:

<blockquote>
  I realize that Aaron’s code is just an example for a slide at a conference, but I can tell you from experience, that any time an authoritative source shows code to others, they take that as the “right way” to do things...
</blockquote>

O fato é que *["desenvolvedores ruins"][6]* sempre levam opiniões e ideias de desenvolvedores formadores de opinião como verdade absoluta gravada em pedra, e tomam suas suas decisões de design de código baseados nisso sem opinião própria, ou por falta de conhecimento ou por falta de curiosidade; E como exemplo claro na comunidade temos é o conceito de **"Thin Controller, Fat Model"**, que é mal interpretado.

Poderia ir além com esse assunto, mas a reflexão que quero deixar é que qualquer decisão tem ônus e deve ter algum embasamento. Remover um callback para uma classe de serviço com uma interface bem definida e dizer que vai evitar efeito colateral em uma aplicação feita durante um Rails Rumble que dura dois dias, é puro preciosismo.


[dhh]: https://twitter.com/dhh
[tl]: https://twitter.com/tenderlove
[dk]: http://en.wikipedia.org/wiki/Donald_Knuth
[srp]: http://en.wikipedia.org/wiki/Single_responsibility_principle
[solid]: http://en.wikipedia.org/wiki/SOLID

[1]: https://twitter.com/dhh/status/272446834595729409
[2]: http://www.naildrivin5.com/blog/2012/06/10/single-responsibility-principle-and-rails.html
[3]: https://twitter.com/rafaelfranca/status/272447970241286144
[4]: https://twitter.com/dhh/status/272456084369858560
[5]: https://twitter.com/dhh/status/272450403201867776
[6]: https://twitter.com/dhh/status/272460237997473793
[7]: http://www.youtube.com/watch?v=bNn6M2vqxHE
