---
layout: post
title:  "Silly Notes about Data Engineering"
date:   2023-10-31 21:25:22 -0300
categories: jekyll update
---
Bem vindos a minha jornada como engenheiro de dados.

## Pipeline de dados ##
O engenheiro de dados é responsável por integrar, modelar e processar dados. Para esse processo, damos o conceito de *pipeline de dados*, que garante um dado pontual e íntegro.

## Dados transacionais ##
Dados transacionais são dados capturados de transações, podendo ser gerado por diversos aplicativos

## Dados analíticos ##
Os dados analíticos, como o nome sugere, surgem por meio de cálculos ou análises executadas nos dados transacionais.

## Dados mestres ##
Os dados mestres representam os objetos de negócios reais e críticos sobre os quais essas transações são realizadas, levando também em consideração os parâmetros com base nos quais a análise de dados é realizada.

## ETL ##
**Extract, transform, load**. É o processo de extrair dados de uma fonte (raw) transformar e carregar para um data-base.
![](https://learn.microsoft.com/pt-br/azure/architecture/data-guide/images/etl.png)

## ELT ##
**Extract, load, transform**. É o processo de transformar os dados diretamente no banco de dados, surgiu com o cloud computing e torna os dados mais escaláveis.
![](https://learn.microsoft.com/pt-br/azure/architecture/data-guide/images/elt.png)

## Analytics ##
O processo de análise de dados.