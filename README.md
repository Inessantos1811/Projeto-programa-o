
# Dados relativos aos 50 jogadores de maior destaque na NBA 🏀

# Contexto 🏀

Estes dados surgem de uma procuram por gostos comuns aos 4 elementos do grupo, onde se concluiu o tema: desporto. A NBA, especificamente, deve-se pela maior facilidade na colheita de dados. Os mesmos, consistem numa tabela dedicada aos 50 jogadores de maior destaque na última temporada regular jogada e alguns dos seus feitos (ex.: equipa onde jogam, pontos por jogo, arremessos convertidos, etc.).

Os dados usados, são retirados do site oficial do MSN ( https://www.msn.com/pt-br/esportes/basquete/nba/estatisticas-do-jogador ), dia 20 de abril de 2021. Acreditamos que esta seja uma fonte confiável, devido à sua popularidade e frequente atualização. É importante referir que, posteriormente a esta data, poderá haver uma nova atualização da tabela do site, no entanto, mantivemos os dados iniciais até ao fim deste projeto, sem alterá-los conforme o MSN.

Para uma melhor utilização, achamos por bem fazer uma “limpeza”, retirando alguns zeros, pontos e vírgulas que se mostraram desnecessários, acabando por também rejeitar 3 colunas de dados dispensáveis: Percentagem de Arremessos, Percentagem de Arremessos de 3 Pontos e Percentagem de Lances Livres. Depois de uma análise ainda no Excel, acreditamos não existirem valores ausentes, duplicados, ou a precisar de correção. 


# Bibliografia 🏀

➜ https://www.msn.com/pt-br/esportes/basquete/nba/estatisticas-do-jogador (21.04.2021)

➜ https://fangohr.github.io/python/book/Introduction-to-Python-for-Computational-Science-and-Engineering.pdf

➜ https://www.utc.fr/~jlaforet/Suppl/python-cheatsheets.pdf

Programação em Python-Fundamentos e Resolução de Problemas, de Ernesto Costa 


# Estrutura 🏀

`Jogadores em destaque NBA.csv`:  dados relativos aos 50 jogadores, da NBA, em maior destaque, na última temporada regular jogada. Estes dados foram recolhidos no dia 20 de abril de 2021.


# API’s usados – notas técnicas 🏀

Primeiramente apresentou-se o HTML (MSN). Como o mesmo tem apenas a tabela que queremos analisar, transferimos a mesma para csv.

Apresentação do HTML:
#df = pd.read_html ('https://www.msn.com/pt-br/esportes/basquete/nba/estatisticas-do-jogador?ocid=StripeOCID')

HTML para csv: código feito através de pesquisa no youtube:
#df[0].to_csv('Dados NBA 2021') 
Baseado no video:
https://www.youtube.com/watch?v=ODNMNwgtehk&t=213s ('Scrape HTML tables easily with Pandas and Python')

Depois de ter o código em csv, passamos à analise: averiguar se faltam dados na tabela ( df.info() ) e comprovar que encontra corretamente preenchida, sem dados em falta. Assim ficamos a saber, também, com que tipos de dados vamos trabalhar.

Este processo foi realizado para todos os dados.


# Dicionário de dados 🏀

| Nome  | Significado | Tipo de dados |
| ------| ----------- | --------------|
|`Posição`| Classificação dos melhores jogadores|int64|
|`Jogador`| Nome do jogador(primeiro e último) |object|
|`Equipa`| Nome da equipa de onde cada jogador faz parte|object|
|`Partidas jogadas`|Número de jogos que cada jogador fez ao longo da época|int64|
|`Minutos por jogo`|Média de minutos que cada atleta jogou por partida|float64|
|`Pontos`|Média de pontos que cada atleta marcou por partida|float64|
|`Arremessos convertidos`|Número de lançamentos convertidos por cada jogador ao longo da época|int64|
|`Tentativa de arremessos`|Número de tentativas de lançamentos por cada jogador ao longo da época|int64|
|`Arremesso de 3 pontos convertidos`|Número de lançamentos de 3 pontos convertidos por cada jogador ao longo da época|int64|
|`Tentativa de arremessos de 3 pontos`|Número de tentativas de lançamentos de 3 pontos por cada jogador ao longo da época|int64|
|`Lances livre convertido`|Número de lances livres convertidos por cada jogador ao longo da época|int64|
|`Tentativa de arremessos livre`|Número de tentativas de lançamentos livres por cada jogador ao longo da época|int64|


# Poster 🏀
![Destaques NBA](https://user-images.githubusercontent.com/76159858/120102638-dd9dad80-c143-11eb-87b1-be6bbfcd78a4.png)
