7. Quando (não) reinventar a roda
=================================

7.1 - Patterns
--------------

7.1 - O que são e por quê usar?
-------------------------------

* Design Patterns são "formas" de desenvolvimento reutilizáveis e consideradas como boas práticas.
* A lista de patterns conhecidos é long demais para este curso
* Daremos alguns exemplos ilustrativos que atendem o nosso critério de simplicidade.
* São recomendações! Mais importante que usá-las é ter capacidade crítica para determinar quais fazem ou não sentido para o seu projeto.

7.2 - Exemplos
--------------

Daremos breves exemplos em três campos:

* Design: separação de código de dados, sobretudo dados sigilosos!
* Metodologia : DDD e TDD: documentar e testar antes, durante ou depois?
* Implementação: Filosofia UNIX:
  * Pequenos softwares e bibliotecas (desacoplamento).
  * Que fazem bem uma coisa.
  * E que podem ser facilmente combinados.

7.2 - Anti-patterns
-------------------

São o oposto das design patterns: formas de desenvolvimento não recomendadas. Exemplos:

* O mito da pessoa-mês (Lei de Brooks).
* Hype: cuidado com o ciclo dos modismos!
* Inferno de dependências.
* Bitrot: decaimento natural do código!

7.3 - Documentação: lendo e escrevendo
--------------------------------------

* Documente não só para os outros, mas para você mesmo(a) no futuro.
* Quanto mais próxima a documentação está do código, mais difícil dela se desatualizar.
* Docblocks / heredocs: podem ser convertidos em documentação indexada, referenciada e navegável.
* Documente procedimentos enquanto você os realiza.

Roteiro do screencast:

* Concluindo a documentação do blogático, fazendo um commit e um release tag.

7.4 - Inventando, reinventando e desinventando
----------------------------------------------

* Caso tenha acompanhado este curso desde o começo e construiu nosso projeto/invento "blogático" desde o ínicio, agora você tem um software para documentar seu aprendizado em desenvolvimento. Acontece que ele é bem simples. E se você quiser algo mais completo e que seja uma solução pronta, já disponível?

* Agora é hora de converter nosso projeto blogático para uma plataforma com mais funcionalidades!

Roteiro do screencast:

::

  cd ~/projetos/blogatico
  cp -r ../boaspraticas/_templates/ikiwiki/* .
  make

7.5 - Atividades
----------------

#. Consulte as referências por diversos design patterns e antipatterns. Quais patterns você acha mais interessantes? Quais antipatterns são mais perigosos?
#. Crie a documentação do seu projeto. Pense que ela será lida por uma audiência bem geral que nunca ouviu falar do projeto e será determinante para que decidam se irão usá-lo ou não.

7.6 - Referências
-----------------

* Imagens usadas nos vídeos?
* `Versionamento Semântico 2.0.0 <http://semver.org/lang/pt-BR/>`_.
* `On Documentation-Driven Development // Collective Idea | Crafting web and mobile software based in Holland, Michigan <http://collectiveidea.com/blog/archives/2014/04/21/on-documentation-driven-development/>`_.
* `Readme Driven Development <http://tom.preston-werner.com/2010/08/23/readme-driven-development.html>`_.
* https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design
* `From 10x programmer to 0.1x programmer: creating more with less · Code Without Rules <https://codewithoutrules.com/2016/08/25/the-01x-programmer/>`_.
