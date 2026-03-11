
1 - QUANTAS PESSOAS TEM O MESMO NOME DO MEIO?

    SELECT "MiddleName", COUNT("MiddleName") AS "Quantidade"
    FROM person_person
    GROUP BY "MiddleName";

2 - QUAL É A QUANTIDADE MÉDIA DE CADA PRODUTO VENDIDO?

    SELECT "ProductID", AVG("OrderQty") AS "Média"
    FROM sales_salesorderdetail
    GROUP BY "ProductID";

3 - Quais são os 10 produtos com maior valor total de vendas?

    SELECT 
      "ProductID", 
      SUM("LineTotal") AS "Total"
    FROM sales_salesorderdetail
    GROUP BY "ProductID"
    ORDER BY "Total" DESC
    LIMIT 10;
