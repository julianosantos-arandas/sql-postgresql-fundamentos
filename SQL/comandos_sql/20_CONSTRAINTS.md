TABELA clientes
🔹NOME - OBRIGATÓRIO
🔹IDADE - DEVE SER MAIOR OU IGUAL A 18
🔹EMAIL - DEVE CONTER '@"

    CREATE TABLE cliente1(
    nome VARCHAR(50),
    idade INT CHECK (idade >= 18),
    email TEXT CHECK(email ~'@'));
--------------------------------------

    INSERT INTO cliente1(nome, idade, email)
    VALUES 
      ('Juliano', 31, 'juliano@gmail.com'),
	    ('Jessica', 16, 'jessica@gmail.com'),
	    ('Emmanoel', 21, 'emannoel.gmail.com')
