2. Ambientes de desenvolvimento
===============================

- Neste curso será adotado o sistema operacional GNU/Linux como plataforma básica de trabalho.
- Porém, o conteúdo do curso pode ser facilmente adaptado para outros sistemas, como é o caso do MacOSX.
- Se você usa Windows, recomendamos:
  - A criação de uma máquina virtual em GNU/Linux usando o Vagrant de acordo com a aula de `DevOps <devops.html>`_.
  - Ou o uso do Cygwin juntamente com seu editor de textos favorito.

2.1 - Ambiente básico e a guerra dos editores de texto
------------------------------------------------------

2.1 - Ambiente básico
~~~~~~~~~~~~~~~~~~~~~

- Desktop sem distrações: o que é o mínimo que você precisa?
- Editor de texto ou IDE: produz código.
- Emulador de terminal: execução de tarefas.
- Navegador web: ambiente de teste.

2.1 - Editores
~~~~~~~~~~~~~~

- Vantagens dos IDEs (NetBeans, Eclipse, Aptana, etc):
  - Facilidade de uso.
  - Ambiente de desenvolvimento integrado.
- Vantagens dos editores de texto (Atom, Emacs, VIM, Notepad++, gedit etc):
  - Simplicidade.
  - Performance.

2.2 - Emulador de terminal
~~~~~~~~~~~~~~~~~~~~~~~~~~

- Despacha comandos para sistemas.
- Comandos podem ser automatizados.

2.3 - Fluxo de trabalho
~~~~~~~~~~~~~~~~~~~~~~~

- Diário de bordo: de um arquivo de texto a um blog sobre desenvolvimento.
- Organização de pastas.
- Backups.

Roteiro do screencast:

::

    # Criando uma pasta para projetos
    mkdir ~/projetos

    # Criando a pasta do nosso projeto
    mkdir ~/projetos/blogatico

    # Criando a estrutura básica do seu projeto
    cd ~/projetos/blogatico
    touch README.md ChangeLog TODO.md

2.4 - Scripts e templates
-------------------------

- Configurações, scripts e atalhos de produtividade.
- Templates de desenvolvimento.
- Balanço:

  * Customizações deixam os ambientes sob medida.
  * Porém tem um custo de criação e de manutenção.
  * Existem customizações disponíveis e prontas para uso.

2.5 - Atividades
----------------

#. Teste diversos editores de textos e IDEs disponíveis para sua plataforma de desenvolvimento. Avalie cada um deles em termos de performance, funcionalidades, facilidade de uso e adaptação. A preferência pela plataforma de desenvolvimento varia muito de pessoa para pessoa: tente descobrir a sua!

#. Crie a prática de avaliar seu fluxo de trabalho e identificar o que mais lhe incomoda: pode ser aquela tecla de atalho incômoda ou mesmo a falta de uma tecla de atalho para uma dada operação. Pode ser a falta de um script para automatizar tarefas repetitivas ou qualquer coisa que tira transfere a concentração do seu trabalho para tarefas operacionais. Como você poderia resolver o problema?

#. Crie uma pasta para o seu projeto.

#. Hora de programar!

Referências
-----------

- `Atom <https://atom.io/>`_.
- `Lime Text Editor <http://limetext.org/>`_.
