4. Controle de versão e social coding
=====================================

4.1 - O que é? Pra que serve?
-----------------------------

* Salvar o estado do código em revisões sequenciais.
* Integrar o trabalho do time.
* Acompanhar as mudanças no código (encontrar bugs, rollback, etc).
* Ajuda, mas não resolve conflitos na edição de arquivos.
* Boa prática: versionando desde o dia 0.

Imagens:

* https://git-scm.com/book/en/v2/book/01-introduction/images/local.png

4.2 - Sistemas de controle de versão
------------------------------------

4.2 - Quais sistemas existem?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Tópicos:

* RCS (pré-histórico).
* CVS (roots, centralizado).
* Subversion (svn) (tradicional, centralizado).
* Mercurial (hg), Monotone (mtn), Bazaar (bzr), Darcs, Git (modernos, distribuídos).

Imagens:

* Ícones e screenshots do site de cada sistema.

4.2 - Centralizados versus distribuídos
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Tópicos:

* Centralizadaso:

  * Repositório central para onde são enviadas mudanças.
  * Ou seja, existe uma cópia de referência.

* Distribuídos:

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

4.3 - Instalando e configurando
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Focaremos em git pela linha de comando.
* Disponível em tudo que é tipo de sistema operacional.
* A única exigência é especificar um nome e email (de preferência funcional ;) para constar nas informações de revisão.

Roteiro do screencast:

::

  sudo apt-get install git
  git config --global user.name  "Meu Nome"
  git config --global user.email "meu@email.tld"

4.3 - Repositórios
~~~~~~~~~~~~~~~~~~

* Repositórios: "pastas geridas pelo git".
* Pasta ".git" criada no repositório: não polui seu projeto.

Roteiro do screencast:

::

  # Adicionando nosso projeto no git
  cd ~/projetos/blogatico
  git init

  # Clonando um projeto existente
  cd ~/projetos/
  git clone https://github.com/rhatto/boaspraticas

4.4 - Trabalhando no projeto
----------------------------

4.4 - Trabalhando no projeto
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Três estágios de mudanças: cometidas (commited), marcadas para commit (staged) e modificadas (changed).

Roteiro do screencast:

::

  cd ~/projetos/blogatico
  git status
  git add README.md
  git status
  gedit README.md
  git status
  git diff
  git commit -m "Primeira revisão"
  git add README.md # mudanças recentes adicionadas ao estágio de lançamento
  git commit -m "Segunda revisão"
  git add .
  git commit -m "Adiciona demais arquivos" # coloca todas as mudanças no estágio e comete

Imagens:

* https://git-scm.com/book/en/v2/book/01-introduction/images/areas.png

4.4 - Log de revisões
~~~~~~~~~~~~~~~~~~~~~

* Árvore de histórico do repositório.
* Cada "revisão" do histórico representa um estado do repositório (snapshot).
* ID da revisão: hash SHA-1.

Roteiro do screencast:

::

  cd ~/projetos/blogatico
  git log
  sudo apt-get install gitk
  gitk

Imagens:

* https://git-cola.github.io/images/screenshot-main-linux.png
* https://static.lwn.net/images/ns/kernel/gitk.png

4.4 - Interface gráfica
~~~~~~~~~~~~~~~~~~~~~~~

Roteiro do screencast:

::

  sudo apt-get install git-cola
  git cola

4.5 - Ramificações (branches e merges)
--------------------------------------

* Existem vários "ramos" na história de um software.
* Os ramos, ou branches, divergem e convergem.
* A convergência nem sempre é suave, porém o git auxilia com várias estratégias.

Roteiro do screencast:

::

  cd ~/projetos/blogatico
  git branch develop
  git checkout develop
  git commit -a
  git checkout master
  git merge develop

4.6 - Usando o git-flow
-----------------------

* O git-flow é um plugin para o git.
* Ele força um fluxo de trabalho integrado.
* Branches básicos (nomes podem ser customizados):

  * master: branch principal com o código que é submetido para a produção.
  * develop: branch de desenvolvimento onde funcionalidades são integradas e seu conjunto testado.
  * features/: prefixo para branches onde funcionalidades são desenvolvidas.
  * hotfix/: prefixo para branches de correções rápidas (bugfixes).

Roteiro do screencast:

::

  cd ~/projetos/blogatico
  git flow init
  git flow feature start doc
  git commit -a
  git flow feature finish

4.7 - Submódulos
----------------

* Um repositório git dentro de outro.
* "Trava" o submódulo em revisões específicas.
* "Sistema" de gestão de dependências de código simples e integrado ao git.

Roteiro do screencast:

::

  # No repositorio
  cd ~/projetos/blogatico
  git submodule add https://github.com/dhg/Skeleton skeleton
  git commit -a -m "Adiciona skeleton"

  # Clonando o repositorio noutro local
  cd ..
  git clone blogatico blogatico-clonado
  cd blogatico-clonado
  git submodule update --init

  # Ou:
  cd ..
  git clone --recursive projeto projeto-clonado

4.8 - Social coding (gitlab, github, etc)
-----------------------------------------

4.9 - Github: criando e forkando um projeto
-------------------------------------------

4.10 - Github: fazendo um pull request
--------------------------------------

4.11 - Atividades
-----------------

#. Instale o git.
#. Crie uma conta do `Github <https://github.com>`_ ou no `Gitlab <https://gitlab.com>`_.
#. Faça um pequeno site com o Skeleton.
#. Bônus: git log to ChangeLog!

4.12 - Referências
------------------

* `Instalando Git <https://git-scm.com/book/pt-br/v1/Primeiros-passos-Instalando-Git>`_.
* `Curso Básico de Git - RBtech <https://www.youtube.com/watch?v=WVLhm1AMeYE&list=PLInBAd9OZCzzHBJjLFZzRl6DgUmOeG3H0>`_.
* `cheatsheet do git-flow <https://danielkummer.github.io/git-flow-cheatsheet/index.pt_BR.html>`_.
* `Skeleton: Responsive CSS Boilerplate <http://getskeleton.com/>`_
* `git-cola: The highly caffeinated Git GUI <https://git-cola.github.io/>`_
