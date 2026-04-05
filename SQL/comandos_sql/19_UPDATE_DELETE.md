ALTERAR O id_livro '4', COM AS NOVAS INFORMAÇÕES DO id_livro 4.

    UPDATE livros
    SET id_livro = 4, titulo_livro = 'Quincas Borba', ano_publicacao = 1891
    WHERE id_livro = 8;

![desafio_update](../imagens/19_upadate.png)


DELETAR HAMELET DA TABELA LIVROS.
   
    DELETE 
    FROM livros
    WHERE titulo_livro = 'Hamelt';

ANTES 

![desafio_update](../imagens/19_upadate.png)

DEPOIS

![desafio_update](../imagens/19_delete.png)
