1 -  QUAL FOI A MÉDIA DO VALOR DEVIDO POR MÊS.
 
    SELECT 
        DATE_TRUNC('month', orderdate) AS mes,
     AVG(totaldue) AS media
    FROM sales_salesorderheader_clean
    GROUP BY mes
    ORDER BY mes;

![resposta_desafio_extract](../imagens/15_extract_date_trunc_01.png)

2 - SELECIONAR TODAS A COMPRAS POR MÊS DE 2011.

    SELECT  salesorderid,
    EXTRACT(MONTH FROM orderdate) AS "data"
    FROM sales_salesorderheader_clean
    WHERE EXTRACT (YEAR FROM orderdate) = 2011;

![resposta_desafio_extract](../imagens/15_extract_date_trunc_02.png)
    
