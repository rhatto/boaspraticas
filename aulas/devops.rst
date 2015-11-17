5. DevOps: desenvolvendo e orquestrando
=======================================

5.1 - O que é DevOps
--------------------

* Aproximação da administração de sistemas (sysadmin) com o desenvolvimento.
* Entregas constantes em ambientes de alta disponibilidade.
* Foco na automação.

Imagens:

* https://upload.wikimedia.org/wikipedia/commons/b/b5/Devops.svg

5.2 Ambientes reprodutíveis
---------------------------

5.2 - Ambientes
~~~~~~~~~~~~~~~

* Um software depende do seu ambiente para funcionar.
* Se o ambiente muda, o software pode parar de operar corretamente.
* O primeiro princípio DevOps é manter um ambiente de hospedagem reprodutível.

5.2 - Reprodutibilidade
~~~~~~~~~~~~~~~~~~~~~~~

* Automação básica para criar um ambiente de hospedagem a partir de elementos básicos: máquinas virtuais, repositório do código, etc.
* Provision (provisionamento): criação do ambiente de hospedagem.
* Deploy (disponibilização): envio do software para o ambiente.

5.2 - Estágios
~~~~~~~~~~~~~~

No caso de uma arquitetura de serviços, temos os seguintes ambientes:

* Desenvolvimento: em geral na máquina do(a) desenvolvedor(a).
* Testes e estágio (staging): onde versões do software são hospedadas antes de irem ao ar.
* Produção: onde o software está realmente hospedado.

5.3 - Máquinas virtuais
-----------------------

5.3 - Paradigmas
~~~~~~~~~~~~~~~~

* Um computador é uma máquina de Turing, podendo simular qualquer máquina, inclusive uma máquina de Turing.
* Uma máquina virtual é basicamente um software simulando o comportamento parcial ou integral de um computador.

5.3 - Implementações
--------------------

* Contêiners: chroot, Linux-VServer, OpenVZ, docker.
* Paravirtualizadores: Xen.
* Virtualizadores: KVM, VirtualBox.
* Gestores de nuvem: OpenStack.

5.4 - Vagrant
-------------

Roteiro do screencast:

::

  # Instalando o vagrant
  sudo apt-get install vagrant

  cd ~/projetos/blogatico
  vagrant init

5.5 - Integração contínua
-------------------------

- Integração contínua usando o `Travis CI <http://travis-ci.org/>`_.

5.6 - Fazendo o deploy
----------------------

- SSH e rsync.
- Deploy via git.

5.7 Atividades
--------------

#. Instale o vagrant.
#. Crie uma máquina virtual para desenvolver o seu projeto.
#. Crie uma conta no Travis CI.

5.8 - Referências
-----------------

- `Trilha sonora: Daft Punk - TRON Legacy <https://www.youtube.com/results?search_query=tron+legacy+soundtrack+>`_.
- `Automatizando a instalação (deploy) e atualização de sites com Git <http://blog.thiagobelem.net/automatizando-a-instalacao-deploy-e-atualizacao-de-sites-com-git/>`_.
- `Deploy estilo Heroku usando Git – Elton Minetto <http://eltonminetto.net/blog/2013/11/11/deploy-estilo-heroku-usando-git/>`_.
- `Deploy fácil com git - Dan Jesus <https://danjesus.github.io/blog/deploy-facil-com-git/>`_.
- `PuPHPet - Online GUI configurator for Puppet & Vagrant <https://puphpet.com/>`_.
- https://github.com/juancarlospaco/css-html-js-minify
- https://packages.debian.org/stable/tidy
