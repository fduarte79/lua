# Programação LUA

### Introduação
+ Linguagem de script;
+ mas pode ser executado no modo interativo;
+ execução: lua arquivo.lua;
+ case-sensitive
+ gerenciamento automático de memória e coleta d lixo;
+ sudo apt-get update && sudo apt-get install lua5.4
+ comentários: --

### Tipos de Dados
+ **nill**: nulo
+ number: numérico (inteiro ou real)
+ string: cadeia de caracteres
+ function: função
+ userdata
+ table
+ [[ ]]: string de múltiplas linhas
+ "': caractere de escape
+ function: dado tipo função
+ userdata: ponteiro
+ table: tabela

### Escopo de variáveis
Local: quando declarada dentro de um bloco  
Global: não precisa ser declarada  

### Atribuição
Normal: `var_a = 3`  
Múltipla: `var_a, var_b = 'Teste',  3.131415`  

### Operadores Aritméticos
`+`: soma  
`-`: subtração  
`*`: multiplicação  
`/`: divisão  
`-valor`: operador unário negativo  

### Operadores Relacionais
`<`: menor que  
`>`: maior que  
`<=`: menor que  
`>=`: maior que  
`==`: igual  
`~=`: diferente

### Operadores Lógicos  
`and`: e  
`or`: ou  
`not`: negação  

### Aplicação dos Operadores 
`..`: operador de concatenação para strings  
`<`, `<=`, `>`, `>=`: números e strings  
`~=`, `==`: compara número e string e retorna *nil* se falso, *1* se verdadeiro  

### Condicional
+ Se o condicional for verdadeiro, a cláusula é executada;
+ Se o condicional for falso, a cláusula não é executada e retorna *nil*.

**if**  
```
var = 1
if var > 0 then
  print('A')
end
```

**if-else**
```
var = 1
if var < 0 then
  print('A')
else
  print('B')
end
```

**if-elseif**  
```
var = 1
if var < 0 then
  print('A')
elseif var > 0 then
  print('B')
end
```

**if-elseif-else**
```
var = 1
if var < 0 then
  print('A')
elseif var < 1 then
  print('B')
else
  print('C')
end
```

### Laço de repetição While
+ o laço é executado enquanto a condicional for verdadeira
```
var = 3
while var >= 0 do
  print(var)
  var = var - 1
end
```

+ semelhante ao do-while em C, onde existe um laço de de repetição antes do condicional de parada
```
var = 3
repeat
  var = var - 1
until (var == 0)
print(var)
```

+ a linguagem de programação *Lua* não possui laços de repetição `for`

### Tabelas

+ implementam vetores associativos;
+ valores de todos tipos exceto, *nil*;
+ principal estrutura de dados da Lua;
+ a variável contém um ponteiro para o endereço da tabela;
+ devem ser criadas antes de serem utilizadas;
+ os elementos são separados por virgulas;
+ o primeiro elemento possui índice 1;
+ o elemento é acessado por meio do seu índice entre colchetes;
+ criando uma tabela vazia: `tabela_1 = {}`
+ para limpar uma tabela, basta atribuir o valor *nil*

```
> tab_1 = {1, 3.1141516, 'A', "Lua"}
> tab_1
table: 0x55c0c1e2c680
> tab_1[1]
1
> tab_1[2]
3.1141516
> tab_1[3]
A
> tab_1[4]
Lua
> tab_1[5]
nil
```
```
> tab_2 = {t1 = 4, t2 = 5}
> tab_2.t1
4
> tab_2.t2
5
```

### Funções

+ tipo: *function*;
+ é possível armazenar:
  + variáveis;
  + índices de tabelas;
  + parâmetros para outras funções;
  + retorno de funções;
  + Lua atribui o valor *nil* para argumentos que foram ignorados;
  + Se possui mais valores que argumentos, Lua desconsidera o excendete;
  + quando não se sabe o número de argumentos, após o último é possível adicionar `...` desta forma, você estará dizendo que o número de argumentos é variável;
+ valores do tipo:
   + *string* e *number* são passados por valor e possuem escopo local;
   + *table*, *function* e *userdata* são passados por referência;
+ `return` deve ser a última instrução da função;
+ chamada da função:
  + f(): para números
  + f {}: para tabelas
  + f "": para strings

Declarando a função:

```
function f(parâmetros)
end
```

 ou

```
f = function(parâmetros)
end
```

```
l = {1,2}

function exibe(a,b)
   print(a+b)
end

exibe(l[1],l[2])
```

Exemplos:

```
s = 'programação com Lua'

function exibe(arg)
   print(arg)
end

exibe(s)
```

### Funções Pré-definidas

+ `call(func, arg, [, mode])`: invoca uma função,passando os argumentos, e um parâmetro opciobal `p`, que empacota em uma tabela o retorno da invocação;
+ `loadfile`: carrega um arquivo;
+ `dofile(arg)`: recebe um nome de um arquivo como argumeto, abre e executa como um código
+ `dostring(arg)`: recebe uma string no argumento, e o executa como um código
+ `next(table, i)`: retorna o próximo elemento da tabela com índice i;
+ `nextvar(arg)`: enumera as variáveis que tiverem o nome no argumento;
+ `type(arg)`: recebe uma variavel no argumento e retorna o seu tipo;
+ `tonunber(n, b)`: recebe um número *n* como argumento, e o converte para a base *b*;
+ ``:
+ ``:

### Bibliotecas - Expressões Regulares

### Bibliotecas - Manipulação de Strings

### Bibliotecas - Funções Matemáticas

# Referências
+ [Manual de Referência de Lua 5.1](https://www.lua.org/manual/5.1/pt/manual.html)
+ [Lua 5.4 Reference Manual ](https://www.lua.org/manual/5.4/)
