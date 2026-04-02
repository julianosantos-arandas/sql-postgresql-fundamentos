1 - LIMPEZA BÁSICA:
REMOVER ESPAÇOS EXTRA NOS NOMES
DEIXAR O EMAIL EM MINÚSCULO
PADRONIZAR CIDADE (PRIMEIRA LETRA MAIÚSCULA)

    SELECT TRIM(nome_cliente) AS cliente, 
           LOWER(TRIM(COALESCE(email, ''))) AS email,
 	       INITCAP(TRIM(cidade)) AS cidade
    FROM vendas_raw;

![resposta_desafio_funcoes_operadores](../imagens/16_funcoes_operadores_01.png)


2 - TRATAMENTO DE VALOR:
VÍRGULA NO DECIMAL
VALORES VAZIOS 
VALORES INVÁLIDOS 
- TRANSFORMAR EM NUMERICO E INVÁIDOS PARA NULL


      WITH base AS (
      SELECT 
          REPLACE(TRIM(valor), ',', '.') AS valor_tratado
      FROM vendas_raw
      )
      SELECT 
         CASE 
           WHEN valor_tratado ~ '^-?[0-9]+(\.[0-9]+)?$' 
           THEN valor_tratado::NUMERIC 
           ELSE NULL 
         END AS valor_limpo
      FROM base;

![resposta_desafio_funcoes_operadores](../imagens/16_funcoes_operadores_02.png)


3 - COLOCAR O NOMES E OS SOBRENOMES DOS CLIENTE SOMENTE EM UMA COLUNA.

     SELECT CONCAT("FirstName",' ', "LastName") AS "Nome do Cliente"
     FROM person_person
     ORDER BY "Nome do Cliente";

    
![resposta_desafio_funcoes_operadores](../imagens/16_funcoes_operadores_01.png)
