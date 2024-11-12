# Caixa-eletronico
deposito = 0
saque = 0
saldo = 0
condicao = input("Deseja usar o caixa? \n")
while condicao == "sim":
    entrada = input('Qual a operação? \n' )
    if entrada == 'saque' and entrada.isdigit:
        saque = int(input('Qual o valor do saque?\n'))
        if saque > saldo:
            print(f'Saldo insufiente valor do saque é R${saque:.2f} seu saldo e R${saldo:.2f}') 
            condicao = input("Deseja Fazer outra operação?\n")
            if condicao == "sim":
               print('posso ajudar? ')
            else:
              print('Ate mais')
              break
        elif saque < saldo:
            saldo = saldo - saque
            print(f'Valor do saque e R${saque:.2f} seu saldo é R${saldo:.2f}') 
            condicao = input("Deseja Fazer outra operação?\n")
            if condicao == "sim":
               print('posso ajudar? ')
            else:
              print('Ate mais')    
              break    
    elif entrada =='deposito' :
         valor_deposito = float(input('Qual o valor do deposito? '))
         saldo = saldo + valor_deposito
         print(f'O valor do deposito foi R${valor_deposito:.2f} seu saldo atual é {saldo:.2f}')
         condicao = input("Deseja Fazer outra operação?\n") 
         if condicao == "sim":
              print('posso ajudar? ')
         else:
              print('Ate mais')    
              break  
    elif entrada == 'consulta' :
            print(f'Seu Saldo é R${saldo:.2f}')
            condicao = input("Deseja Fazer outra operação? \n") 
print(f'Obrigado e volte sempre!!!"')        


