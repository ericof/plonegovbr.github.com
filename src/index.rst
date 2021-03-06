Introdução
============

`github/plonegovbr`_ é o repositório de código produzido pelos membros da 
comunidade  `PloneGovBr <http://plone.org.br/gov>`_.

Este repositório segue as mesmas regras e práticas do 
`Collective <https://github.com/collective>`_ que é o coletivo de códigos 
criados pela comunidade Plone.

"Regras" do github/plonegovbr
===============================

Usando a termilogia do Github, o **plonegovbr** é uma organização e como tal
permite a criação de repositórios e times de usuários. Para facilitar a gestão
da organização definimos algumas regras:

- Todos os membros desta organização terão a permissão de ``Pull e Push`` para
  todos os repositórios aqui hospedados.
- Cada um dos repositórios terá donos (owners) que terão acesso 
  administrativo a eles.
- Abusos devem ser reportados através de um ticket no repositório 
  `plonegovbr.github.com`_.

Como conseguir acesso
========================

O primeiro passo é ter uma conta no `Github <https://github.com/>`_,
se você ainda não tem,
`crie uma gratuitamente <https://github.com/signup/free>`_.

Com sua conta criada, escolha uma das duas opções abaixo:

* Crie um ticket pedindo permissão através deste endereço:
  https://github.com/plonegovbr/plonegovbr.github.com/issues

* Ou faça o fork do repositório `plonegovbr.github.com`_, edite o arquivo
  ``permissions.cfg``, faça o commit, push e envie um Pull Request para nós
  (veja a seção abaixo para entender os detalhes).


Como gerenciar permissões e repositórios
==========================================

Visão geral
------------

Permissões são armazenadas no arquivo `permissions.cfg`_ no repositório
`plonegovbr.github.com`_.

Realize o fork do repositório 
`plonegovbr.github.com <https://github.com/plonegovbr/plonegovbr.github.com>`_
e edite o arquivo `permissions.cfg`_, realize o commit, push e inicie um
pull request através da interface do Github. 

Temos um script que é executado a cada 10min para verificar diferenças no
arquivo de permissões e atualizar o 
`plonegovbr <https://github.com/plonegovbr/>`_.

No arquivo `permissions.cfg`_ você encontrará uma lista de times e 
repositórios.

Times são representados por seções iniciadas com ``team:`` e repositórios
são seções iniciadas com ``repo:``.

Toda a criação de repositório deve ser feita de acordo com os passos indicados 
a seguir. 

**POR FAVOR não utilize o botão de criar novo repositório da interface
do Github, caso contrário a equipe que mantém esta organização terá que editar
o aquivo permissions.cfg manualmente, o que pode causar uma grande demora na criação.**


Criando um novo repositório
----------------------------

1. Faça o login no github e acesse o repositório do Plonegovbr no 
   endereço https://github.com/plonegovbr;    
2. Realize o fork do repositório plonegovbr.github.com;    
3. Em seu fork, edite o arquivo permissions.cfg. Adicione
   no final deste arquivo as linhas relativas a seu novo projeto 
   no seguinte formato:
   ::

      [repo:NOME_DO_NOVO_REPOSITORIO]
      teams = colaboradores
      owners = MEU_NOME_DE_USUARIO

4. Realize o commit, push e inicie um pull request através da 
   interface do Github.Quando o pull request for aceito, seu repositório
   será criado automaticamente, baseado nas configurações informadas.


Criando um fork de um repositório existente de outro usuário ou organização
-----------------------------------------------------------------------------

1. Faça o login no github e acesse o repositório do Plonegovbr no 
   endereço https://github.com/plonegovbr;    
2. Realize o fork do repositório plonegovbr.github.com;    
3. Em seu fork, edite o arquivo permissions.cfg. Adicione no final
   deste arquivo as linhas relativas a seu novo projeto no seguinte formato:
   ::

      [repo:NOME_DO_REPOSITORIO]
      fork = DE_USUARIO_OU_ORGANIZACAO/NOME_DO_REPOSITORIO
      teams = colaboradores
      owners = MEU_NOME_DE_USUARIO


4. Realize o commit, push e inicie um pull request através da interface do Github.    
   Quando o pull request for aceito, o fork do repositório será criado automaticamente,
   baseado nas configurações informadas.


Adicionando você ao time de colaboradores (ou qualquer outro time)
--------------------------------------------------------------------
1. Faça o login no github e acesse o repositório do Plonegovbr no 
endereço https://github.com/plonegovbr;
2. Realize o fork do repositório plonegovbr.github.com;    
3. Em seu fork, edite o arquivo permissions.cfg. Localize a linha
referente ao grupo colaboradores e adicione seu nome de usuário no final desta lista.
::

    [team:colaboradores]
    members =


4. Realize o commit, push e inicie um pull request através da interface do Github.    
Quando o pull request for aceito, você será adicionado ao grupo de colaboradores.
As mesmas instruções acima são válidas para qualquer outro grupo, basta localiza-lo no arquivo.


Editando o arquivo permissions.cfg
------------------------------------

Repositório criado, mas você não é o dono (owner)
    O repositório foi migrado de outra ferramenta e você não está com a
    permissão corretamente aplicada aqui ? Adicione seu nome de usuário ao
    item ``owners =`` da seção de seu repositório.


.. _`plonegovbr.github.com`: https://github.com/plonegovbr/plonegovbr.github.com
.. _`permissions.cfg`: https://github.com/plonegovbr/plonegovbr.github.com/blob/master/permissions.cfg
.. _`github/plonegovbr`: http://github.com/plonegovbr


Trabalhando com repositórios existentes
==========================================
Para trabalhar em um dos projetos existentes no repositório, você vai precisar
criar uma cópia de trabalho deste repositório. Essa cópia de um repositório é
chamada de Fork.

Fazendo o fork de um repositório
-----------------------------------

1. No Github, vá até a página do projeto que deseja realizar um Fork;
2. Click no botão 'Fork' que aparece no canto superior direito;

Na sequencia, uma cópia do projeto será criado em sua conta do github.
Veja no passo a seguir como trabalhar localmente em seu fork.

Trabalhando localmente em um fork
-----------------------------------
Você pode editar os arquivos de seu fork diretamente nas páginas do Github.
Entretanto é muito mais fácil e produtivo trabalhar em uma cópia do projeto
em seu computador. Fazer uma cópia do projeto é a operação conhecida como
clonar. Para clonar o seu repositório, execute o código a seguir:
::

    $ git clone git@github.com:username/nomedoseuprojeto.git


Configurando seu repositório
-----------------------------
QUando um repositório é clonado , ele está diretamente associado ao seu fork
no github, e não ao repositório que originou o fork. Para acompanhar as 
alterações feitas no repositório original, você precisa configurar o upstream:
::

    $ cd nomedoseuprojeto
    $ git remote add upstream git://github.com/plonegovbr/nomedoseuprojeto.git
    $ git fetch upstream


