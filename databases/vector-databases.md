---
title: "Vector Databases"
date: 2026-07-13
tags: ["databases", "vector-databases", "AI"]
---

Hoje li um texto sobre banco de dados vetoriais e no que ele difere de um comum banco transacional estilo SQL e onde essa diferenca e benefica em cenarios como AI, RAG e outros.

O texto comeca fazendo uma distincao de buscas comuns e eficazes em bancos transacionais como "Buscar emails de clientes nessas condicoes" e buscas como "documentos similares a este" ou "as secoes mais relevantes de um livro dado um topico".

Numa segunda etapa ele abre um parenteses para ja tirar algo que estava em minha mente durante a leitura "e quanto a busca por termos e ferramentas como Elastic Search?" e explica que busca semantica ainda e um desafio para bancos de dados tradicionais, exemplos como "como consertar cano estourado" teria pouca ou nenhuma similaridade com "Resolvendo problemas de encanamento residencial".

O autor chama isso de "keyword gap problem" pois ferramentas como elasticsearch tenta encontrar similaridade atraves de tokens mas nao entende contexto e semantica por tras. 

Na sessao seguinte do texto ja e abordado um pouco da base computacional da coisa: busca por vetores e como um banco vetorial busca. largando mao de uma busca classica para buscar um qualidade assintotica maior em buscas probabilisticas, mais especificamente o algoritmo "Approximate Nearest Neighbor (ANN)", e que apesar de entregar o resultado correto 95%~99% das vezes, para casos de uso como RAG e buscas semanticas e o suficiente.

Depois aborda como esses vetores podem ser indexados, citando algoritmos associados a computacao baseada e grafos como "Hierarchical Navigable Small World (HNSW)" e "Inverted File System (IVF)".

Por fim o autor conclui com erros comuns como "focar mais em banco de dados do que algoritmo de embedding".

Eu ja sabia que banco de dados baseado em grafos estavam sendo revisitados para RAG e busca semantica, mas ler esse texto me ajudou a relacionar cases de muito alto-nivel com a computacao real da coisa.