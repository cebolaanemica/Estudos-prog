#											:paperclip: **Principais características** :paperclip:

+ OpenSource

+ Point in time recovery

+ Linguagem procedural com suporte a linguagens de programação

+ Views, functions, procedures, triggers

+ Consultas complexas e Common table expressions (CTE)

+ Suporte a dados geográficos (PostGis)

+ Controle de concorrência multi-versão

+ colunas = atributos

  # 		**Colunas importantes**

## Chave primária / *Primary key* / **PK** :old_key:

- Conjunto de um ou mais campos que nunca se repetem. identidade da tabela. São usados como índice de referência na criação de relacionamentos entre tabelas.

## Chave Estrangeira / *Foreign Key* / **FK** :key:

- Valor de referência a uma PK de outra tabela da mesma tabela para criar um relacionamento.



# 		Sistemas de gerenciamento de bancos de dados :bank:

​	Ou Sistemas de gestão de base de dados (SGBD).

​	Conjunto de programas ou softwares responsáveis pelo gerenciamento de um banco de dados.

​	Programas que facilitam a administração de um banco de dados.

# Arquivo PostgreeSQL.conf :⏳

## Definição

​	Arquivo onde estão definidas e armazenadas todas as configurações do servidor PostgreSQL.

​	Alguns parâmetros só podem ser alterados com uma reinicialização do banco de dados.

​	A view pg_settings, acessada por dentro do banco de dados, guarda todas as configurações atuais.

​		**SELECT name, setting**

​		**FROM pg_settings;**

​	Ou: **SHOW [parâmetro];**

## Postgresql.conf

- Por padrão, o arquivo encontra-se dentro do diretório PGDATA definido no momento da inicialização do cluster de banco de dados.

- No sistema operacional Ubuntu, se o SQL foi instalado a partir do repositório oficial, o local será:

  ​	etc/postgresql/[versão]/[nome do cluster]/postgresql.conf 

## Configurações de conexão :red_circle:

- ### *LISTEN_ADDRESSES*

  ​	Endereços TCP/IP das interfaces que o servidor SQL vai escutar/liberar conexões.

- ### *PORT*

  ​	A porta TCP que o servidor SQL vai ouvir. O padrão é 5432.

- ### *MAX_CONNECTIONS*

  ​	Número máximo de conexões simultaneas no servidor SQL

- ### *SUPERUSER_RESERVED_CONNECTIONS*

  ​	Número de conexões (slots) reservados para conexões do banco de dados de super usuários.

  ## Configurações de autenticação :lock:

- ### *AUTHENTICATIONC_TIMEOUT*

  ​	Tempo máximo em segundos para o cliente conseguir uma conexão com o servidor.

- ### *PASSWORD_ENCRYPTION*

  ​	Algoritmo de criptográfia das senhas dos novos usuários criados no BC.

- ### *SSL*

  ​	Habilita a conexão criptografada por SSL (Somente de se o PGSQL foi compilado som suporte SSL)

