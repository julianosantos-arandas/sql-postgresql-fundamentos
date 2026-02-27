
1 - OBTER O ID DOS 10 PRODUTOS MAIS CAROS CADASTRADOS NO SISTEMA, LISTANDO DO MAIS CARO PARA O MAIS BARATO.
    
    SELECT "ProductID", "Name", "ListPrice"
    
    FROM production_product
    
    ORDER BY "ListPrice" DESC
    
    LIMIT 10;

![Resultado do ORDER BY](../imagens/05_order_by_01.png)
  
