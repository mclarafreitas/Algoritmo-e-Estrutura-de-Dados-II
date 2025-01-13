# Unidade 2 Trabalho 3 - Algoritmos Clássicos (Dijkstra e Kruskal)

## Aluna:  
- Maria Clara Moura de Freitas (20230093652)

## Objetivo Geral:  

Utilizou-se o algoritmo de Kruskal, que é empregado para encontrar a Árvore Geradora Mínima (MST) de um grafo ponderado e conectado. O algoritmo funciona ordenando as arestas por peso e adicionando-as à MST em ordem crescente, desde que não formem ciclos. Essa abordagem gananciosa assegura a minimização do peso total da árvore geradora. No contexto deste trabalho, havia a possibilidade de escolher entre alguns problemas sugeridos, e o escolhido foi o relacionado ao transporte na cidade de Natal. O objetivo foi conectar grandes centros de transporte, especificamente terminais de ônibus, utilizando uma Árvore Geradora Mínima (MST). O propósito central é identificar as rotas mais curtas entre esses pontos de interesse (POIs), reduzindo a distância total de viagem e otimizando a infraestrutura de transporte urbano.

# Problema 1 - Dijkstra

## Objetivo Geral:

## Desenvolvimento

## Resultados e Discussão

## Conclusão

# Problema 2 - Kruskal

## Objetivo Geral:  

Utilizou-se o algoritmo de Kruskal, que é empregado para encontrar a Árvore Geradora Mínima (MST) de um grafo ponderado e conectado. O algoritmo funciona ordenando as arestas por peso e adicionando-as à MST em ordem crescente, desde que não formem ciclos. Essa abordagem gananciosa assegura a minimização do peso total da árvore geradora. No contexto deste trabalho, havia a possibilidade de escolher entre alguns problemas sugeridos, e o escolhido foi o relacionado ao transporte na cidade de Natal. O objetivo foi conectar grandes centros de transporte, especificamente terminais de ônibus, utilizando uma Árvore Geradora Mínima (MST). O propósito central é identificar as rotas mais curtas entre esses pontos de interesse (POIs), reduzindo a distância total de viagem e otimizando a infraestrutura de transporte urbano.

## Desenvolvimento  

Para atingir o objetivo proposto, o trabalho foi desenvolvido em etapas principais descritas a seguir:

Coleta de Dados Geográficos:
Os dados espaciais de Natal foram obtidos através da biblioteca OSMnx, que permite a extração de redes viárias e outras informações geográficas diretamente do OpenStreetMap (OSM). Foram identificados os POIs correspondentes aos terminais de ônibus na cidade.

Construção do Grafo da Rede Viária:
A malha viária de Natal foi representada como um grafo utilizando o NetworkX. Cada nó no grafo representa um ponto da malha viária, e as arestas representam as conexões entre os pontos, ponderadas pelas distâncias reais em metros.

Seleção dos POIs:
Os POIs correspondentes aos terminais de ônibus foram filtrados a partir do grafo da cidade. A localização geográfica dos terminais foi obtida e convertida em coordenadas no grafo.

Geração da MST:
Foi utilizada a biblioteca scipy para calcular a Árvore Geradora Mínima (MST) entre os POIs selecionados. A MST é composta pelas arestas que conectam todos os POIs de forma eficiente, minimizando a distância total sem criar ciclos.

Visualização dos Resultados:
A MST gerada foi sobreposta ao mapa de Natal. As rotas otimizadas foram destacadas em vermelho, enquanto os POIs foram marcados como pontos azuis para facilitar a interpretação.

![Natal-RN](https://github.com/mclarafreitas/Algoritmo-e-Estrutura-de-Dados-II/blob/c47537d1924af4e7edb0cd06730f494a3cdc7192/Images/Unknown-3.png)


## Resultados e Discussão
A Árvore Geradora Mínima gerada conectou eficientemente os terminais de ônibus em Natal, resultando em um comprimento total de 61.174,97 metros. Este valor reflete a soma das distâncias das rotas otimizadas entre os POIs. O uso do algoritmo de Kruskal foi fundamental para garantir a eficiência no processo de geração da MST, uma vez que sua abordagem gananciosa, baseada na ordenação e seleção de arestas de menor peso, permitiu a criação de uma rede otimizada sem ciclos.

Visualização:

As rotas da MST foram exibidas no mapa de Natal, com as conexões otimizadas destacadas em vermelho.

Os POIs foram representados como pontos azuis, correspondendo às localizações dos terminais de ônibus.

Impacto da Análise:

A MST minimiza o custo total de conexões entre os terminais, oferecendo uma solução ideal para o planejamento de infraestrutura viária.

A implementação desse modelo em cenários reais poderia reduzir custos de deslocamento e melhorar a acessibilidade urbana.

Limitações:

Apenas os terminais de ônibus foram considerados como POIs. Outros grandes centros de transporte, como estações de trem e aeroportos, poderiam ser incluídos em análises futuras.

O modelo não considerou fatores como condições das vias ou custos de construção, que podem impactar a implementação prática.
A Árvore Geradora Mínima gerada conectou eficientemente os terminais de ônibus em Natal, resultando em um comprimento total de 61.174,97 metros. Este valor reflete a soma das distâncias das rotas otimizadas entre os POIs.
  
## Conclusão

O trabalho demonstrou que o uso de uma Árvore Geradora Mínima (MST) é uma abordagem eficaz para conectar grandes centros de transporte, minimizando distâncias e otimizando a infraestrutura urbana. A implementação do modelo em Natal resultou em uma rota total de 61.174,97 metros, conectando eficientemente os terminais de ônibus. A metodologia pode ser expandida para incluir outros tipos de centros de transporte e variáveis, como custos e acessibilidade, tornando-a uma ferramenta ainda mais robusta para o planejamento urbano. Além disso, o uso do algoritmo de Kruskal mostra-se aplicável em cenários futuros, onde a geração de redes otimizadas pode beneficiar o planejamento de infraestrutura em outras cidades ou contextos. A visualização gerada oferece um recurso valioso para tomadores de decisão na gestão de infraestrutura de transporte.

## Formas de executar o código

O código completo está disponível neste repositório do Github. Para executar o código é recomendável usar o Google Colab, que já possui as bibliotecas necessárias. No caso do uso de outro ambiente, talvez seja necessário instalar algumas dessas bibliotecas.

## Link para a apresentação do código em vídeo

[**Youtube**](https://youtu.be/LzVxKbDd_Y8)

## Referências

https://github.com/ivanovitchm/datastructure



