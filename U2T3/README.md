# Unidade 2 Trabalho 3 - Titulo

## Aluna:  
- Maria Clara Moura de Freitas (20230093652)

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

![Natal-RN](https://github.com/mclarafreitas/Algoritmo-e-Estrutura-de-Dados-II/blob/c93796cad7b58dffa101013386432ef0547fbf24/U1T4/Imagens/natalrn.png)


## Resultados e Discussão

  
## Conclusão


## Formas de executar o código

O código completo está disponível neste repositório do Github. Para executar o código é recomendável usar o Google Colab, que já possui as bibliotecas necessárias. No caso do uso de outro ambiente, talvez seja necessário instalar algumas dessas bibliotecas.

## Link para a apresentação do código em vídeo

[**Youtube**](https://youtu.be/LzVxKbDd_Y8)

## Referências
https://github.com/gboeing/osmnx

https://osmnx.readthedocs.io/en/stable/getting-started.html

https://github.com/ivanovitchm/datastructure



