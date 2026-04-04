
1 - QUANTAS PESSOAS TEM O MESMO NOME DO MEIO?

    SELECT "MiddleName", COUNT("MiddleName") AS "Quantidade"
    FROM person_person
    GROUP BY "MiddleName";
![resultado_group_by_01](../imagens/09_group_by_01.png)

2 - QUAL É A QUANTIDADE MÉDIA DE CADA PRODUTO VENDIDO?

    SELECT "ProductID", AVG("OrderQty") AS "Média"
    FROM sales_salesorderdetail
    GROUP BY "ProductID";
![resultado_group_by_02](../imagens/09_group_by_02.png)

3 - Quais são os 10 produtos com maior valor total de vendas? Do maior para o menor.

    SELECT 
      "ProductID", 
      SUM("LineTotal") AS "Total"
    FROM sales_salesorderdetail
    GROUP BY "ProductID"
    ORDER BY "Total" DESC
    LIMIT 10;
![resultado_group_by_03](../imagens/09_group_by_03.png)

4 - Quais foram as 10 vendas com maior valor total? Do maior para o menor.

     SELECT 
      "SalesOrderID", 
      SUM("LineTotal") AS "Total"
    FROM sales_salesorderdetail
    GROUP BY "SalesOrderID"
    ORDER BY "Total" DESC
    LIMIT 10;
![resultado_group_by_04](../imagens/09_group_by_04.png)

5 - QUANTOS PRODUTOS TEMOS CADASTRADO E A MÉDIA DOS MESMOS NAS ORDENS DE SERVIÇO?

    SELECT "productid", 
    COUNT("productid") AS "quantidade", 
    AVG("orderqty") AS "media"
    FROM production_workorder
    GROUP BY "productid";

![resultado_group_by_04](../imagens/09_group_by_05.png)
