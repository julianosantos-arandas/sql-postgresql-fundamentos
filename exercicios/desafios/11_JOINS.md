
1 - BUSQUE O NOME DOS PRODUTOS E AS INFORMAÇÕES DAS SUBCATEGORIAS JUNTAMENTE COM OS PREÇOS. USAR AS TABELAS production_productsubcategory E production_product.

    SELECT 
    pp."ListPrice", 
    pp."Name", 
    ps. "Name",
    pp. "ProductSubcategoryID"
    FROM production_product pp
    INNER JOIN production_productsubcategory ps ON pp."ProductSubcategoryID" = ps."ProductSubcategoryID";

![resultado_]
