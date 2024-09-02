# exercicio-dataset-sql
re-exercicio sobre banco de dados

Dataset escolhido:
https://www.kaggle.com/datasets/sidtwr/videogames-sales-dataset

conjunto de 3 tabelas contendo informações sobre vendas de jogos para consoles de videogame; as tabelas menores(PS4_GamesSales e XboxOne_GameSales) possuem informações datadas entre 2013 e 2020, além de uma quantidade considerável de entradas sem ano. O outro arquivo(Video_Games_Sales_as_at_22_Dec_2016), tem sua entrada mais antiga com o ano de 1980, apenas 3 entradas com o ano de 2017 e uma única entrada com o ano de 2020, além de um numero comparativamente menor de entradas sem ano.


as tabelas possuem uma serie de informações em comum, mas a tabela maior possui colunas que as outras duas não possuem.
em comum, as 3 tabelas possuem as colunas de: "nome do jogo", "ano do seu lançamento", "gênero", "distribuidora",  e "pontuação de vendas" nos EUA, na Europa, no Japão, em "outros países", além de "vendas globais" que é apenas a soma dos valores das outras colunas de vendas.
 
a principal diferença entre as tabelas é que a a tabela com uma quantidade maior de informações possui colunas de informações que as outras duas não possuem, tendo 4 colunas com informações de agregadores de avaliações("notas da critica", "numero de críticos", "notas dos usuários", "numero de usuários"), além de: diferenciar "distribuidora" de "desenvolvedora", com uma coluna dedicada para cada; uma coluna dedicada para "classificação indicativa no sistema dos EUA"; e uma coluna para qual console o jogo foi lançado, já que esta tabela cobre um grande numero deles.

além disso, por algum motivo, a tabela do XboxOne possui uma coluna para um numero de id("primary_key").


foram realizadas 3 consultas, uma em cada tabela:

a tabela do PS4 foi apenas ordenada por ano de lançamento:
select * from PS4_Games_Sales
order by Year_of_Release

