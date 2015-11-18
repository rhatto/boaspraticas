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

* Ferramenta para criação e gestão de ambientes de desenvolvimento.
* Sua aplicação roda localmente, porém dentro de uma máquina virtual.
* O simples comando `vagrant up` ergue a máquina virtual e realiza a configuração do ambiente.
* A "receita" do ambiente de desenvolvimento pode ser compartilhada entre todos(as) desenvolvedores(as) do software.
* O vagrant se soma ao nosso ambiente de trabalho e também serve como ambiente de testes.

Roteiro do screencast:

::

  # Instalando o vagrant
  sudo apt-get install vagrant

  cd ~/projetos/blogatico
  vagrant init

5.5 - Fazendo o deploy
----------------------

- Deploy: disponibilizar o código em ambiente de hospedagem (desenvolvimento, staging ou produção).
- SSH: protocolo de comunicação criptografada e autenticada entre cliente e servidor.
- Git, rsync e sftp: diversos, dentre inúmeros, meios de se transferir o código.
- O deploy também pode ser automatizado usando scripts ou softwares especializados (ansible, capistrano, etc).

Roteiro do screencast:

* SSH: entrando no servidor (fingerprints e senha).
* SSH: autenticação por chave.
* Bônus: github com chave pública.
* Clonando o repositório em produção.
* Atualizando o repositório.
* Bônus: deploy automatizado com git-hooks.

5.6 - Testes e integração contínua
----------------------------------

- Erros de programação são muito comuns.
- Apenas a atenção não é suficiente.
- Testar manualmente o software é importante, porém é um trabalho repetitivo, cansativo e também sujeito a falhas.
- Rotinas automatizadas de teste podem pegar muitos erros e serem feitas localmente ou através de serviços.

Roteiro do screencast:

* Mostrar softwares e serviços de integração contínua.
* Criar um protótipo local e simples de teste e integração contínua.

5.7 Atividades
--------------

#. Crie um ambiente de desenvolvimento vagrant para o seu projeto.
#. Experimente o PuPHPet para gerar uma configuração mais complexa de ambiente virtual de desenvolvimento.
#. Crie uma rotina de testes simples para o seu projeto.

5.8 - Referências
-----------------

- `Trilha sonora: Daft Punk - TRON Legacy <https://www.youtube.com/results?search_query=tron+legacy+soundtrack+>`_.
- `Automatizando a instalação (deploy) e atualização de sites com Git <http://blog.thiagobelem.net/automatizando-a-instalacao-deploy-e-atualizacao-de-sites-com-git/>`_.
- `Deploy estilo Heroku usando Git – Elton Minetto <http://eltonminetto.net/blog/2013/11/11/deploy-estilo-heroku-usando-git/>`_.
- `Deploy fácil com git - Dan Jesus <https://danjesus.github.io/blog/deploy-facil-com-git/>`_.
- `PuPHPet - Online GUI configurator for Puppet & Vagrant <https://puphpet.com/>`_.
- `Comparison of continuous integration software - Wikipedia, the free encyclopedia <https://en.wikipedia.org/wiki/Comparison_of_continuous_integration_software>`_.
