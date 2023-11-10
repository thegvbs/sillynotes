---
layout: post
title:  "Silly Notes about Statistics"
date:   2023-10-31 21:25:22 -0300
categories: jekyll update
---
Aproveitando a temporada de leitura, também dediquei um tempo a algumas anotações do livro **Estatística Prática para Cientista de Dados** de Peter Bruce e Andrew Bruce, com o intuito de melhorar meu conhecimento em estatística e matemática.

## História ##
A matéria de estatística surgiu no século XX, a teoria das probabilidades -- fundamento matemático de estatística -- foi desenvolvida em XVII e XIX por Thomas Bayes, Pierre-Simon Laplace e Carl Gauss. A estatística moderna tem sua origem com Francis Galton no final de 1800. 
A estatística clássica é baseada na *inferência*, basicamente um conjunto de procedimentos para tirar conclusões de populações baseadas em amostras.
Em 1962, John W. Turkey -- criador dos termos bit e software -- propõe a análise de dados, colocando a inferência como apenas uma parte de um processo bem mais complexo.

## Dados estruturados ##
Lidamos com diversos tipos de dados e é **extremamente importante** saber com o que estamos trabalhando em ciência de dados, afinal esse é o maior desafio, transformar dados não estruturados em informação acessível.

## Glossário de tipos de dados ##
> Contínuos
<br>Dados que podem assumir qualquer valor em um intervalo.

> Discretos
<br>Dados que podem assumir valores numéricos (inteiro).

> Categóricos
<br>Dados podem assumir somente um conjunto específico de valores.
<br>Ex: Alabama, TV de LED, Plasma, LCD etc.

> Binários
<br>Dados categóricos que só assumem dois valores (0 ou 1, verdadeiro ou falso).

> Ordinais
<br>É um dado categórico que possui ordem explícita.
<br>Ex: 1, 2, 3, 4 ou 5

Declarar os tipos de dados melhora seu desempenho computacional e como o software processa os cálculos.

## Dados retangulares ##
Dado retangular é uma planilha ou tabela de um banco de dados  (ou matriz bidimensional com **linhas indicando registros** e **colunas indicando características**).

**Quadro de dados**
<br>Os dados retangulares (planilha) são a estrutura básica de dados para estatística e aprendizado de máquina.

**Característica**
<br>São as colunas na tabela.

**Registros**
<br>São as linhas na tabela.

<img>![Tabela](https://www.sqlshack.com/wp-content/uploads/2020/07/anatomy-of-a-sql-table-1.png)
Exemplo de tabela.

## Quadro de dados e Índices
Nas tabelas de bancos de dados relacionais, uma ou mais colunas são usadas como índices. O que facilita uma consulta em SQL posteriormente. Em Python, com a biblioteca pandas, a estrutura básica de dados retangulares é um objeto *DataFrame*. Por padrão, é atribuído um índice automático com base nos registros ao criar um *DataFrame*.

## Dados não retangulares ##
Estrutura de dados especiais, focados em um objeto como um vídeo, foto, texto, emoji, etc.

## Estimativas de localização ##
Variáveis com dados de medição ou contagem que podem ter milhares de valores diferentes. É importante definir um "valor típico" para cada característica.

**Média**
<br> A soma de todos os valores, dividida pelo número de valores.

**Média ponderada**
<br>A soma de todos os valores, multiplicada por um peso e dividida pela soma dos pesos

**Mediana**
<br>Valor que ocupa a posição central dos dados

**Mediana ponderada**
<br>Valor cuja posição está no centro da soma dos pesos, estando metade da soma antes e metade depois desse dado.

**Média aparada/truncada**
<br>A média de todos os valores depois da exclusão de um número fixos de valores extremos

**Outlier**
<br>Um valor de dados que é muito diferente da maioria dos dados.

Vamos nos aprofundar nas definições de cada estimativa.

## Média ##
A estimativa para localizar dados mais básica é a média, ou valor médio. A média é a soma de todos os valores, dividida pelo número de valores. Considere: {3 5 1 2}. A média é (3 + 5 + 1 + 2 ) / 4 = 11 / 4 = 2,75.
<br>Sua fórmula é: ![""](https://matematicabasica.net/wp-content/uploads/2019/02/definicao-media-aritmetica.png)
<br>O símbolo X̄ representa média de uma amostra de população. N (ou n) representa o número total de reigstros. **Em estatística, ele é maiúsculo se for referente a uma população e minúsculo se for referente a uma amostra de população. Em ciência de dados, a representação é indiferente.**

## Média aparada ##
É calculada excluindo um número fixado de valores selecionados em cada ponta , e então tirando uma média dos valores restantes.
<br>Sua fórmula é: ![''](https://miro.medium.com/v2/resize:fit:644/1*wsvNuI9WU05wr7tlf3URLg.png)
<br>Uma média aparada elimina a influência dos valores extremos.

## Média ponderada ##
Se calcula pela multiplicação de cada valor de dado xi por um peso wi e dividindo a somatória pela soma de todos os pesos.
<br>Sua fórmula é: ![""](https://matesnoaburridas.files.wordpress.com/2017/05/formula_media_ponderada.gif)

## Mediana ##
A mediana é o número central em uma lista de dados classificada. Se houver um número par de valores de dados, o valor central é aquele que não está realmente no  conjunto de dados, mas sim a média dos dois valores que dividem os valores classificados em superior e inferior. Digamos que queremos observar os rendimentos familiares em bairros próximos a Lake Washington, em Seattle.
Ao comparar o bairro Medina com o bairro Windermere, usando a média teríamos resultados muito distintos, pois Bill Gates mora em Medina. Porém, se usarmos a mediana, não importa a fortuna de Bill Gates -- pois a observação central será a mesma --.

## Outliers ##
Qualquer valor que seja muito distante dos outros valores observados em um conjunto de dados. Um outlier não torna o valor de um dado inválido ou errado (como no exemplo anterior com Bill Gates).
Ainda assim, um outlier costuma ser o resultado de erros de dados, como mistura de unidades diferentes. *Em qualquer caso, devem ser identificados e investigados.*

**Detecção de anomalias**
<br>Na detecção de anomalias, o ponto de interesse são os outliers para definir os valores "normais" dos dados.

## Estimativas de Localização de População e Taxas de Homicídio ##