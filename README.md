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
