1. Metodologias e técnicas de produtividade
===========================================

1.1 - O que são boas práticas em desenvolvimento?
-------------------------------------------------

1.1 - Apresentação do professor e do curso
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Silvio Rhatto, desenvolvedor autodidata.
- Curso dividido em aulas independentes umas das outras.
- O curso completo é acompanhado pelo desenvolvimento de uma pequena aplicação.

1.1 - O que são boas práticas de desenvolvimento?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Trata-se de *organização* no trabalho para que ele flua.
- Não há um único caminho: existem inúmeras metodologias e técnicas.
- Vou ensinar as mais *simples* e que tendem a resistir ao tempo.
- Foco em Software Livre e Aberto (FOSS).
- Experimente diversas metodologias, técnicas e ferramentas e monte seu próprio kit!

Imagens:

* https://upload.wikimedia.org/wikipedia/commons/7/7c/Yin_and_Yang.svg
* https://www.gnu.org/graphics/meditate.en.html

Link:

* https://www.youtube.com/watch?v=2FQU0WeGSEM

1.1 - O problema fundamental
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* O processo criativo não é linear e difícil de colocá-lo numa metodologia de trabalho.
* Muitos métodos tentam dominar e formatar o fluxo natural de atividades.
* Queremos técnicas e ferramentas que reduzam o ruído no trabalho, mas que não acarretem na perda de liberdade criativa.
* Dificuldades essenciais e acidentais (Aristóteles).

1.2 - Metodologias pessoais
---------------------------

Queremos evitar:

- Cabeça cheia de ruído.
- Ansiedade.
- Procrastinação.
- Empacamento.

Queremos:

- Simplicidade sem perda de qualidade (KISS).
- Excelência (melhoria incremental) ao invés de perfeccionismo obsessivo.

1.2 - Metodologias pessoais - Básico
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Fundamental: fazer fluir a criatividade.
- Evitar distrações e preocupações.
- Foco na missão: uma tarefa por vez.
- Básico: agenda, lista de tarefas e log (registro).
- Fazer o essencial e ter autocrítica sobre isso.
- Método não é lei, é sugestão de caminho. Você descobriu que é multi-tarefas e funciona melhor assim? Ok! :)
- Mude seus hábitos aos poucos!

1.2 - Metodologias pessoais - Pomodoro
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

É uma técnica simples para execução de tarefas:

- Material: alarme e lista de tarefas.
- Escolha uma tarefa e anote na sua lista.
- Ajuste o cronômetro (25 minutos tradicionalmente).
- Trabalhe na tarefa até o cronômetro disparar. Marque um X na lista ao lado da tarefa.
- Pare por um tempo curto (5 minutos, por exemplo).
- Depois de 4 pomodoros, faça uma pausa mais longa (15 a 30 minutos).

Imagem:

* `Cronômetro do pomodoro <https://en.wikipedia.org/wiki/Pomodoro_Technique#/media/File:Il_pomodoro.jpg>`_.

1.3 - Get Things Done (GTD)
---------------------------

É uma técnica para organização de tarefas / vida.

- Colete: apareceu na sua frente? Coloque para fora da cabeça!
- Processe.
- Organize.
- Planeje.
- Faça!
- Workflow: https://en.wikipedia.org/wiki/Getting_Things_Done#/media/File:GTDcanonical.png

1.4 - Zen to Done (ZTD)
-----------------------

ZTD é um GTD simplificado e mais estruturado:

- Tenha uma rotina.
- Reduza as suas tarefas ao essencial.
- Comece o dia realizando as tarefas importantes. Não se perca.
- Sugestão do chef: ZTD com Pomodoro!

1.5 - Metodologias em equipe
----------------------------

1.5 - A Catedral e o Bazar
~~~~~~~~~~~~~~~~~~~~~~~~~~

- Eficiência do código aberto.
- Agile: conjunto de princípios.

1.5 - Metodologias populares
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Scrum: metodologia de gerenciamento de projetos.
- XP: metodologia de engenharia de software.
- Kanban: controle coletivo de tarefas.
- Híbridação: Scrumban + XP :D

1.6 - Começando um projeto
--------------------------

1.6 - Etapas
~~~~~~~~~~~~

- Etapa 0: descoberta, brainstorm e levantamento de escopo!

    - Qual ou quais problemas a serem atacados?
    - Como definir o projeto e seu escopo? O que é e o que não é?
    - Quais soluções possíveis? Qual a escolhida?
    - A ser realizado em conjunto pela equipe de desenvolvimento e quaisquer partes envolvidas (clientes, por exemplo).
    - Descrição em alto nível.

- Etapa 1: pesquisa do que já existe: quais soluções abarcam os problemas formulados? No que deixam a desejar?
- Etapa 2: planejamento inicial: escolha inicial de metodologias, bootstrap, provas de conceito, etc.
- Etapa 3: aplicar um conjunto de metodologias mas principalmente *realizar* o projeto.

Imagens:

* Diagramas jocosos de problema/solução.

1.7 - Projeto de exemplo
~~~~~~~~~~~~~~~~~~~~~~~~

