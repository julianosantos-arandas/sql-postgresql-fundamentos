
1 - QUAIS NOMES NO SISTEMA TEM UMA OCORRÊNCIA MAIOR QUE 10 VEZES, PORÉM SOMENTE ONDE O TÍTULO É 'Mr,'?

    SELECT "FirstName", COUNT("Title") AS "quantidade"
    FROM person_person
    WHERE "Title" = 'Mr.'
    GROUP BY "FirstName", "Title"
    HAVING COUNT("Title") >10;

  ![resposta_desafio_having](../imagens/09_having_01.png)
