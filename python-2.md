# Aula 21/11/2022 - Python

## Praticar
- Criação de funções
- Booleanos e expressões lógicas
- Condicional
- Loops

## Exercício 1

Faça um programa que peça um número inteiro e informe ao usuário se é par ou ímpar.

`O número informado é [par ou ímpar]`

### Objetivos:
- Operações matemáticas 
- Condicionais

### Possível respsota:
```
def checkParidade(num):

  if num % 2 == 0:
    return "é par"
  return "é ímpar"

num = int(input("Entre com o número que deseja saber a paridade "))
print("O número informado", checkParidade(num))
```

## Exercício 2

Faça um programa que solicite o nome do usuário e imprima-o na vertical. Exemplo:

Entrada:
`FULANO`
Saída:
```
F
U
L
A
N
O
```

### Objetivos:
- Exercitar Strings
- Uso de Loops

### Possível resposta
```
def imprime_vertical(string):

  for letra in string:
    print(letra)

string = input("Entre com seu nome ")
imprime_vertical(string)
```

## Exercício 3

Faça um programa que peça um numero inteiro positivo e em seguida mostre este numero invertido. Saída:
Entrada:
```
12376489
```
Saída
```
98467321
```

### Objetivos:
- Trabalhar com números inteiros
- Trabalhar com strings
- Exercitar Loops

### Possível resposta
```
def inverte_numero(num):
  num_str = str(num)

  reverse_str = ''

  for i in range(len(num_str) - 1, -1, -1):
    reverse_str = reverse_str + num_str[i]
  
  return reverse_str

num = int(input("Entre com o seu número inteiro "))
print(inverte_numero(num))
```

## Exercício 4

 Um palíndromo é uma seqüência de caracteres cuja leitura é idêntica se feita da direita para esquerda ou vice−versa. Por exemplo: OSSO e OVO são palíndromos. Faça um programa que uma palavra ao usuário e retorne dizendo se são palíndromos ou não.


### Objetivos:
- Praticar strings
- Exercitar o uso de funções
- Exercitar o uso de Condicionais
- Exercitar o uso de Loops
  
### Possível resposta
```
def check_palindromo(string):

  indice_reverso = len(string) - 1
  
  for i in range(len(string)):
    if string[i] != string[indice_reverso - i]:
      return "Não é palíndromo"

  return "É palíndromo"


string = input("Entre com a string que quer checar ")
print(check_palindromo(string))
```

## Informações

- [Fonte dos exerícios de condicional](https://wiki.python.org.br/EstruturaDeDecisao)
- [Fonte dos exercícios de Loops com strings](https://wiki.python.org.br/ExerciciosComStrings)
- [Fonte dos exercícios de Loops](https://wiki.python.org.br/EstruturaDeRepeticao)
- [Google Colab com a resolução dos exercícios da aula](https://colab.research.google.com/drive/1Suqiuk9f_6kSrtGRa0xwMoDuNCWrvz_C?usp=sharing)