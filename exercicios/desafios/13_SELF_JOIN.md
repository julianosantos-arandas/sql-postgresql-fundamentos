1 - LOCALIZAR TODOS OS CLIENTES QUE MORAM NA MESMA REGIÃO.

    SELECT a.contact_name, b.contact_name, a.region
    FROM customers a
    JOIN customers b 
      ON a.region = b.region
      AND a.customer_id < b.customer_id;

  
