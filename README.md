# Atividade_Oscar
Atividade de Banco de dados

Hoje vamos trabalhar com o Oscar.
A ideia de premiar ou ser premiado é para reconhecer:
- Reconhecer uma qualidade
- Reconhecer um atributo
- Reconhecer o esforço... 

Alguns diriam que prêmios são apenas um reconhecimento superficial do nosso trabalho, uma forma de massagear o ego e nos deixar com a sensação de que estamos fazendo algo certo. Outros, no entanto, defendem que os prêmios são uma forma de validação do nosso trabalho, uma prova de que estamos no caminho certo e de que estamos fazendo a diferença.

Prêmios têm sim o seu valor, mas que eles não são o único indicador de sucesso. É claro que é sempre bom ser reconhecido pelo nosso trabalho e ter um troféu ou uma placa para pendurar na parede, mas o mais importante mesmo é a satisfação pessoal que sentimos quando fazemos algo que amamos e que acreditamos ser importante. Então, sim, prêmios importam, mas não devemos deixá-los ser o único fator que determina o nosso sucesso e a nossa felicidade.

Nem todos os prêmios são merecidos e nem todos que merecem ganham prêmios. 
Então vale mesmo a pena, premiar? 

# Atividades para trabalhar com o Oscar

1 - Quantas vezes Natalie Portman foi indicada ao Oscar?
- Natalie Portman foi indicada três vezes ao oscar.

```
SELECT COUNT(*) FROM `movies` WHERE name = "Natalie Portman";
```

2 - Quantos Oscars Natalie Portman ganhou?
- Natalie Portman ganhou um oscar.

```
SELECT * from `movies` WHERE name = "Natalie Portman" and winner = "True";
```

3 - Amy Adams já ganhou algum Oscar?
-  Amy Adams não ganhou oscar.

```
SELECT * from `movies` where name = "Amy Adams" and winner = "True";
```

4 -  A série de filmes Toy Story ganhou um Oscar em quais anos?
- Toy Story ganhou dois oscars em 2011.

```
SELECT * from `movies` where `film` = "Toy Story 3" and winner = "True";
```

5 - Quem tem mais Oscars: a categoria "Melhor Ator" ou "Melhor Filme"?
- A categoria com mais Oscars é a de "Melhor filme".
```
SELECT COUNT(*) FROM movies WHERE category = "actor" and winner = "True"; 
SELECT COUNT(*) FROM movies WHERE category = "best picture" and winner = "True";
```

6 - O primeiro Oscar para melhor Atriz foi para quem? Em que ano?
- O primeiro Oscar para a melhor atriz foi para a Janet Gaynor em 1927.

```
SELECT year_film, name, category, winner FROM movies WHERE category = "actress" and winner = "true" ORDER BY year_film asc;
```

7 - Na coluna/campo Winner, altere todos os valores com "True" para 1 e todos os valores "False" para 0.

```
UPDATE movies SET winner = 1 WHERE winner = "True";
UPDATE movies SET winner = 0 WHERE winner = "False";
```

8 - Em qual edição do Oscar "Crash" ganhou o prêmio principal?
- "Crash" ganhou o principal prêmio na edição de 2006.

```
SELECT film, year_ceremony, winner, category FROM movies WHERE film = "Crash" and category = "best picture" and winner = 1;
```

9 - Bom... dê um Oscar para um filme que merece muito, mas não ganhou.
- " Piratas do Caribe: No Fim do Mundo".

```
UPDATE movies SET winner = 1 WHERE film = "Pirates of the Caribbean: At Worlds End";
```

10 - O filme Central do Brasil aparece no Oscar?
- Não aparece.

```
SELECT * FROM movies WHERE film LIKE "%central Brazil%"
```

11 - Inclua no banco 3 filmes que nunca nem foram nomeados ao Oscar, mas que na sua opinião, merecem. 
- 
