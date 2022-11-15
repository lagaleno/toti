# Aula 14/11/2022 - Python

## Praticar
- Entrada e saída (`input()` e `print()`)
- Operações matemáticas básicas
- Tipos de dados
- Strings e suas operações

## Exercício 1

Faça um programa que peça um número inteiro e então imprima a mensagem

`O número informado foi [número]`

### Objetivos:
- Conceito de entrada e saída 
- Uso do `input()` com números
- Uso do `print()` concatenando informações

### Possível respsota:
```
num = int(input("Entre com o número "))

print("o número informado foi", num)
```

## Exercício 2

Faça um Programa que peça dois números e imprima a soma.

### Objetivos:
- Conceito de entrada e saída 
- Uso do `input()` com números
- Uso do `print()` concatenando informações
- Operação de soma

### Possível resposta
```
num1 = float(input("Entre com o primeiro número "))
num2 = float(input("Entre com o segundo número "))

soma = num1 + num2
print(soma)
```

## Exercício 3

Tendo como dados de entrada a altura de uma pessoa, construa um algoritmo que calcule seu peso ideal, usando a seguinte fórmula: `(72.7*altura) - 58`

### Objetivos:
- Conceito de entrada e saída 
- Uso do `input()` com números
- Uso do `print()` concatenando informações
- Operações matemáticas

### Possível resposta
```
altura = float(input("Entre com a sua altura (ex: 1.65) "))

peso_ideal = (72.7 * altura) - 58

print("Tendo a altura", altura, "seu peso ideal aproximado é:", peso_ideal)
```

## Exercício 4

Faça um programa que leia 2 strings e informe o conteúdo delas seguido do seu comprimento. Exemplo:

```
Entre com a string1: Brasil Hexa 2022
Entre com a string2: Brasil! Hexa 2022!
Tamanho de "Brasil Hexa 2022": 16 caracteres
Tamanho de "Brasil! Hexa 2022!": 18 caracteres
```

### Objetivos:
- Conceito de entrada e saída 
- Uso do `input()` com strings
- Uso do `print()` concatenando informações
- Operações com strings

### Possível resposta
```
string1 = input("Entre com a string1 ")
string2 = input("Entre com a string2 ")

len_string1 = len(string1)
len_string2 = len(string2)

print("Tamanho de", string1, ":", len_string1, "caracteres")
print("Tamanho de", string2, ":", len_string2, "caracteres")
```

## Informações

- [Fonte dos exerícios](https://wiki.python.org.br/EstruturaSequencial)
- [Fonte dos exercícios](https://wiki.python.org.br/ExerciciosComStrings)
- [Google Colab com a resolução dos exercícios da aula](https://colab.research.google.com/drive/17R8U0fSMVk-1mwbfivAJq3_1YdDrpP5g?usp=sharing)