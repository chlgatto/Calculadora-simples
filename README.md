# Calculadora simples
num1 = 0
num2 = 0
Resultado = 0
operacao = ''

while True:
    try:
        num1 = int(input('Digite o numero 1: '))
        operacao = input('Digite a operacao (+, -, *, /): ')
        num2 = int(input('Digite o numero 2: '))

        if operacao == '+':
            Resultado = num1 + num2
        elif operacao == '-':
            Resultado = num1 - num2
        elif operacao == '*':
            Resultado = num1 * num2
        elif operacao == '/':
            if num2 != 0:  # Verificar divisão por zero
                Resultado = num1 / num2
            else:
                print('Erro: Divisão por zero não é permitida.')
                continue
        else:
            print('Operação inválida. Tente novamente.')
            continue

        print(f'{num1} {operacao} {num2} = {Resultado}')

    except ValueError:
        print('Erro: Insira valores numéricos válidos.')
