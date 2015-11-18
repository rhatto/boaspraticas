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

2.2 - Adote o GNU/Linux
~~~~~~~~~~~~~~~~~~~~~~~

* Além de ser livre, o GNU/Linux é um ambiente natural para desenvolvimento.
* Você não precisa largar de vez seu sistema operacional. Vá aos poucos, começando com uma imagem live.
* Sugestões: Debian GNU Linux e Ubuntu.

2.1 - O essencial
~~~~~~~~~~~~~~~~~

Desktop sem distrações: o que é o mínimo que você precisa? No nosso caso, usaremos basicamente:

- Editor de texto ou IDE: produz código.
- Emulador de terminal: execução de tarefas.
- Navegador web: ambiente de teste.

Roteiro do screencast:

#. Exibir um desktop básico e limpo.
#. Discorrer sobre cores de fundo, teclas de atalho, abas de terminal e editor de texto, layouts de janela, etc.

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
--------------------------

2.2 - O que é?
~~~~~~~~~~~~~~

- Despacha comandos textuais.
- Comandos podem ser automatizados em scripts.
- Comandos básicos de UNIX usados no curso.
- Atalhos do terminal (histórico de comandos, limpeza da tela e movimentos do cursor).
- Shells: bash, zsh, php, python, irb, nodejs, etc!

Roteiro do screencast:

#. Mostrar entrada de comandos no terminal.
#. Mostrar outros shells.

2.2 - Comandos básicos: navegação
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Roteiro do screencast:

::

  # Sintaxe de comandos
  comando [opcoes] <argumento-obrigatorio> [argumento-opcional]

  # Navegação
  pwd
  cd ..
  pwd
  cd
  cd /
  cd -

2.2 - Comandos básicos: arquivos e pastas
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Roteiro do screencast:

::

  # Criando e apagando arquivos e pastas
  touch arquivo
  mkdir pasta

  # Listando pastas
  ls
  ls /
  ls ..
  ls ~

  # Movendo e copiando arquivos
  cp arquivo pasta
  mv pasta pasta.20151112

  # Criando atalhos
  ln pasta.20151112 pasta.latest
  ls -l

  # Apagando arquivos e pastas
  rm arquivo
  rm pasta.20151112
  rm -r pasta.20151112
  ls -l
  rm pasta.latest

2.2 - Comandos básicos: dominando o sistema!
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Roteiro do screencast:

::

  # Quem sou eu?
  whoami

  # Executando com permissões de superusuário
  sudo whoami

  # Instalando um programa
  sudo apt-get install tree

  # Sistema de arquivos
  tree
  tree /
  tree -d /

  # Entrada e saida padrao
  tree -d / > saida.log
  less saida.log

  # Dutos
  tree -d / | less

  # Processos
  ps
  ps -A
  pstree | less

  # Procurando ajuda!
  man ls

2.3 - Fluxo de trabalho
-----------------------

2.3 - Básico
~~~~~~~~~~~~

- Seu desktop funciona como uma bancada de trabalho: mantenha-o sempre arrumado, limpando a sujeira toda a vez que finalizar uma tarefa.
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

* README: em Markdown (.md ou .mdwn), reStructuredText (.rst), texto simples (.txt), etc.
* ChangeLog: opcional e pode ser gerado automaticamente.
* Makefile ou outro arquivo dependendo do método de construção do software (Rakefile, setup.py, etc).

Roteiro do screencast:

::

  # Criando a estrutura básica do seu projeto
  cd ~/projetos/blogatico
  touch README.mdwn ChangeLog TODO.mdwn
  gedit README.mdwn

2.3 - Markdown e texto estruturado
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Convenções de formatação para arquivos de texto simples.
* Podem ser facilmente convertidos para outros formatos (html, pdf, epub, por exemplo).

2.3 - Gestão de tarefas (tickets)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Kanban.
* Arquivo TODO em formatos plaintext, Markdown, etc.
* Taskwarrior ou similar.
* Aplicação própria (Trac, etc)
* TODOs and FIXMEs ao longo do código (em última instância).

Roteiro do screncast:

::

  gedit TODO.mdwn

Imagens:

* Diversos sistemas de tickets.
* https://en.wikipedia.org/wiki/Kanban_board#/media/File:Simple-kanban-board-.jpg

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
  touch blogatico

  # Não funciona sem permissão de execução!
  exec blogatico

  # Agora vai!
  chmod +x blogatico
  exec blogatico
  ./blogatico

  # Editando
  gedit blogatico

  # Criando o conteúdo inicial
  mkdir data
  gedit data/index.mdwn

  # Testando!
  blogatico

2.4 - Atividades
----------------

#. Teste diversos editores de textos e IDEs disponíveis para sua plataforma de desenvolvimento. Avalie cada um deles em termos de performance, funcionalidades, facilidade de uso e adaptação. A preferência pela plataforma de desenvolvimento varia muito de pessoa para pessoa: tente descobrir a sua!

#. Crie a prática de avaliar seu fluxo de trabalho e identificar o que mais lhe incomoda: pode ser aquela tecla de atalho incômoda ou mesmo a falta de uma tecla de atalho para uma dada operação. Pode ser a falta de um script para automatizar tarefas repetitivas ou qualquer coisa que tira transfere a concentração do seu trabalho para tarefas operacionais. Como você poderia resolver o problema?

#. Crie a estrutura básica do seu projeto.

2.5 - Referências
-----------------

- `Guia Foca Linux <http://www.guiafoca.org/>`_.
- `Solarized - Ethan Schoonover <http://ethanschoonover.com/solarized>`_.
