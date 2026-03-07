1 - O time quer analisar produtos que:

   Foram lançados entre 2011-01-01 e 2012-12-31

   Têm StandardCost entre 100 e 1000

   São produtos finais (FinishedGoodsFlag = true)

   Mas há uma regra extra:

   Dentro desse grupo, ordenar primeiro pelos produtos
   com menor margem de segurança
   (SafetyStockLevel - ReorderPoint)

   Depois:

   maior custo primeiro

   nome em ordem alfabética

    SELECT *
    FROM production_product
    WHERE "SellStartDate" BETWEEN '2001-01-01' AND '2012-12-31' 
    AND "StandardCost" BETWEEN 100 AND 1000
    AND "FinishedGoodsFlag" = true
    ORDER BY ("SafetyStockLevel" - "ReorderPoint") ASC,
    "StandardCost" DESC,
    "Name" ASC;

![Resultado_desafio_BETWEEN](../)

             
  
