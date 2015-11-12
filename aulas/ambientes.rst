2. Ambientes de desenvolvimento
===============================

2.1 - Ambiente básico
---------------------

2.1 - Sistemas Operacionais
~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Neste curso será adotado o sistema operacional GNU/Linux como plataforma básica de trabalho.
- Porém, o conteúdo do curso pode ser facilmente adaptado para outros sistemas, como é o caso do MacOSX.
- Se você usa Windows, recomendamos:
  - A criação de uma máquina virtual em GNU/Linux usando o Vagrant de acordo com a aula de `DevOps <devops.html>`_.
  - Ou o uso do Cygwin juntamente com seu editor de textos favorito.

2.1 - O essencial
~~~~~~~~~~~~~~~~~

Desktop sem distrações: o que é o mínimo que você precisa?

- Editor de texto ou IDE: produz código.
- Emulador de terminal: execução de tarefas.
- Navegador web: ambiente de teste.

Roteiro do screencast:

#. Exibir um desktop básico e limpo.
#. Discorrer sobre cores de fundo, teclas de atalho e abas de terminal e editor de texto.

2.1 - Editores
~~~~~~~~~~~~~~

- Vantagens dos IDEs (NetBeans, Eclipse, Aptana, etc):
  - Facilidade de uso.
  - Ambiente de desenvolvimento integrado.
- Vantagens dos editores de texto (Atom, Emacs, VIM, Notepad++, Gedit etc):
  - Simplicidade.
  - Performance.

Roteiro do screncast:

#. Abrir alguns editores de texto e IDEs e seus sites.

2.2 - Emulador de terminal
~~~~~~~~~~~~~~~~~~~~~~~~~~

- Despacha comandos textuais.
- Comandos podem ser automatizados em scripts.
- Comandos básicos de UNIX usados no curso.
- Atalhos do terminal (histórico de comandos, limpeza da tela e movimentos do cursor).
- Shells: bash, zsh, php, python, rvm, node, etc!

Roteiro do screencast:

::

  # Navegação
  pwd
  ls
  ls /
  ls ..
  ls ~
  cd
  cd -
  cd ..
  cd /

  # Criando e apagando arquivos e pastas
  touch arquivo
  mkdir pasta
  rm arquivo
  rmdir pasta

  # Movendo e copiando arquivos
  cp arquivo pasta
  mv pasta pasta.20151112
  rm arquivo

  # Criando atalhos
  ln pasta.20151112 pasta.latest
  ls -l

  # Procurando ajuda!
  man ls

  # Quem sou eu?
  whoami

  # Executando com permissões de superusuário
  sudo whoami

  # Instalando um programa
  sudo apt-get install git

2.3 - Fluxo de trabalho
-----------------------

2.3 - Básico
~~~~~~~~~~~~

- Diário de bordo: de um arquivo de texto a um blog sobre desenvolvimento (o próprio blogático, no nosso caso!).
- Organização de pastas.
- Backups.

Roteiro do screencast:

::

  # Criando uma pasta para projetos
  mkdir ~/projetos

  # Criando a pasta do nosso projeto
  mkdir ~/projetos/blogatico

2.3 - Arquivos básicos
~~~~~~~~~~~~~~~~~~~~~~

* README: em Markdown (.md), reStructuredText (.rst), texto simples (.txt), etc.
* ChangeLog: opcional e pode ser gerado automaticamente.
* Makefile ou outro arquivo dependendo do método de construção do software (Rakefile, setup.py, etc).

Roteiro do screencast:

::

    # Criando a estrutura básica do seu projeto
    cd ~/projetos/blogatico
    touch README.md ChangeLog TODO.md

2.3 - Sistemas de tickets (tarefas)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Kanban.
* Arquivo TODO em formatos plaintext, Markdown, etc.
* Um arquivo por tarefa em pastas `open` e `closed`.
* Taskwarrior ou similar.
* Aplicação própria (Trac, etc)
* TODOs and FIXMEs ao longo do código (em última instância).

Roteiro do screncast:

::

    gedit README.md TODO.md

Imagens:

* Diversos sistemas de tickets.

2.3 - Scripts e templates
~~~~~~~~~~~~~~~~~~~~~~~~~

- Configurações, scripts e atalhos de produtividade.
- Templates de desenvolvimento.
- Balanço:

  * Customizações deixam os ambientes sob medida.
  * Porém tem um custo de criação e de manutenção.
  * Existem customizações disponíveis e prontas para uso.

Roteiro do screencast:

::

  # Criando um script!
  mkdir bin
  touch bin/build

  # Não funciona sem permissão de execução!
  ./bin/build

  # Agora vai!
  chmod +x bin/build
  ./bin/build

  gedit bin/build

2.4 - Atividades
----------------

#. Teste diversos editores de textos e IDEs disponíveis para sua plataforma de desenvolvimento. Avalie cada um deles em termos de performance, funcionalidades, facilidade de uso e adaptação. A preferência pela plataforma de desenvolvimento varia muito de pessoa para pessoa: tente descobrir a sua!

#. Crie a prática de avaliar seu fluxo de trabalho e identificar o que mais lhe incomoda: pode ser aquela tecla de atalho incômoda ou mesmo a falta de uma tecla de atalho para uma dada operação. Pode ser a falta de um script para automatizar tarefas repetitivas ou qualquer coisa que tira transfere a concentração do seu trabalho para tarefas operacionais. Como você poderia resolver o problema?

#. Crie uma pasta para o seu projeto.

#. Hora de programar!

Referências
-----------

- `Atom <https://atom.io/>`_.
- `Lime Text Editor <http://limetext.org/>`_.
