# Calculadora-em-Python
Nestes algoritmos presentes, utilizei operadores de pertencimento, aritméticos, comparação e condicionais. Além disso, foi utilizado o loop infinito (while), entrada com a função (input). Assim, foi usada também a conversão de dados.

    
    while True:
    numero_1 = input('Digite um número: ')
    numero_2 = input('Digite outro número: ')
    operador = input('Digite um operador (+-/*): ')
    
    numero_validos = None
    
    
    
    try:
        numero_1_int = int(numero_1)
        numero_2_int = int(numero_2)
        numero_validos = True
    except:
        numero_validos = None
            
    if numero_validos is None:
            print('Um ou ambos os números são inválidos.')
            continue    
        
    operador_valido = '+-/*'
    
    
    if  len (operador) > 1:
        print('Digite apenas um operador.')
        continue
    
    if operador not in operador_valido:
        print('O operador digitado não é válido.')
        continue
    if  operador == '+':
        resultado = numero_1_int+numero_2_int
    
        
        print(f'{calculo_em_andamento}: \n {resultado}')
        continue
    
    calculo_em_andamento = 'Seu claculo está sendo processado, confira o resultado abaixo.'
    
    if  operador == '-':
        resultado = numero_1_int-numero_2_int
        
        
        print(f'{calculo_em_andamento} \n {resultado}')
        continue
    
    if  operador == '*':
        resultado = numero_1_int*numero_2_int
        
        print(f'{calculo_em_andamento} \n {resultado}')
        continue
    
    if  operador == '/':
        resultado = numero_1_int/numero_2_int
        
        
        print(f'{calculo_em_andamento} \n {resultado}')
        continue
    
    sair = input('Quer sair? [s]im: ').lower().startswith('s')

    if sair is True:
        break
    
