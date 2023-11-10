---
layout: post
title:  "Silly Notes about Data Science from Scratch"
date:   2023-10-31 21:25:22 -0300
categories: jekyll update
---
## Olá, mundo ##

Dias atrás decidi finalmente tirar da estante e ler o livro **Data Science do Zero** de Joel Grus.
Pensei que documentar meu aprendizado poderia ajudar em revisões e alguns iniciantes na área. 
Neste livro utilizamos a linguagem Python pois dispõe de inúmeras bibliotecas e é nossa favorita.

Ciência de dados é a habilidade estatística e matemática usada para criar ideias de negócios a partir de dados, indico [este artigo](https://aws.amazon.com/pt/what-is/data-science/). 

## Iniciando ##
Primeiramente, é necessário baixar o Python e você pode fazer isso no site do [Python](https://www.python.org).
Eu recomendo também, ler a documentação oficial de boas práticas do Python [(pep8)](https://pep8.org/), usaremos elas.

## Ambientes virtuais e pip ##
Não crie o mau hábito de usar a instalação padrão do Python para todos seus projetos.
Para separar seus projetos, facilitar o uso de versões de bibliotecas e até do Python, existe o *venv*.
Para criar um ambiente virtual, digite no terminal: <code>python -m venv nomedoprojeto </code>

Dentro desse ambiente virtual você pode instalar bibliotecas através do *pip*, o gerenciador de pacotes do Python. Ele vem instalado junto com o Python e para usá-lo, digite no terminal: <code> pip install nomedopacote </code>
## Funções ## 
Funções ou módulos, são regras que recebem argumentos (entradas) e retornam uma saída.
<code> def funcao(idade):<br>
    &nbsp;return 21
 </code>

 Ao chamar a função ela irá printar 21.

## Strings ##
Strings são cadeias de caracteres, definidas por aspas simples ou duplas:

<code> nome = "Gabriel" </code>

<code> sobrenome = "Francisco" </code>

## Listas ## 
Lista ou em outras linguagens simplesmente *array*, é uma coleção de dados ordenados:

<code> numeros = [1,2,3] </code>

Para pegar uma posição da lista utilize colchetes:

<code> numeros[0]</code> retornará 1, pois as listas iniciam na posição 0

<code> numeros[1]</code> retornará 2

<code> numeros[2]</code> retornará 3

## Tuplas ## 
Parecidas com as listas, porém não são manipuláveis. 

<code>tupla = (1,2,3)</code>

## Dicionários ##
Dicionário ou dict, é uma estrutura de chave e valor.

<code> gabs = {'Nome': 'Gabriel', 'Idade': 21}</code>

Se for pegar um valor, use o método .get():

<code>pega_nome = gabs.get('Nome')</code> retorna Gabriel.

<code>pega_idade = gabs.get('Idade')</code> retorna 21.

## Fluxo de Controle ##
São ações condicionais.

<code>if 1 > 2:
    <br>&nbsp;print('Algo está errado, isso não faz sentido.')
    <br>elif 1 > 3:
        <br>&nbsp;print('Houston, we got a problem!)
    <br>else:
        <br>&nbsp;print('As coisas parecem em ordem por aqui!')
        </code>
<br><br>Você também pode fazer isso em uma linha só:
<br><code> paridade = "par" if x % 2 == 0 else "impar" </code>

Em alguns casos usamos o loop *while*:
<br>
<code> x = 0 
<br>while x < 10:
<br>&nbsp;print(f"{x} é menor que 10")
<br>&nbsp;x += 1
</code>
<br><br>Porém o mais comum é usarmos *for* e *in*
