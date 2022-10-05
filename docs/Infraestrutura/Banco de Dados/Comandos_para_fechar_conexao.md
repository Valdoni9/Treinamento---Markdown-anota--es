# Postgre - Fechando sessão de usuario

````{.py3 hl_lines="4 10 17 22 26 34 35 36" linenums="1" title="Como verificar conexões ativas no PostgreSQL"}
Para conseguir listar o número de conexões ativas no PostgreSQL 
utilize o comando:

select * from pg_stat_activity;

conexoes_postgresql_mini

Você pode utilizar o comando count() para contar as conexões.

select count(*) from pg_stat_activity;

É possível filtrar por Banco de Dados colocando na clausula “where” o 
banco desejado.

Ex.:

select * from pg_stat_activity where datname = ‘NOME_DO_BANCO’;

Finalizar Conexões
Para finalizar conexões você pode utilizar a função abaixo passando como 
parâmetro o número do pid. O pid é obtido através do select na 
tabela '(pg_stat_activity)'.

Atenção: Esse comando não existe em versões do PostgreSQL  inferiores a 8.4.

select pg_terminate_backend(pid);

Obs.: A coluna “pid” em versões inferiores a 9.2 do PostgreSQL 
tinha o nome de “procpid”.

É possível finalizar todas as conexões menos a sua conexão através da 
query abaixo.

SELECT pg_terminate_backend(pid)
FROM pg_stat_activity
WHERE pid <> pg_backend_pid();
````