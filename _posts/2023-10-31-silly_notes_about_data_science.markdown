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

<code>def funcao(idade):<br>
    &nbsp;return 21
 </code>

 Ao chamar função(), ela irá printar 21.

## Strings ##
Strings são cadeias de caracteres, definidas por aspas simples ou duplas:

<code>nome = "Gabriel"</code>

<code>sobrenome = "Francisco"</code>

## Listas ## 
Lista ou em outras linguagens simplesmente *array*, é uma coleção de dados ordenados:

<code>numeros = [1,2,3]</code>

Para pegar uma posição da lista utilize colchetes:

<code>numeros[0]</code> retornará 1, pois as listas iniciam na posição 0

<code>numeros[1]</code> retornará 2

<code>numeros[2]</code> retornará 3

## Tuplas ## 
Parecidas com as listas, porém não são manipuláveis. 

<code>tupla = (1,2,3)</code>

## Dicionários ##
Dicionário ou dict, é uma estrutura de chave e valor.

<code>gabs = {'Nome': 'Gabriel', 'Idade': 21}</code>

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
<br><code>paridade = "par" if x % 2 == 0 else "impar" </code>

Em alguns casos usamos o loop *while*:
<br>
<code>x = 0 
<br>while x < 10:
<br>&nbsp;print(f"{x} é menor que 10")
<br>&nbsp;x += 1
</code>
<br><br>Porém o mais comum é usarmos *for* e *in*

<code>
for x in range(10):
<br>&nbsp;print(f"{x} is less than 10")
<br>&nbsp;x += 1
</code>

## Veracidade ##
Os booleanos funcionam como na maioria das linguagens, porém com letras maiúsculas. 

<code> 1 < 2  # Retorna True</code>
<br>
<code> 1 > 10  # Retorna False</code>

O valor **None** indica um valor não existente, igual o **null** em outras linguagens.

x = None
assert x == None

No Python, você pode inserir qualquer valor que indique um booleano. Todos os valores abaixos são falsos.

- False
- None
- [] (lista vazia)
- {} (dict vazio)
- ""
- set()
- 0 
- 0.0

A maioria dos outros valores são tratados como True. Para iterar listas, strings ou dicts vazio, use *if*

<code> s = funcao()
<br>&nbsp;if s:
<br>&nbsp; first_char = s[0]
<br>else:
<br>&nbsp;firtst_char = ""

Uma outra forma de fazer o bloco código acima é:

<code> first_char = s and s[0] </code>

O and retorna um segundo valor quando o primeiro é verdadeiro, e o primeiro quando ele não é.

## Classificação ##
Em Python, toda lista possui um método (função) *sort* que a organiza.

<code>x = [4,1,2,3]
<br>x.sort()</code> agora a lista é [1, 2, 3, 4]

Por padrão, o método organiza os elementos do menor para o maior, se quiser inverter a ordem você pode usar o parâmetro reverse=True.

<code>x = sorted([-4, 1, -2, 3], reverse=True)</code>

## Compreensão de Listas ##
Para transformar uma lista em outra, você deve selecionar alguns elementos, transfórmá-los, ou ambos.

<code>pares  = [x for x in range(5) if x % 2 == 0]</code> retorna [0, 2, 4]

<code>raiz_qd = [x * x for x in range(5)]</code> retorna [0, 1, 4, 9, 16]

<code>pares_raiz_qd = [x * x for x in pares]</code> reto


## Testes Automatizados e asserção ## 
Como confirmar que um código de um cientista de dados está correto? Uma opção são os tipos (veremos logo a frente); mas há também os *testes automatizados*.
Existem frameworks sofistificados para testes, mas iremos usar apenas as instruções assert [asserção] para que o código gere um *AssertionError* caso a condição solicitada não seja verdadeira.

<code>
assert 1+1 == 2<br>assert 1 + 1 == 2, "Algo está errado, isso deveria ser 2".</code>