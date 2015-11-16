7. Quando (não) reinventar a roda
=================================

7.1 - Patterns
--------------

* Separando código de dados, sobretudo dados sigilosos!
* Desacoplamento.
* Filosofia UNIX:
  * Pequenos softwares/bibliotecas.
  * Que fazem uma coisa bem.
  * E que podem ser facilmente combinados.

7.2 - Antipatterns
------------------

* Hype: cuidado com o ciclo dos modismos!
* Linearidade: o mito da pessoa-mês (Lei de Brooks).
* Inferno de dependências.
* Bitrot: decaimento natural do código!

7.3 - Inventando, reinventando e desinventando
----------------------------------------------

Hora de converter nosso projeto blogático para uma plataforma com mais funcionalidades!

Roteiro do screencast:

::

  cd ~/projetos/blogatico
  cp -r ../boaspraticas/_templates/ikiwiki/* .
  make

7.4 - Documentação: lendo e escrevendo
--------------------------------------

* Quanto mais próxima a documentação está do código, mais difícil dela se desatualizar.
* Docblocs / heredocs.

Roteiro do screencast:

::

  sudo apt-get install ttyrec

7.5 - Atividades
----------------

7.6 - Referências
-----------------

* `Versionamento Semântico 2.0.0 <http://semver.org/lang/pt-BR/>`_.
