🔹CONTEXTO  
  SIMULAR UM SISTEMA SIMPLES ONDE: EXISTEM AUTORES, EXISTEM LIVROS, UM AUTOR PODE TER VÁRIOS LIVROS. 

TABELA 1: AUTORES  
CRIE UMA TABELA COM:  
🔹IDENTIFICADOR DO AUTOR  
🔹NOME DO AUTOR  
🔹PAÍS DE ORIGEM 

    CREATE TABLE autores(
    autor_id INT,
    nome_autor VARCHAR(50),
    pais_origem VARCHAR(50),
    PRIMARY KEY(autor_id)
    );

TABELA 2: LIVROS   
CRIE UMA TABELA COM:   
🔹IDENTIFICADOR DO LIVRO   
🔹TÍTULO DO LIVRO   
🔹ANO DE PUBLICAÇÃO   
🔹IDENTIFICADOR DO AUTOR (RELAÇÃO)   

    CREATE TABLE livros(
    autor_id INT,
    id_livro INT,
    titulo_livro VARCHAR(50),
    ano_publicacao INT,
    PRIMARY KEY(autor_id, id_livro),
    FOREIGN KEY(autor_id) REFERENCES autores(autor_id)
    );

*RELACIONAMENTO  
 🔹UM AUTOR PODE TER VÁRIOS LIVROS  
 🔹UM LIVRO PERTENCE A UM AUTOR  


INSERT INTO  
🔹 INSIRA PELO MENOS:  
   AUTORES (3 REGISTROS)

    INSERT INTO autores(autor_id, nome_autor, pais_origem)
    VALUES 
       (10, 'Machado de Assis', 'Brasil'),
       (20, 'Ernest Hemingway', 'Estados Unidos'),
       (30,	'William Shakespeare', 'Reino Unido')

![desafio_insert](../imagens/18_insert_into.png)
