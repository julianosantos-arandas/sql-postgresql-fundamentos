1 -  QUAL FOI A MÉDIA DO VALOR DEVIDO POR MÊS.

    SELECT AVG(totaldue) AS "media", EXTRACT(MONTH FROM orderdate) AS "mes"
    FROM sales_salesorderheader_clean
    GROUP BY EXTRACT(MONTH FROM orderdate)
    ORDER BY "mes";

![resposta_desafio_extract](../imagens/15_extract_01.png)

