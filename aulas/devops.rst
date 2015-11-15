5. DevOps: desenvolvendo e orquestrando
=======================================

5.1 - O que é DevOps
--------------------

* Aproximação da administração de sistemas (sysadmin) com o desenvolvimento.
* Entregas constantes em ambientes de alta disponibilidade.
* Foco na automação.

Imagens:

* https://upload.wikimedia.org/wikipedia/commons/b/b5/Devops.svg

5.1 Ambientes reprodutíveis
---------------------------

5.2 - Vagrant
-------------

Roteiro do screencast:

::

  # Instalando o vagrant
  sudo apt-get install vagrant

  cd ~/projetos/blogatico
  vagrant init

5.3 - KVM, docker, chroot e afins
---------------------------------

5.4 - Integração contínua
-------------------------

- Integração contínua usando o `Travis CI <http://travis-ci.org/>`_.

5.5 - Fazendo o deploy
----------------------

- SSH e rsync.
- Deploy via git.

5.6 Atividades
--------------

#. Instale o vagrant.
#. Crie uma máquina virtual para desenvolver o seu projeto.
#. Crie uma conta no Travis CI.

5.7 - Referências
-----------------

- `Trilha sonora: Daft Punk - TRON Legacy <https://www.youtube.com/results?search_query=tron+legacy+soundtrack+>`_.
- `Automatizando a instalação (deploy) e atualização de sites com Git <http://blog.thiagobelem.net/automatizando-a-instalacao-deploy-e-atualizacao-de-sites-com-git/>`_.
- `Deploy estilo Heroku usando Git – Elton Minetto <http://eltonminetto.net/blog/2013/11/11/deploy-estilo-heroku-usando-git/>`_.
- `Deploy fácil com git - Dan Jesus <https://danjesus.github.io/blog/deploy-facil-com-git/>`_.
- `PuPHPet - Online GUI configurator for Puppet & Vagrant <https://puphpet.com/>`_.
- https://github.com/juancarlospaco/css-html-js-minify
- https://packages.debian.org/stable/tidy
