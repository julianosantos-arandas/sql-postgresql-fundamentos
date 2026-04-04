
1 - QUAIS NOMES NO SISTEMA TEM UMA OCORRÊNCIA MAIOR QUE 10 VEZES, PORÉM SOMENTE ONDE O TÍTULO É 'Mr,'?

    SELECT "FirstName", COUNT("FirstName") AS "quantidade"
    FROM person_person
    WHERE "Title" = 'Mr.'
    GROUP BY "FirstName"
    HAVING COUNT("Title") >10
    ORDER BY "quantidade" DESC;

  ![resposta_desafio_having](../imagens/10_having_01.png)

2 - Identificar as províncias (stateprovinceid) que aparecem mais de 1000 vezes.

    SELECT "stateprovinceid", COUNT("stateprovinceid") AS "quantidade"
    FROM person_address
    GROUP BY "stateprovinceid"
    HAVING COUNT ("stateprovinceid") >= 1000
    ORDER BY "quantidade" DESC;

![resposta_desafio_having](../imagens/10_having_02.png)


3 - QUAIS PRODUTOS EM MÉDIA ESTÃO ABAIXO DE $ 1.000.000,00.

    SELECT "ProductID", AVG("LineTotal")
    FROM sales_salesorderdetail
    GROUP BY "ProductID"
    HAVING AVG("LineTotal") < 1000000;

![resposta_desafio_having](../imagens/10_having_03.png)
