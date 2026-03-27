3 - QUAIS OS PRODUTOS TEM O MESMO PERCENTUAL DE DESCONTO?

    SELECT 
       a.product_id,
       a.discount,
       b.product_id,
       b.discount
    FROM (
       SELECT DISTINCT product_id, discount
       FROM order_details
       ) a
    INNER JOIN (
      SELECT DISTINCT product_id, discount
      FROM order_details
      ) b
    ON a.discount = b.discount
    WHERE a.product_id < b.product_id;

![resposta_desafio_self_join](../imagens/14_subquery_01.png)
