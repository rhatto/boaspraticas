6. Segurança e privacidade
==========================

6.1 - Segurança começa no desenvolvimento
-----------------------------------------

* Criptografia é só uma parte das práticas seguras.
* Testes de penetração: inverta os papéis: e se você fosse o/a atacante?

6.2 - Use bibliotecas consolidadas!
-----------------------------------

6.3 - Princípio das permissões mínimas
--------------------------------------

* Permissões de arquivos são propriedades no sistema de arquivo! Elas não são necessariamente preservadas com a cópia de arquivos entre sistemas!

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
