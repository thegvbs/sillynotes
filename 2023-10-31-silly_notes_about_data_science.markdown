## Olá, mundo! ##

Dias atrás decidi finalmente tirar da estante e ler o livro **Data Science do Zero** de Joel Grus.
Pensei que documentar algumas partes, poderia ajudar em revisões e alguns iniciantes na área. Dito isto, proponho proponho abordar os seguintes assuntos/capítulos da obra original (_clique em qualquer um deles para ler_):

1. [Curso intensivo de Python](#curso-intensivo-de-python)
2. [Visualizando Dados (matplotlib)]()
4. [Álgebra Linear]()
9. [Obtendo Dados]()
11. [Aprendizado de Máquina]()
21. [Processamento de Linguagem Natural(**NLP**)]()
24. [Banco de Dados e SQL]()
25. [MapReduce]()

Já vou adiantando que a ciência de dados é a habilidade estatística e matemática usada para criar ideias de negócios a partir de dados, indico [este artigo](https://aws.amazon.com/pt/what-is/data-science/). 
## Curso Intensivo de Python
Primeiramente, é necessário baixar o Python e você pode fazer isso no site do [Python](https://www.python.org).
Eu recomendo também, ler a documentação oficial de boas práticas do Python [(pep8)](https://pep8.org/), usaremos ela.

## Ambientes virtuais e pip
Não crie o mau hábito de usar a instalação padrão do Python para todos seus projetos.
Para separar seus projetos, facilitar o uso de versões de bibliotecas e até do Python, existe o *venv*.
Para criar um ambiente virtual, digite no terminal: 
<pre class="highlight"><code>python -m venv nomedoprojeto </code></pre>

Dentro desse ambiente virtual você pode instalar bibliotecas através do *pip*, o gerenciador de pacotes do Python. Ele vem instalado junto com o Python e para usá-lo, digite no terminal:
<pre class="highlight"><code> pip install nomedopacote </code></pre>
## Funções ## 
Funções ou módulos, são regras que recebem argumentos (entradas) e retornam uma saída.


<pre class="highlight"><code>def funcao(idade):
&nbsp;return 21</code></pre>

 Ao chamar função(), ela irá printar 21.

## Strings ##
Strings são cadeias de caracteres, definidas por aspas simples ou duplas:

<pre class="highlight"><code>nome = "Gabriel"
sobrenome = "Francisco"</code></pre>

## Listas
Lista ou em outras linguagens simplesmente *array*, é uma coleção de dados ordenados:

<pre class="highlight"><code>numeros = [1,2,3]</code></pre>

Para pegar uma posição da lista utilize colchetes:

<pre class="highlight"><code>numeros[0]</code></pre> retornará 1, pois as listas iniciam na posição 0

<pre class="highlight"><code>numeros[1]</code></pre> retornará 2

<pre class="highlight"><code>numeros[2]</code></pre> retornará 3

## Tuplas ## 
Parecidas com as listas, porém não são manipuláveis. 

<pre class="highlight"><code>tupla = (1,2,3)</code></pre>

## Dicionários
Dicionário ou dict, é uma estrutura de chave e valor.

<pre class="highlight"><code>gabs = {'Nome': 'Gabriel', 'Idade': 21}</code></pre>

Se for pegar um valor, use o método .get():

<pre class="highlight"><code>pega_nome = gabs.get('Nome')</code></pre> retorna Gabriel.

<pre class="highlight"><code>pega_idade = gabs.get('Idade')</code></pre> retorna 21.

## Fluxo de Controle
São ações condicionais.

<pre class="highlight"><code>if 1 > 2:
    &nbsp;print('Algo está errado, isso não faz sentido.')
    elif 1 > 3:
    &nbsp;print('Houston, we got a problem!)
    else:
    &nbsp;print('As coisas parecem em ordem por aqui!')
</code></pre>

Você também pode fazer isso em uma linha só:
<pre class="highlight"><code>paridade = "par" if x % 2 == 0 else "impar"</code></pre>

Em alguns casos usamos o loop *while*:
<br>
<pre class="highlight"><code>x = 0 
<br>while x < 10:
<br>&nbsp;print(f"{x} é menor que 10")
<br>&nbsp;x += 1
</code></pre>
Porém o mais comum é usarmos *for* e *in*
<pre class="highlight"><code>for x in range(10):
<br>&nbsp;print(f"{x} is less than 10")
<br>&nbsp;x += 1
</code></pre>

## Veracidade
Os booleanos funcionam como na maioria das linguagens, porém com letras maiúsculas. 

<pre class="highlight"><code>1 < 2  # Retorna True
1 > 10  # Retorna False</code></pre>

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
<pre class="highlight"><code> s = funcao()
&nbsp;if s:
&nbsp; first_char = s[0]
else:
&nbsp;firtst_char = ""
</code></pre>
Uma outra forma de fazer o bloco código acima é:
<pre class="highlight"><code> first_char = s and s[0] </code></pre>

O and retorna um segundo valor quando o primeiro é verdadeiro, e o primeiro quando ele não é.

## Classificação
Em Python, toda lista possui um método (função) *sort* que a organiza.

<pre class="highlight"><code>x = [4,1,2,3]
<br>x.sort()</code></pre> agora a lista é [1, 2, 3, 4]

Por padrão, o método organiza os elementos do menor para o maior, se quiser inverter a ordem você pode usar o parâmetro reverse=True.

<pre class="highlight"><code>x = sorted([-4, 1, -2, 3], reverse=True)</code></pre>

## Compreensão de Listas 
Para transformar uma lista em outra, você deve selecionar alguns elementos, transfórmá-los, ou ambos.

<pre class="highlight"><code>pares  = [x for x in range(5) if x % 2 == 0]</code></pre>
retorna [0, 2, 4]

<pre class="highlight"><code>raiz_qd = [x * x for x in range(5)]</code></pre>  
retorna [0, 1, 4, 9, 16]

<pre class="highlight"><code>pares_raiz_qd = [x * x for x in pares]</code></pre>

retorna [0, 1, 4, 9, 16]
## Testes Automatizados e asserção 
Como confirmar que um código de um cientista de dados está correto? Uma opção são os tipos (veremos logo a frente); mas há também os *testes automatizados*.
Existem frameworks sofisticados para testes, mas iremos usar apenas as instruções assert [asserção] para que o código gere um *AssertionError* caso a condição solicitada não seja verdadeira.

<pre class="highlight"><code>def smallest(xs):
&nbsp;return min(xs)

assert smallest([10, 20, 5, 40]) == 5
assert smallest([1, 9, -1, 2]) == -1
</code></pre>


## Programação Orientada a Objetos (POO)
Para encapsular dados e suas respectivas funções, podemos usar *classes*. De vez em quando usaremos esse recurso para deixar o código mais limpo e simples. 

<pre class="highlight"><code>class ContaClicks:
"""A classe deve ter um docstring, como as funções"""
</code></pre>
 
Uma classe contém zero ou mais métodos. Cada função recebe um parâmetro, self, que se refere a instância da classe específica.
Em geral, a classe tem um construtor chamado _init_, que recebe todos os parâmetros necessários para construir uma instância da classe e implementa as configurações

<pre class="highlight"><code>def __init__(self, count):
    self.count = count
</code></pre>

Embora o construtor tenha um nome engraçado, criamos as instâncias do contador usando apenas o nome da classe:

<pre class="highlight"><code>clicker1 = CountingClicker()
clicker2 = CountingClicker(100) # começa em count = 100
</code></pre>

Métodos "mágicos" ou métodos com duplo sublinhado, são chamados de "dunder" (double-underscore) e representam comportamentados especiais. Como por exemplo os métodos mágicos init e repr.

## Iteráveis e Geradores
Geradores podem ser iterados como listas , mas são lentos e geram apenas os valores solicitados.
É possível criar geradores usando funções e o operador yield.
<pre class="highlight"><code>def generate_range(n):
i = 0
while i < n:
    yield i #cada chamada para yield produz um valor do gerador
    i += 1 
</code></pre>

O loop a seguir consumirá cada um dos valores gerados pelo yield até que não sobre nenhum:
<pre class="highlight"><code>def generate_range(n):
for i in generate_range(10)
    print(f"i: {i}")
</code></pre>
Em geral, quando iteramos em uma lista ou um gerador, não queremos obter apenas os valores mas também seus índices. Nesse caso, o Python tem a função enumerate, que transforma os valores em pares (index, value):

<pre class="highlight"><code>names = ["Alice", "Bob", "Charlie", "Debbie"]
for i, name in enumerate(names):
    print(f"name {i} is {name}")
</code></pre>
Usaremos bastante este recurso.

## Aleatoriedade 
Durante o curso precisaremos gerar números aleatórios e isso pode ser feito com a função random:
<pre class="highlight"><code>import random
random.seed(10)
four_uniform_randoms = [random.random() for _ in range(4)]
</code></pre>
O módulo random produz números pseudoaleatórios (ou seja, determinísticos) com base em um estado interno que você pode definir com random.seed para obter resultados reproduzíveis.
Às vezes, usaremos o random.randrange, que recebe um ou mais argumentos e retorna um elemento escolhido aleatoriamente no range correspondente.
<pre class="highlight"><code>random.randrange(10) # [0,1, ..., 9]
random.randrange(3, 6) # [3,4,5]
</code></pre>
Outros métodos, como o random.shuffle reordenam aleatoriamente os elementos de uma lista:
<pre class="highlight"><code>up_to_five = [1, 2, 3, 4, 5]
random.shuffle(up_to_five)
print(up_to_five)
</code></pre>

Para escolher aleatoriamente um elemento de uma lista, você pode usar o random.choice:
<pre class="highlight"><code>best_friend = random.choice(["Alice, "Bob", "Charlie"])
</code></pre>

E, para escolher aleatoriamente uam amostra de elementos sem substituição (especialmente, sem repetição), você pode usar o random.sample:
<pre class="highlight"><code>lottery_numbers = range(60)
winning_numbers = random.sample(lottery_numbers) # [16, 36, 10, 6, 25, 9]
</code></pre>

## Expressões Regulares
As expressões regulare são uma forma de procurar texto 
<pre class="highlight"><code>import re
re_examples = [
    re.search("a", "cat"), # procura 'a' em 'cat'
    not re.search("c", "dog")] # '  dog' não possui 'c'
assert all(re_examples)</code></pre>

## zip e Descompactação de Argumentos ##
Muitas vezes teremos que compactar duas ou mais listas.
Devido ao zip ser lento devemos fazer um _for_ para acelerar as coisas.
<pre class="highlight"><code>lista1 = ['a', 'b', 'c']
lista2 = [1, 2, 3]
[pair for pair in zip([lista1, lista2])</code></pre>

## args e kwargs 
`*Args` e `**kwargs` permitem que você passe um número não especificado de argumentos para uma função.
<pre class="highlight"><code>def magic(*args, **kwargs):
    print("unamed args:", args)
    print("keyword args:", kwargs</code></pre>

## Anotações de Tipo
O Python é uma linguagem _tipada dinamicamente_. Ou seja, ele geralmente não liga com os tipos dos objetos se forem utilizados de forma válida:
<pre class="highlight"><code>def add(a, b)
    return a + b
assert add (10, 5) == 15,
assert add([1, 2] [3]) == [1, 2, 3]

try:
    add(10, "five")
except TypeError:
    print("Não é possível somar um inteiro com string")</code></pre>

Já em uma linguagem tipada estaticamente, as funções e objetos tem tipos específicos:
<pre class="highlight"><code>def add(a: int, b: int) -> int:
    return a + b

add(10, 5)
add("Olá", "mundo")</code></pre>                        