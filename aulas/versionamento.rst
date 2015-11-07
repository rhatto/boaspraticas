4. Controle de versão e social coding
=====================================

4.1 - O que é? Pra que serve?
-----------------------------

Tópicos:

* Salvar o estado do código em revisões sequenciais.
* Integrar o trabalho do time.
* Acompanhar as mudanças no código (encontrar bugs, rollback, etc).
* Boa prática: versionando desde o dia 0.
* Ajuda, mas não resolve conflitos na edição de arquivos.

Imagens:

* https://git-scm.com/book/en/v2/book/01-introduction/images/local.png

4.2 - Quais sistemas existem?
-----------------------------

Tópicos:

* RCS (pré-histórico).
* CVS (roots, centralizado).
* Subversion (svn) (tradicional, centralizado).
* Mercurial (hg), Monotone (mtn), Bazaar (bzr), Darcs, Git (modernos, distribuídos).

Imagens:

* Ícones e screenshots do site de cada sistema.

4.2 - Centralizados versus distribuídos
---------------------------------------

Tópicos:

* Centralizado:

  * Repositório central para onde são enviadas mudanças.
  * Ou seja, existe uma cópia de referência.

* Distribuído:

  * Cada cópia de trabalho é um repositório completo e possui todo o histórico de revisões (também uma forma de backup).
  * Não requer um repositório central, porém um ponto de trocas central pode ser estipulado entre os desenvolvedores/as.

Imagens:

* Centralizado: http://phillihp.com/wp-content/uploads/2012/06/scm.png
* Distribuído: https://git-scm.com/book/en/v2/book/01-introduction/images/distributed.png

4.3 - Git: introdução
---------------------

4.3 - Características
~~~~~~~~~~~~~~~~~~~~~

* Desenvolvido inicialmente por Linus Torvalds.
* É o mais popular e difundido.
* Complexo e poderoso, porém pode ser usado de modo simples.
* Checagem de integridade nativa!

4.3 - Instalando
~~~~~~~~~~~~~~~~

* Focaremos em git pela linha de comando.
* Disponível em tudo que é tipo de sistema operacional.

4.3 - Configurando
~~~~~~~~~~~~~~~~~~

A única exigência é especificar um nome e email (de preferência funcional ;)
ara constar nas informações de revisão.

::

  git config --global user.name  "Seu Nome"
  git config --global user.email "seu@email"

4.3 - Repositórios
~~~~~~~~~~~~~~~~~~

* Repositórios: "pastas geridas pelo git".
* Iniciando um projeto no git:

::

    mkdir projeto
    cd projeto
    git init

* Pasta ".git" criada no repositório: não polui seu projeto.

4.3 - Trabalhando no projeto
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Três estágios de mudanças: cometidas (commited), marcadas para commit (staged) e modificadas (changed).

::

    atom README.md    # edite seu arquivo
    git status
    git add README.md # em seguida edite mais um pouco
    git status
    git diff
    git commit -m "Primeira revisão"
    git add README.md # mudanças recentes adicionadas ao estágio de lançamento
    git commit -m "Segunda revisão"
    git commit -a -m "Terceira revisão" # coloca todas as mudanças no estágio e comete

Imagens:

* https://git-scm.com/book/en/v2/book/01-introduction/images/areas.png

4.4 - Git: navegando no histórico
---------------------------------

4.4 - Log de revisões
~~~~~~~~~~~~~~~~~~~~~

* Árvore de histórico do repositório.
* Cada "revisão" do histórico representa um estado do repositório (snapshot).
* ID da revisão: hash SHA-1.

::

    git log
    git cola
    gitk

Imagens:

* https://git-cola.github.io/images/screenshot-main-linux.png
* https://static.lwn.net/images/ns/kernel/gitk.png

4.4 - Revertendo uma mudança
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Você pode fazer um novo commit na unha ou usar o ferramental do git.

::

    git commit --amend
    git revert
    git rebase

4.5 - Ramificações (branches e merges)
--------------------------------------

4.6 - Usando o git-flow
-----------------------

4.7 - Submódulos
----------------

* Um repositório git dentro de outro.
* Trava em revisões específicas.
* "Sistema de empacotamento" simples e integrado ao git.

4.8 - Social coding (gitlab, github, etc)
-----------------------------------------

4.9 - Github: criando e forkando um projeto
-------------------------------------------

4.10 - Github: fazendo um pull request
--------------------------------------

4.11 - Github: sistema de tickets
---------------------------------

4.12 - Atividades
-----------------

#. Instale o git.
#. Crie uma conta do `Github <https://github.com>`_ ou no `Gitlab <https://gitlab.com>`_.
#. Faça um pequeno site com o Skeleton.

Referências
-----------

* `cheatsheet do git-flow <https://danielkummer.github.io/git-flow-cheatsheet/index.pt_BR.html>`_.
* `Skeleton: Responsive CSS Boilerplate <http://getskeleton.com/>`_
* `Versionamento Semântico 2.0.0 <http://semver.org/lang/pt-BR/>`_.
* `Curso Básico de Git - RBtech <https://www.youtube.com/watch?v=WVLhm1AMeYE&list=PLInBAd9OZCzzHBJjLFZzRl6DgUmOeG3H0>`_.
* `Instalando Git <https://git-scm.com/book/pt-br/v1/Primeiros-passos-Instalando-Git>`_.
* `git-cola: The highly caffeinated Git GUI <https://git-cola.github.io/>`_
