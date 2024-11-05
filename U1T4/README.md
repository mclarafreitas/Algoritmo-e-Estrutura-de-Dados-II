# Unidade 1 Trabalho 4 - Análise da Conectividade e Estrutura da Rede de Ruas de Natal-RN usando OSMnx e NetworkX

## Aluna:  
- Maria Clara Moura de Freitas (20230093652)

## Objetivo Geral:  
Este trabalho teve como objetivo utilizar as métricas de análise de redes estudadas em sala de aula para explorar a rede de ruas da cidade de Natal-RN. Para isso, utilizamos as bibliotecas *OSMnx* e *Networkx* para acessar dados do OpenStreetMap e calcular métricas que apresentam a conectividade e estrutura da rede urbana. As métricas analisadas foram o comprimento médio do menor caminho, o diâmetro de rede e o coeficiente de agrupamento.


## Desenvolvimento  
Para a realização destas analises foram utilizados duas bibliotecas em Python:
1. *OSMnx*: Uma biblioteca que permite a extração e visualização de dados de redes urbanas via OpenStreetMap. Com esta biblioteca, foi possível obter a rede de ruas de Natal e representá-la como um grafo, onde cada interseção de ruas é um nó e cada segmento de rua é uma aresta.
2. *Networkx*: É uma biblioteca voltada para o estudo de grafos, utilizamos ela para calcular as métricas da rede. Onde transformamos o grafo gerado pelo *OSMnx* em um grafo de formato simples não direcionado para facilitar o cálculo de métricas.

Para extrair a rede das ruas de Netal foi baixado utilizando a função *graph_from_place* do *OSMnx*, limitando-se a ruas acessíveis a veículos. Com isso, foi impresso a imagem da representação visual da cidade, como ilustrado na imagem abaixo:
![Natal-RN](https://github.com/mclarafreitas/Algoritmo-e-Estrutura-de-Dados-II/blob/c93796cad7b58dffa101013386432ef0547fbf24/U1T4/Imagens/natalrn.png)
Em seguida, extraímos o maior compenente fortemente conectado, o que nos garante que todas as partes da rede analisada fossem acessíveis entre si. Após isso, calcumos as três métricas escolhidas por mim, que foram:
* Comprimento médio do menor caminho: Indica a média de menor distância entre pares de interseções, representando o nível geral de conectividade.
* Diâmetro da rede: Representa o maior menor caminho possível entre dois nós da rede, fornecenedo uma medida da extensão da cidade.
* Coeficiente de agrupamento: Mede a probabilidade de que dois vizinhos de um nó estejam conectados, o que representa o nível de interconectividade local na rede.

A Análise desses métricas proporciona uma visão detalhada da acessibilidade e conectividade da infraestrutura viária de Natal, possibilitando, por exemplo, identificar a complexidade e eficiência da rede, bem como áreas que podem ser melhor conectadas para facilitar o transporte urbano.

## Resultados e Discussão
Os valores encontrados para as métricas foram:
* Comprimento Médio do Menor Caminho (79.29): Esse valor indica que, em média, o menor caminho entre dois pontos na rede de ruas de Natal é de aproximadamente 79 unidades. Isso sugere uma boa conectividade entre diferentes áreas da cidade, embora o valor relativamente alto possa indicar alguma dispersão nas rotas.

* Diâmetro da rede (209): Este valor representa a maior distância mínima entre quaisquer dois pontos na rede. Um diâmetro alto pode indicar que existem áreas da cidade mais distantes entre si, ou seja, pode haver uma região menos acessível em relação ao centro da cidade ou a outras áreas mais conectadas.

* Coeficiente de Agrupamento (0.0305): O coeficiente de agrupamento baixo indica que a rede de ruas de Natal tem poucas conexões entre vizinhos de um nó. Isso é comum em redes de ruas com um layout mais linear, como avenidas e ruas longas, em vez de configurações com muitas interseções, como em redes com alta densidade de cruzamentos.

Após todo o desenvolvimento, três perguntas importantes surgiram:
1. Como está a conectividade geral entre diferentes pontos da cidade de Natal? A estrutura de rede de ruas permite um deslocamento eficiente entre as áreas da cidade:
    * O comprimento médio do menor caminho (Average Shortest Path Length) de 79.29 indica que, em média, a distância mínima entre dois pontos na rede é razoavelmente alta. Esse valor sugere que, embora exista conectividade entre diferentes áreas da cidade, o deslocamento entre pontos pode envolver trajetos longos, o que pode ser uma limitação para a eficiência no transporte urbano. Esse resultado pode indicar a necessidade de novas conexões em áreas que possivelmente são menos acessíveis.
   
2. A estrutura de ruas de Natal é densa em interseções e conexões entre vizinhos, ou é mais dispersa, com menos cruzamentos diretos?
   * O coeficiente de agrupamento (Clustering Coefficient) de 0.0305 indica um baixo nível de interconexão entre os vizinhos dos nós na rede. Isso significa que a estrutura de ruas de Natal tem uma configuração mais linear e menos densa em interseções. Em vez de muitos cruzamentos interligados, a rede parece ter mais avenidas principais e ruas que se estendem sem tantas interconexões locais. Esse tipo de estrutura pode ser menos adequado para deslocamentos curtos e pode indicar uma rede mais dispersa, comum em cidades que privilegiam um layout voltado para vias arteriais.
   
3. Existem áreas da cidade de Natal que são significativamente distantes entre si, dificultando o acesso e o deslocamento?
    * O diâmetro da rede (Diameter of Network) de 209 representa a maior distância mínima entre dois pontos da rede. Esse valor elevado sugere que existem áreas da cidade com distâncias consideráveis entre si, o que indica uma estrutura de rede onde alguns pontos estão relativamente isolados. Essa característica pode ser um desafio para o acesso a determinadas áreas, especialmente se estas não estiverem próximas de rotas principais ou de conexões diretas.
  
## Conclusão

A aplicação das métricas de redes urbanas usando OSMnx e NetworkX permitiu uma análise detalhada da conectividade e estrutura da rede viária de Natal, RN. A média do menor caminho e o diâmetro alto indicam uma cidade com uma rede de ruas relativamente conectada, mas com algumas áreas potencialmente mais distantes entre si. O baixo coeficiente de agrupamento aponta para uma estrutura de ruas onde as interconexões entre vizinhos são menos frequentes, característica comum em cidades com avenidas principais e bairros menos interligados.

Essas análises são fundamentais para urbanistas e planejadores urbanos, pois permitem identificar áreas que poderiam ser melhor conectadas, promovendo maior acessibilidade e eficiência de deslocamento na cidade.

## Formas de executar o código

O código completo está disponível neste repositório do Github. Para executar o código é recomendável usar o Google Colab, que já possui as bibliotecas necessárias. No caso do uso de outro ambiente, talvez seja necessário instalar algumas dessas bibliotecas.

## Link para a apresentação do código em vídeo

[**Youtube**](https://youtu.be)

## Referências


