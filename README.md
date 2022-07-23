# TESTE TARGT 2

print('_'*30)

print('Sequência de Fibonacci')

print('_'*30)

n = int(input('Insira um numero para gerar a sequência de Fibonnaci: '))

t1 = 0

t2 = 1

print('~'*30)

print('{} -> {}'.format(t1, t2), end = '')

cont = 3

while cont <= n:

   t3 = t1 + t2

   print('-> {}'.format(t3), end = '')

   t1 = t2

   t2 = t3

   cont += 1

print('-> FIM'




TESTE TARGT 3

import json

f = open('answers/assignment 3/dados.json')

dados = json.load(f)

aux = 0
maior = 0
menor = 0
soma = 0
media = 0


for dia in dados:

    if (dia['valor']) != 0:
        aux = dia['valor']

        if (aux > maior):
            maior = aux

        if(menor == 0):
            menor = aux
        elif (aux < menor):
            menor = aux

        soma += dia['valor']

print('O maior valor de faturamento do mês foi: R$ ' + str(maior) + '.')
print('O menor valor de faturamento do mês foi: R$ ' + str(menor) + '.')


media = soma / len(dados)

diasFaturamento = ''

for i in dados:
    if (i['valor']) != 0:
        if (i['valor']) > media:
           diasFaturamento += (str(i['dia']) + ' ')
        
print('Os dias em que o faturamento foi maior que a média mensal foram: ' + diasFaturamento)



TESTE TARGT 4

e = ['SP', 'RJ', 'MG', 'ES', 'OUTROS']

faturamento = list()
for c in e:
    while True:
        try:
            v = float(input(f'Digite o faturamento mensal de {c}: '))
            if v < 0:
                print('\033[31mValor INVÁLIDO! Digite apenas valores maiores ou iguais a "0":\033[m')
            break
        except:
            print('\033[31mValor INVÁLIDO! Digite apenas valores reais!\033[m')

    faturamento.append(v)

faturamento_total = sum(faturamento)
print(f'\033[32mO faturamento total da Distribuidora foi: R$ {faturamento_total:.2f}'.replace('.', ','))

cont = 0
for i in faturamento:
    cont += 1
    percentual = ((i / faturamento_total) * 100)
    print(f'O percentual de faturamento de {e[cont - 1]} é: {percentual:.2f} %')
    



TESTE TARGT 5    


print("--- Inversor de palavras ---")

palavra = input("Digite uma palavra:")

caracteres = []

inverse = ''

for letra in palavra:
    caracteres.append(letra)

tam = len(caracteres) - 1

while tam >= 0:
    inverse += (caracteres[tam])
    tam -= 1

print("Palavra invertida: ")
print(inverse)
