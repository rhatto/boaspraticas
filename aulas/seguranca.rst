6. Segurança e privacidade
==========================

6.1 - Segurança começa no desenvolvimento
-----------------------------------------

* Criptografia é só uma parte das práticas seguras.
* Modelagem de ameaças e testes de penetração: inverta os papéis: e se você fosse o/a atacante?
* A dificuldade de se encontrar vulnerabilidades.
* Segurança por isolamento ajuda, mas botar a aplicação dentro de um cordão sanitário protege mais o ambiente de hospedagem do que a aplicação.

6.2 - Use bibliotecas criptográficas consolidadas!
--------------------------------------------------

* Erros de implementação são grandes fontes de brechas de segurança.
* Caso você precise implementar primitivas criptográficas no seu código, use bibliotecas existentes!
* Encapsule as conexões das suas aplicações em canais criptografados.
* TLS é o protocolo mais consolidado e adequado, apesar de não ser perfeito.

6.3 - Princípio das permissões mínimas
--------------------------------------

* Comece o desenvolvimento com o mínimo de permissões necessárias para a sua aplicação e libere o acesso conforme necessário.
* Permissões de arquivos são propriedades no sistema de arquivo!
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

6.4 - Criptografia básica
-------------------------

* Assinaturas digitais.
* Comunicação cifrada.
* Checagem de integridade de código no git e em geral.

6.5 - Certificados x509 para SSL/TLS/HTTPS
------------------------------------------

* `Let's Encrypt <https://letsencrypt.org>`_.
