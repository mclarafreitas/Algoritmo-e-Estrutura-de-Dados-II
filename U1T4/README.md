# Unidade 1 Trabalho 4 - Análise da Conectividade e Estrutura da Rede de Ruas de Natal-RN usando OSMnx e NetworkX

## Aluna:  
- Maria Clara Moura de Freitas (20230093652)

## Objetivo Geral:  
Este trabalho teve como objetivo utilizar as métricas de análise de redes estudadas em sala de aula para explorar a rede de ruas da cidade de Natal-RN. Para isso, utilizamos as bibliotecas *OSMnx* e *Networkx* para acesssar dados do OpenStreetMap e calcular métricas que apresentam a conectividade e estrutura da rede urbana. As métricas analisadas foram o comprimento médio do menor caminho, o diâmetro de rede e o coeficiente de agrupamento.


## Desenvolvimento  
Para a realização destas analises foram utilizados duas bibliotecas em Python:
1. *OSMnx*: Uma biblioteca que permite a extração e visualização de dados de redes urbanas via OpenStreetMap. Com esta biblioteca, foi possível obter a rede de ruas de Natal e representá-la como um grafo, onde cada interseção de ruas é um nó e cada segmento de rua é uma aresta.
2. *Networkx*: É uma biblioteca voltada para o estudo de grafos, utilizamos ela para calcular as métricas da rede. Onde transformamos o grafo gerado pelo *OSMnx* em um grafo de formato simples não direcionado para facilitar o cálculo de métricas.

Para extrair a rede das ruas de Netal foi baixado utilizando a função *graph_from_place* do *OSMnx*, limitando-se a ruas acessíveis a veículos. Com isso, foi impresso a imagem da representação visual da cidade, como ilustrado na imagem abaixo:
IMAGEM!!!
Em seguida, extraímos o maior compenente fortemente conectado, o que nos garante que todas as partes da rede analisada fossem acessíveis entre si. Após isso, calcumos as três métricas escolhidas por mim, que foram:
* Comprimento médio do menor caminho: Indica a média de menor distância entre pares de interseções, representando o nível geral de conectividade.
* Diâmetro da rede: Representa o maior menor caminho possível entre dois nós da rede, fornecenedo uma medida da extensão da cidade.
* Coeficiente de agrupamento: Mede a probabilidade de que dois vizinhos de um nó estejam conectados, o que representa o nível de interconectividade local na rede.

A Análise desses métricas proporciona uma visão detalhada da acessibilidade e conectividade da infraestrutura viária de Natal, possibilitando, por exemplo, identificar a complexidade e eficiência da rede, bem como áreas que podem ser melhor conectadas para facilitar o transporte urbano.

## Resultados e Discussão
Os valores encontrados para as métricas foram:
Comprimento Médio do Menor Caminho: 79.29 Esse valor indica
Diâmetro da rede: 209
Coeficiente de Agrupamento: 0.0305

Após todo o desenvolvimento, três perguntas importantes segiram:
1. Como está a conectividade geral entre diferentes pontos da cidade de Natal? A estrutura de rede de ruas permite um deslocamento eficiente entre as áreas da cidade:
2. A estrutura de ruas de Natal é densa em interseções e conexões entre vizinhos, ou é mais dispersa, com menos cruzamentos diretos? 
3.Existem áreas da cidade de Natal que são significativamente distantes entre si, dificultando o acesso e o deslocamento?

## Conclusão


## Formas de executar o código

O código completo está disponível neste repositório do Github, juntamente com o arquivo de dados em formato .csv. Para executar o código é recomendável usar o Google Colab, que já possui as bibliotecas necessárias. No caso do uso de outro ambiente, talvez seja necessário instalar algumas dessas bibliotecas.

## Link para a apresentação do código em vídeo

[**Youtube**](https://youtu.be)

## Referências


