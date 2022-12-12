6. Segurança e privacidade
==========================

6.1 - Segurança da informação
-----------------------------

É a hora de falar sobre segurança e privacidade no desenvolvimento. Grosso
modo, podemos dividir a segurança da informação em algumas propriedades, como
por exemplo:

1. Confidencialidade: é a garantia de que apenas a comunicação poderá
   ser interpretada pelas partes envolvidas, isto é, mesmo havendo interceptação
   por terceiros o conteúdo da comunicação estará protegido.

2. Integridade: é a garantia de que o conteúdo da comunicação não foi
   adulterado por terceiros.

3. Disponibilidade: garantia de que o sistema de comunicação estará acessível
   sempre que necessário.

4. Autenticidade: garante que cada uma das partes possa verificar se está de
   fato se comunicando com quem pensa estar se comunicando, isto é, a garantia
   de que não há um impostor do outro lado da comunicação.

Opcionalmente também podemos falar de:

5. Não-repúdio: garantir que as partes envolvidas na comunicação não possam negar
   ter participado da comunicação.

6. Anonimato: garantia de de as partes envolvidas na comunicação não possam ser
   identificadas.

Nem sempre os sistemas satisfazem todas essas propriedades!

6.2 - Segurança começa no desenvolvimento
-----------------------------------------

* Segurança: para fins do nosso curso, é a proteção da aplicação.
* Privacidade: proteção dos dados em poder da aplicação.
* Criptografia é só uma parte das práticas seguras.
* Obscuridade não é segurança: disclosures são saudáveis no desenvolvimento.

6.3 - Modelagem de ameaças e auditoria
--------------------------------------

* É fácil (e barato) produzir e difícil (e caro) encontrar vulnerabilidades.
* Modelagem de ameaças (teoria) e testes de penetração (prática): inverta os papéis: e se você fosse o/a atacante?
* Segurança por isolamento ajuda, mas botar a aplicação dentro de um cordão sanitário protege mais o ambiente de hospedagem do que a aplicação.

6.4 - Exemplo de ameaça: princípio das permissões mínimas
---------------------------------------------------------

* Exemplo de ameaça: o(a) atacante tem permissão de escrita no código da aplicação.
* Mitigação: forneça o mínimo de permissões necessárias para a sua aplicação e libere o acesso conforme necessário.
* Atenção! Permissões de arquivos são propriedades no sistema de arquivo!
* Elas não são necessariamente preservadas com a cópia de arquivos entre sistemas!

Roteiro do screencast:

::

  # Vendo as permissões e a posse de arquivos e pastas
  ls -l projetos

  # Mudando as permissões de um arquivo
  touch cofrinho
  chmod 000 cofrinho
  chmod 600 cofrinho

  # Mudando a posse de arquivos e pastas
  chown

6.5 - Criptografia básica
-------------------------

* Criptografia não é tudo em segurança, porém é o requisito básico e essencial.
* Ameaça: machine-in-the-middle.
* Mitigação:
  * Comunicação cifrada: HTTPS.
  * Checagem de integridade de código no git e em geral (assinaturas e checksums).

6.6 - Use bibliotecas criptográficas consolidadas!
--------------------------------------------------

* Erros de implementação são grandes fontes de brechas de segurança.
* Caso você precise implementar primitivas criptográficas no seu código, use bibliotecas existentes!
* Encapsule as conexões das suas aplicações em canais criptografados.
* TLS é o protocolo mais consolidado e adequado, apesar de não ser perfeito.

6.7 - HTTPS
-----------

6.7 - O que é
~~~~~~~~~~~~~

* HTTPS: HTTP em cima de uma conexão SSL/TLS.
* Padrão dos anos 90 e melhorado desde então.
* Se bem implementado: oferece segurança da informação num nível aceitável, porém não oferece anonimato.
* Se mal implementado: só oferece ilusão de segurança.
* Movimento crescente para tornar HTTPS padrão em todos os sites!

6.7 - Certificados para HTTPS
-----------------------------

* No HTTPS, a autenticidade é obtida usando uma "cadeia de certificação" provida por autoridades certificadoras.
* Checagem feita no navegador.
* É um esquema altamente vulnerável: a qualquer momento o castelo de cartas pode ruir.
* As alternativas a esse modelo ainda são incipientes.

6.8 - Atividades
----------------

#. Faça um pequeno documento de modelagem de ameaças para o seu projeto. Coloque-o na forma de "ameaça/mitigação". Organize cada par ameaça/mitigação segundo probabilidade decrescente de ocorrência e custo crescente de implementação, facilitando a implementação de cada medida de segurança.
#. Desafio: caso seu projeto seja uma aplicação web, obtenha um certificado e configure uma conexão HTTPS.

6.9 - Referências
-----------------

* Imagens usadas nos vídeos?
* `Let's Encrypt <https://letsencrypt.org>`_.
* `Segurança da informação – Wikipédia, a enciclopédia livre <https://pt.wikipedia.org/wiki/Seguran%C3%A7a_da_informa%C3%A7%C3%A3o>`_.
* `Web Privacy Rocks! <https://webprivacy.rocks/>`_: collection of documents about privacy on the Web and developing for the privacy-friendly web.
