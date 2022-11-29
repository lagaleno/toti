# Aula 28/11/2022 - Python

## Praticar
- Loops
- Listas
- Tratamento de erros

## Exercício 1
Faça um Programa que peça 5 números inteiros, armazene-os em uma lista e mostre-os na ordem inversa.
Exemplo:
```
Entrada: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Saída: [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```
OBS: lembre-se de usar função e tratamento de erro


### Objetivos:
- Exercitar criação de listas
- Loops

### Possível respsota:
```
def inverte_lista(lista):
  lista_invertida = []
  for i in range(len(lista), 0, -1):
    lista_invertida.append(i)

  return lista_invertida
  
try:
  lista_entrada = []
  i = 0
  while i < 5:
    elemento = int(input("Entre com o número "))
    lista_entrada.append(elemento)
    i = i + 1

  print(lista_entrada)
  lista_saida = inverte_lista(lista_entrada)
  print(lista_saida)

except Exception as error:
  print(error)
```

## Exercício 2
Faça um Programa que leia 10 números inteiros e armazene-os numa lista. Armazene os números pares na lista `par` e os números ímpares na lista `impar`. Imprima as três listas.

OBS: lembre de usar função e tratameto de erros

### Objetivos:
- Exercitar listas
- Exercitar retorno de função com mais de um elemento (tuplas)
- Condicional
- Loops

### Possível resposta
```
def analisa_paridade(lista):
  par = []
  impar = []
  for i in lista:
    if i % 2 == 0:
      par.append(i)
    else:
      impar.append(i)
  
  return par, impar
  
try:
  lista_entrada = []
  i = 0
  while i < 10:
    elemento = int(input("Entre com o número "))
    lista_entrada.append(elemento)
    i = i + 1

  print(lista_entrada)
  par, impar = analisa_paridade(lista_entrada)
  print(par)
  print(impar)

except Exception as error:
  print(error)
```

## Exercício 3
Faça um programa que leia um número indeterminado de valores, correspondentes a notas, encerrando a entrada de dados quando for informado um valor igual a -1 (que não deve ser armazenado). Após esta entrada de dados, faça:

  a. Mostre a quantidade de valores que foram lidos;

  b. Exiba todos os valores na ordem em que foram informados, um ao lado do outro;

  c. Exiba todos os valores na ordem inversa à que foram informados, um abaixo do outro;

  d. Calcule e mostre a soma dos valores;

  e. Calcule e mostre a média dos valores;

  f. Calcule e mostre a quantidade de valores acima da média calculada;

  g. Calcule e mostre a quantidade de valores abaixo de sete;

  h. Encerre o programa com uma mensagem;

OBS: lembre-se de usar tratamento de erro e funções

### Objetivos:
- Exercitar criação de lista
- Exercitar loops infinitos e breaks
- Exercitar funções de listas
- Exercitar loops
- Exercitar condicionais

### Possível resposta
```
def conta_elementos(lista):
  return len(lista)

def inverte_lista(lista):
  lista_invertida = []
  for i in range(len(lista)-1, -1, -1):
    lista_invertida.append(lista[i])

  return lista_invertida

def faz_soma(lista):
  return sum(lista)

def calcula_media(soma, qtd):
  return soma/qtd

def avalia_media(lista, media):
  acima_media = []
  for i in lista:
    if i > media:
      acima_media.append(i)

  return acima_media, len(acima_media)

def abaixo_sete(lista):
  lista_temp = []

  for i in lista:
    if i < 7:
      lista_temp.append(i)

  return lista_temp, len(lista_temp)


try:
  lista_entrada = []
  while True:
    elemento = float(input("Entre com o número "))
    if elemento == -1:
      break;
    lista_entrada.append(elemento)

  
  # quantidade elementos
  qtd_elementos = conta_elementos(lista_entrada)
  print("Quantidade de elementos", qtd_elementos)

  # imprime elementos
  print(lista_entrada)

  # imprime elementos na ordem inversa
  lista_invertida = inverte_lista(lista_entrada)
  print(lista_invertida)

  # soma dos valores
  soma = faz_soma(lista_entrada)
  print('Soma dos elementos', soma)

  # calcula média
  media = calcula_media(soma, qtd_elementos)
  print("Média ", media)

  # avalia media
  acima_media, qtd = avalia_media(lista_entrada, media)
  print("Tem ", qtd, " de valores acima da média que são ", acima_media)

  # avalia abaixo de sete
  lista_abaixo_sete, qtd = abaixo_sete(lista_entrada)
  print("Tem ", qtd, " de valores abaixo de sete que são ", lista_abaixo_sete)

  # encerra o programa
  print("Encerrando o programa")

except Exception as error:
  print(error)

```

## Informações

- [Fonte dos exerícios](https://wiki.python.org.br/ExerciciosListas)
- [Google Colab com a resolução dos exercícios da aula](https://colab.research.google.com/drive/1fZ8fl5FG132Tr4XISEdwUObtLYt7PLN0?usp=sharing)