0. Descoberta:
 
  * Problema: garantir que o aluno, ao concluir este curso, possua um blog simples para relatar suas descobertas em desenvolvimento de software (knowledge base / bagagem de conhecimento pessoal).
  * Escopo:

    * O blog deve ser construido de acordo com as ferramentas abordadas neste curso.
    * Quanto mais simples, melhor: fácil de construir e confortável para manter e consultar (afinal, não queremos gastar tempo no futuro mantendo esse projeto).
    * Que dificilmente se torne tecnologicamente obsoleto: sem base de dados, com o mínimo de programação e formato de edição simples.
    * Que dependa o mínimo de bibliotecas e aplicações externas.
    * Que seja fácil de hospedar em qualquer local, fácil de fazer backup e que possa facilmente ser transformado noutros formatos (livro).
  * Soluções:

    * Criar um blog em qualquer lugar e fazer backups na unha? Pouco elegante e não atende a todos os requisitos.
    * Criar um blog em HTML simples e subir manualmente para um servidor? Não, queremos algo entre a web 1.0 e a web contemporânea.
    * Que tal criarmos um blog gerado estaticamente, isto é, um conjunto de arquivos simples de editar e que são compilados para o formato de site que possa ser facilmente enviado para um servidor como qualquer outra aplicação web?

1. Pesquisa: pesquise pesquise pesquise! O que você encontrou?
2. Bootstrap:

   * Precisamos de um nome. Curiosamente, nomear um projeto é a etapa mais difícil, mas hoje estamos criativos e chamaremos de "blogático", gerador de sítio estático :)
   * A metodologia utilizada será o desenvolvimento incremental ao longo deste curso.
   * Design inicial: o blogático varre uma pasta com arquivos de texto e gera o conteúdo no formato de website numa outra pasta.
   * Plano inicial para a dominação mundial:

    * Criar o repositório do projeto.
    * Script básico para geração do site.
    * Conteúdo inicial para testes.
    * Documentação.
    * Lançamento!

3. Realização: quer ver como o projeto pode ser realizado? Continue com o curso! :P

1.8 - Atividades
----------------

#. Adote a técnica Pomodoro numa tarefa grande e importante do seu dia. Você pode usar qualquer cronômetro disponível -- do seu computador, do telefone, do relógio de pulso ou mesmo um timer de cozinha. Permaneça apenas realizando a tarefa importante em cada bloco de 25 minutos. Avalie a eficácia do método: ele te ajudou?

#. Para este curso, definimos o nosso projeto de exemplo como sendo um website/blog bem simples. Você pode fazer o mesmo ou então escolher qualquer projeto que queira fazer usando qualquer linguagem de programação e adaptar as atividades propostas nas aulas seguintes de acordo com o seu caso. Sugerimos apenas que você escolhe um nome para o seu projeto, mesmo que temporário! Mas lembre-se: nomes tem poder! :)

#. Bônus: esboce um documento simples de escopo para o seu projeto. Ele pode ser um importante guia nas fases iniciais.

1.9 - Referências
-----------------

- `Best coding practices - Wikipedia, the free encyclopedia <https://en.wikipedia.org/wiki/Best_coding_practices>`_.
- `Best practices for software development projects <http://www.ibm.com/developerworks/websphere/library/techarticles/0306_perks/perks2.html>`_.
- `Boas práticas de engenharia de software \| Guia da Startup e da Gestão de Produtos de Software <http://www.guiadastartup.com.br/boas-praticas-de-engenharia-de-software/>`_.
- `Boas Práticas de Desenvolvimento – melhorando o seu dia-a-dia <http://blog.matheusbodo.com/boas-praticas-de-desenvolvimento-melhorando-o-seu-dia-a-dia/>`_.
- `Melhores Práticas para Desenvolvimento de Sistemas e Software <http://www.ibm.com/developerworks/br/rational/library/systems-software-lifecycle-development/>`_.
- `Arquitetura, padrões, projetos e boas práticas sobre desenvolvimento de software - georgemendonca <http://softwarelivre.org/georgemendonca/blog/arquitetura-padroes-projetos-e-boas-praticas-sobre-desenvolvimento-de-software>`_.
- `HOME -The Pomodoro Technique® <http://pomodorotechnique.com/>`_.
- `Técnica de Pomodoro: Melhorar a Produtividade \| Freelancer e Produtividade <http://www.escolafreelancer.com/tecnica-de-pomodoro-melhorar-produtividade/>`_
- `Técnica pomodoro – Wikipédia, a enciclopédia livre <https://pt.wikipedia.org/wiki/T%C3%A9cnica_pomodoro>`_.
- `Zen to Done - ZTD - Lucas Teixeira <http://lucasteixeira.com/ztd/>`_.
- `Zen To Done (ZTD): The Simple Productivity System : zen habits <http://zenhabits.net/zen-to-done-ztd-the-ultimate-simple-productivity-system/>`_.
- `Time management - Wikipedia, the free encyclopedia <https://en.wikipedia.org/wiki/Time_management>`_.
- `Princípios por trás do Manifesto Ágil <http://www.agilemanifesto.org/iso/ptbr/principles.html>`_.
- `Manifesto para o desenvolvimento ágil de software <http://www.manifestoagil.com.br/>`_.
- https://www.mountaingoatsoftware.com/blog/differences-between-scrum-and-extreme-programming
- http://manifesto.co.uk/kanban-vs-scrum-vs-xp-an-agile-comparison/
- `Zen e a Arte de Manutenção de Motocicletas <https://pedropeixotoferreira.files.wordpress.com/2014/03/robert-pirsig-zen-e-a-arte-da-manutenc3a7c3a3o-de-motocicletas.pdf>`_.
- `O Tao da programação <http://www.geocities.ws/worgtal/2002/tao.pdf>`_.
- `Top Open-Source Static Site Generators - StaticGen <https://www.staticgen.com/>`_.
- `principles - IndieWebCamp <https://indiewebcamp.com/Principles>`_.
- `Aprenda sobre Desenvolvimento Ágil de Software | DesenvolvimentoAgil.com.br <http://www.desenvolvimentoagil.com.br/>`_.
- `A Catedral e o Bazar - Wikisource <https://pt.wikisource.org/wiki/A_Catedral_e_o_Bazar>`_.
