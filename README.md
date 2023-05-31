# Soda-Machine-1

cedula2 = 0
cedula5 = 0
cedula10 = 0
cedula20 = 0
moeda1 = 0
moeda050 = 0
moeda025 = 0
moeda010 = 0
moeda005 = 0

while True:  
    
    adm = int(input("Selecione o tipo de usuário: \n 1 - Administrador \n 2 - Consumidor \n 3 - Sair \n "))
    if adm == 1:
        while True:
            senha = int(input("Digite 1 para digitar a senha ou 2 para voltar \n "))
            if senha == 1:
                senha = str(input("Digite a senha:"))
                if senha != '1234':
                    print("Senha inválida!")
                    break
                else:
                    while True:
                        print("\nBem vindo ADM!\n\nValores disponíveis:")
                        print("Quantidade de cédulas de R$2,00 :", cedula2, "Valor total: R$", cedula2*2)
                        print("Quantidade de cédulas de R$5,00 :", cedula5, "Valor total: R$", cedula5*5)
                        print("Quantidade de cédulas de R$10,00:", cedula10, "Valor total: R$", cedula10*10)
                        print("Quantidade de cédulas de R$20,00:", cedula20, "Valor total: R$", cedula20*20)
                        print("Quantidade de moedas de R$1,00  :", moeda1, "Valor total: R$", moeda1*1)
                        print("Quantidade de moedas de R$00,50 :", moeda050, "Valor total: R$", moeda050*0.50)
                        print("Quantidade de moedas de R$00,25 :", moeda025, "Valor total: R$", moeda025*0.25)
                        print("Quantidade de moedas de R$00,10 :", moeda010, "Valor total: R$", moeda010*0.10)
                        print("Quantidade de moedas de R$00,05 :", moeda005, "Valor total: R$", moeda005*0.05)
                        
                        opcaoAdm = str(input("Escolha a opção desejada? \n1 - Atualizar quantidades \n2 - Voltar\n"))
                        if opcaoAdm == '2':
                            break
                        elif opcaoAdm == '1':
                            print("Escolha a moeda a ser alterada?")
                            
                            print("  2 - Cédulas de R$2,00")
                            print("  5 - Cédulas de R$5,00")
                            print(" 10 - Cédulas de R$10,00")
                            print(" 20 - Cédulas de R$20,00")
                            print("  1 - Medas de R$1,00")
                            print("050 - Moedas de R$0,50")
                            print("025 - Moedas de R$0,25")
                            print("010 - Moedas de R$0,10")
                            print("005 - Moedas de R$0,05")
                            print("X - Voltar")
                            menuMoeda = str(input("Escolha a opção desejada para atualizar a quantidade ou X para Voltar\n"))
                            if (menuMoeda == 'X' or menuMoeda == 'x'):
                                continue
                            elif menuMoeda == '2':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$2,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X' or qtdeMoeda =='x':
                                        continue
                                    else:
                                        cedula2 =  cedula2 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$2,00 é", cedula2,". Total em caixa R$:", cedula2*2)
                                        continue      
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$2,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X' or qtdeMoeda == 'x':
                                        continue
                                    else :
                                        if (cedula2 - int(qtdeMoeda) < 0):
                                            print("ATEÇÃO: Valor em caixa não pode ser negativo, tente novamente! Valores não atualizados!")
                                            print("Valores atuais em caixa:")
                                            print("---> Quantidade de cédulas de R$2,00 é", cedula2, ". Total em caixa R$:", cedula2*2) 
                                            continue
                                        else:
                                            cedula2 =  cedula2 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$2,00 é", cedula2, ". Total em caixa R$:", cedula2*2)   
                                            continue                                
                            elif menuMoeda == '5':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$5,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        cedula5 =  cedula5 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$5,00 é", cedula5,". Total em caixa R$:", cedula5*5)       
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$5,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        if (cedula5 - int(qtdeMoeda) < 0):
                                            print("Valor em caixa não pode ser negativo, tente novamente!")
                                            break
                                        else:
                                            cedula5 =  cedula5 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$5,00 é", cedula5, ". Total em caixa R$:", cedula5*5)  

                            elif menuMoeda == '10':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$10,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        cedula10 =  cedula10 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$10,00 é", cedula10,". Total em caixa R$:", cedula10*10)       
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$10,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        if (cedula10 - int(qtdeMoeda) < 0):
                                            print("Valor em caixa não pode ser negativo, tente novamente!")
                                            break
                                        else:
                                            cedula10 =  cedula10 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$10,00 é", cedula10, ". Total em caixa R$:", cedula10*10)

                            elif menuMoeda == '20':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$20,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        cedula20 =  cedula20 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$20,00 é", cedula2,". Total em caixa R$:", cedula20*20)       
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$20,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        if (cedula20 - int(qtdeMoeda) < 0):
                                            print("Valor em caixa não pode ser negativo, tente novamente!")
                                            break
                                        else:
                                            cedula20 =  cedula20 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$20,00 é", cedula20, ". Total em caixa R$:", cedula20*20)

                            elif menuMoeda == '1':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de moedas de R$1,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        moeda1 =  moeda1 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$1,00 é", moeda1,". Total em caixa R$:", moeda1*1)       
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$1,00 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        if (moeda1 - int(qtdeMoeda) < 0):
                                            print("Valor em caixa não pode ser negativo, tente novamente!")
                                            break
                                        else:
                                            moeda1 =  moeda1 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$1,00 é", moeda1, ". Total em caixa R$:", moeda1*1)


                            elif menuMoeda == '050':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de moedas de R$0,50 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        moeda050 =  moeda050 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$0,50 é", moeda050,". Total em caixa R$:", moeda050*0.50)       
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$0,50 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break

                                    else:
                                        if (moeda050 - int(qtdeMoeda) < 0):
                                            print("Valor em caixa não pode ser negativo, tente novamente!")
                                            break
                                        else:
                                            moeda050 =  moeda050 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$0,50 é", moeda050, ". Total em caixa R$:", moeda050*0.50)   


                            elif menuMoeda == '025':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de moedas de R$0,25 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        moeda025 =  moeda025 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$0,25 é", moeda025,". Total em caixa R$:", moeda025*0.25)       
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$0,25 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break

                                    else:
                                        if (moeda025 - int(qtdeMoeda) < 0):
                                            print("Valor em caixa não pode ser negativo, tente novamente!")
                                            break
                                        else:
                                            moeda025 =  moeda025 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$0,25 é", moeda025, ". Total em caixa R$:", moeda025*0.25)   


                            elif menuMoeda == '010':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de moedas de R$0,10 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        moeda010 =  moeda010 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$0,10 é", moeda010,". Total em caixa R$:", moeda010*0.10)       
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$0,10 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    
                                    else:
                                        if (moeda010 - int(qtdeMoeda) < 0):
                                            print("Valor em caixa não pode ser negativo, tente novamente!")
                                            break
                                        else:
                                            moeda010 =  moeda010 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$0,10 é", moeda010, ". Total em caixa R$:", moeda010*0.10)   


                            elif menuMoeda == '005':
                                menuOpcaoMoeda = str(input("Escolha a opção desejada? \n1 - Adicionar quantidades \n2 - Remover quantidades \n3 - Voltar\n"))
                                
                                if menuOpcaoMoeda == '1':
                                    qtdeMoeda = str(input("Digite a quantidade de moedas de R$0,05 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break
                                    else:
                                        moeda005 =  moeda005 + int(qtdeMoeda)
                                        print("Valor atualizado para:")
                                        print("---> Quantidade de cédulas de R$0,05 é", moeda005,". Total em caixa R$:", moeda005*0.05)       
                                elif menuOpcaoMoeda == '2':
                                    qtdeMoeda = str(input("Digite a quantidade de Cédulas de R$0,05 ou X para Voltar\n"))
                                    if qtdeMoeda == 'X':
                                        break

                                    else:
                                        if (moeda005 - int(qtdeMoeda) < 0):
                                            print("Valor em caixa não pode ser negativo, tente novamente!")
                                            break
                                        else:
                                            moeda005 =  moeda005 - int(qtdeMoeda)
                                            print("Valor atualizado para:")
                                            print("---> Quantidade de cédulas de R$0,05 é", moeda005, ". Total em caixa R$:", moeda005*0.05)   


                            else:
                                print("Opção inválida!")     
                                
                        else:
                            print("Opção inválida!")     
                            
            else:
                break

    elif adm == 2:
        print("#" * 30)
        print("{:^30}".format("BEM-VINDO AO NICE SODA!"))
        print("#" * 30)
        while True:
            cod = int(input("\nInsira o código do produto: \n1 - Coca-cola \n2 - Pepsi \n3 - Soda  \n4 - Fanta\n"))

            if cod == 1:
                print("Você selecionou Coca-cola!")
                print("Valor é R$6,00")
                valor = 6
                break
            elif cod == 2:
                print("Você selecionou Pepsi!")
                print("Valor é R$10,00")
                valor = 10
                break
            elif cod == 3:
                print("Você selecionou Soda!")
                print("Valor é R$5,00")
                valor = 5
                break
            elif cod == 4:
                print("Você selecionou Fanta!")
                print("Valor é R$4,00")
                valor = 4
                break
            else:
                print("Código incorreto!")
                continue

        pagamento = int(input("O pagamento será em: \n1-Moedas \n2-Cédulas \n3-Moedas e cédulas\n"))
        quantCedula2 = 0
        quantCedula5 = 0
        quantCedula10 = 0
        quantCedula20 = 0
        quantMoeda1 = 0
        quantMoeda050 = 0
        quantMoeda025 = 0
        quantMoeda010 = 0
        quantMoeda005 = 0
        troco = False

        if pagamento == 1:
            total = 0
            troco = 0

            while True:
                quantMoeda1 = int(input("Insira a quantidade de moedas de R$1,00: "))
                total = quantMoeda1
                if total == valor:
                    moeda1+= quantMoeda1
                    print("Retire sua bebida!")
                    break
                elif total < valor:
                    quantMoeda050 = int(input("Insira a quantidade de moedas de R$0,50: "))
                    total += (quantMoeda050  * 0.5)
                    print("Você ja inseriu R$", total)

                    if total == valor:
                        moeda1+= quantMoeda1
                        moeda050+= quantMoeda050
                        print("Retire sua bebida!")
                        break
                    elif total < valor:
                        quantMoeda025 = int(input("Insira a quantidade de moedas de R$0,25: "))
                        total += (quantMoeda025  * 0.25)
                        print("Você ja inseriu R$", total)
                    
                        if total == valor:
                            moeda1+= quantMoeda1
                            moeda050+= quantMoeda050
                            moeda025+= quantMoeda025
                            print("Retire sua bebida!")
                            break
                        elif total < valor:
                            quantMoeda010 = int(input("Insira a quantidade de moedas de R$0,10: "))
                            total += (quantMoeda010  * 0.10)
                            print("Você ja inseriu R$", total)
                        
                            if total == valor:
                                moeda1+= quantMoeda1
                                moeda050+= quantMoeda050
                                moeda025+= quantMoeda025
                                moeda010+= quantMoeda010
                                print("Retire sua bebida!")
                                break
                            elif total < valor:
                                quantMoeda005 = int(input("Insira a quantidade de moedas de R$0,05: "))
                                total += (quantMoeda005  * 0.05)
                                print("Você ja inseriu R$", total)
                            
                                if total == valor:
                                    moeda1+= quantMoeda1
                                    moeda050+= quantMoeda050
                                    moeda025+= quantMoeda025
                                    moeda010+= quantMoeda010
                                    moeda005+= quantMoeda005
                                    print("Retire sua bebida!")
                                    break
                                elif total < valor:
                                    print("ATENÇÃO: Você ja inseriu R$", total,"Este valor é insuficiente para comprar o produto. Por favor recolha as moedas devolvidas e incie novamente!")
                                    break  
                                else:
                                    troco = True
                            else:
                                troco = True
                        else:
                            troco = True
                    else:
                        troco = True
                else:
                    troco = True

                if troco == True:
                    dinheiroCaixa = cedula2*2 + cedula5*5 +cedula10*10 +cedula20*20 + moeda050*0.50 + moeda025*0.25 + moeda010*0.10 + moeda005*0.05
                    precoProduto = valor
                    troco = total - precoProduto
                    
                    if troco > dinheiroCaixa:
                        print("Não há notas suficientes no caixa para dar o troco. Tente outa forma de pagamento!")
                        break
                    else:    
                        print("Você receberá de troco:")
                        moeda1+= quantMoeda1
                        moeda050+= quantMoeda050
                        moeda025+= quantMoeda025
                        moeda010+= quantMoeda010
                        moeda005+= quantMoeda005

                        contador = (total - valor) * 100
                        troco1 = 100
                        troco050 = 50
                        troco025 = 25
                        troco010 = 10
                        troco005 = 5

                        nota1 = int(contador / troco1)
                        contador = contador - (nota1 * troco1 )
                        if nota1 > 0:
                            moeda1 -= nota1

                        nota050 = int(contador / troco050)
                        contador = contador - (nota050 * troco050 )
                        if nota050 > 0:
                            moeda050 -= nota050

                        nota025 = int(contador / troco025)
                        contador = contador - (nota025 * troco025 )
                        if nota025 > 0:
                            moeda025 -= nota025

                        nota010 = int(contador / troco010)
                        contador = contador - (nota010 * troco010 )
                        if nota010 > 0:
                            moeda010 -= nota010
                            
                        nota005 = int(contador / troco005)
                        contador = contador - (nota005 * troco005 )
                        if nota005 > 0:
                            moeda005 -= nota005

                        print (nota1, "moedas de R$", troco1 / 100)
                        print (nota050, "moedas de R$", troco050 / 100)
                        print (nota025, "moedas de R$", troco025 / 100)
                        print (nota010, "moedas de R$", troco010 / 100)
                        print (nota005, "moedas de R$", troco005 / 100)
                    break
                                    
        elif pagamento == 2:
            while True:
                quantCedula2 = int(input("Insira a quantidade de cédulas de R$2,00: "))
                total = (quantCedula2 * 2)
                if total == valor:
                    cedula2+= quantCedula2 
                    print("Retire sua bebida!")
                    break
                elif total < valor:
                    quantCedula5 = int(input("Insira a quantidade de cédulas de R$5,00: "))
                    total += (quantCedula5 * 5)
                    print("Você ja inseriu R$", total)
                 
                    if total == valor:
                        cedula2+= quantCedula2
                        cedula5+= quantCedula5
                        print("Retire sua bebida!")
                        break
                    elif total < valor:
                        quantCedula10 = int(input("Insira a quantidade de cédulas de R$10,00: "))
                        total += (quantCedula10 * 10)
                        print("Você ja inseriu R$", total)
                    
                        if total == valor:
                            cedula2+= quantCedula2
                            cedula5+= quantCedula5
                            cedula10+= quantCedula10
                            print("Retire sua bebida!")
                            break
                        elif total < valor:
                            quantCedula20 = int(input("Insira a quantidade de cedulas de R$20,00: "))
                            total += (quantCedula20 * 20)
                            print("Você ja inseriu R$", total)
                        
                            if total == valor:
                                cedula2+= quantCedula2
                                cedula5+= quantCedula5
                                cedula10+= quantCedula10
                                cedula20+= quantCedula20
                                print("Retire sua bebida!")
                                break
                                
                            elif total < valor:
                                print("ATENÇÃO: Você ja inseriu R$", total,"Este valor é insuficiente para compara o produto. Por favor recolha as moedas devolvidas e incie novamente!")
                                break   
                            else:
                                troco = True
                        else:
                            troco = True
                    else:
                        troco = True
                else:
                    troco = True
                
                if troco == True:
                    dinheiroCaixa = cedula2*2 + cedula5*5 +cedula10*10 +cedula20*20 + moeda050*0.50 + moeda025*0.25 + moeda010*0.10 + moeda005*0.05
                    precoProduto = valor
                    troco = total - precoProduto
                    
                    if troco > dinheiroCaixa:
                        print("Não há notas suficientes no caixa para dar o troco. Tente outa forma de pagamento!")
                        break
                    else:
                        print("Você receberá de troco:")

                        cedula2+= quantCedula2
                        cedula5+= quantCedula5
                        cedula10+= quantCedula10
                        cedula20+= quantCedula20
                        
                        contador = (total - valor) * 100
                        troco20 = 2000
                        troco10 = 1000
                        troco5 = 500
                        troco2 = 200
                        troco1 = 100
                        troco050 = 50
                        troco025 = 25
                        troco010 = 10
                        troco005 = 5

                        nota20 = 0
                        nota10 = 0
                        nota5 = 0
                        nota2 = 0
                        nota1 = 0
                        nota050 = 0
                        nota025 = 0
                        nota010 = 0
                        nota005 = 0
                        
                        if cedula20 > 0:
                            nota20 = int(troco // 20)
                            if nota20 <= cedula20: 
                                troco = troco - (nota20 * 20 )
                                cedula20 = cedula20 - nota20
                            else:     
                                troco = troco - (cedula20 * 20 )
                                cedula20 = 0

                        if cedula10 > 0:
                            nota10 = int(troco // 10)
                            if nota10 <= cedula10:
                                troco = troco - (nota10 * 10 )
                                cedula10 = cedula10 - nota10
                            else:   
                                troco = troco - (cedula10 * 10 )
                                cedula10 = 0

                        if cedula5 > 0:
                            nota5 = int(troco // 5)
                            if nota5 <= cedula5: 
                                troco = troco - (nota5 * 5 )
                                cedula5 = cedula5 - nota5
                            else:     
                                troco = troco - (cedula5 * 5 )


                        if cedula2 > 0:
                            nota2 = int(troco // 2)
                            if nota2 <= cedula2: 
                                troco = troco - (nota2 * 2 )
                                cedula2 = cedula2 - nota2
                            else:     
                                troco = troco - (cedula2 * 2 )

                        if moeda1 > 0:
                            nota1 = int(troco // 1)
                            if nota1 <= moeda1: 
                                troco = troco - (nota1 * 1 )
                                moeda1 = moeda1 - nota1
                            else:     
                                troco = troco - (moeda1 * 1 )
                    
                        if moeda050 > 0:
                            nota050 = int(troco // 0.50)
                            if nota050 <= moeda050: 
                                troco = troco - (nota050 * 0.50 )
                                moeda050 = moeda050 - nota050
                            else:     
                                troco = troco - (moeda050 * 0.50 )
                        
                        if moeda025 > 0:
                            nota025 = int(troco // 0.25)
                            if nota025 <= moeda025: 
                                troco = troco - (nota025 * 0.25 )
                                moeda025 = moeda025 - nota025
                            else:     
                                troco = troco - (moeda025 * 0.25 )
                            
                        if moeda010 > 0:
                            nota010 = int(troco // 0.10)
                            if nota010 <= moeda010: 
                                troco = troco - (nota010 * 0.10 )
                                moeda010 = moeda010 - nota010
                            else:     
                                troco = troco - (moeda010 * 0.10 )
                        if moeda005 > 0:
                            nota005 = int(troco // 0.05)
                            if nota005 <= moeda005: 
                                troco = troco - (nota005 * 0.05 )
                                moeda005 = moeda005 - nota005
                            else:     
                                troco = troco - (moeda005 * 0.05 )

                        print (nota20, "notas de R$", troco20 / 100)
                        print (nota10, "notas de R$", troco10 / 100)
                        print (nota5, "notas de R$", troco5 / 100)
                        print (nota2, "notas de R$", troco2 / 100)
                        print (nota1, "moedas de R$", troco1 / 100)
                        print (nota050, "moedas de R$", troco050/ 100)
                        print (nota025, "moedas de R$", troco025 / 100)
                        print (nota010, "moedas de R$", troco010 / 100)
                        print (nota005, "moedas de R$", troco005 / 100)
                    
                    break
                
        elif pagamento == 3:
            total = 0
            while True:
                quantMoeda1 = int(input("Insira a quantidade de moedas de R$1,00: "))
                total = quantMoeda1
                if total == valor:
                    moeda1+= quantMoeda1
                    print("Retire sua bebida!")
                    break
                elif total < valor:
                    quantMoeda050 = int(input("Insira a quantidade de moedas de R$0,50: "))
                    total += (quantMoeda050  * 0.5)
                    print("Você ja inseriu R$", total)
                 
                    if total == valor:
                        moeda1+= quantMoeda1
                        moeda050+= quantMoeda050
                        print("Retire sua bebida!")
                        break
                    elif total < valor:
                        quantMoeda025 = int(input("Insira a quantidade de moedas de R$0,25: "))
                        total += (quantMoeda025  * 0.25)
                        print("Você ja inseriu R$", total)

                        if total == valor:
                            moeda1+= quantMoeda1
                            moeda050+= quantMoeda050
                            moeda025+= quantMoeda025
                            print("Retire sua bebida!")
                            break
                        elif total < valor:
                            quantMoeda010 = int(input("Insira a quantidade de moedas de R$0,10: "))
                            total += (quantMoeda010  * 0.10)
                            print("Você ja inseriu R$", total)

                            if total == valor:
                                moeda1+= quantMoeda1
                                moeda050+= quantMoeda050
                                moeda025+= quantMoeda025
                                moeda010+= quantMoeda010
                                print("Retire sua bebida!")
                                break
                            elif total < valor:
                                quantMoeda005 = int(input("Insira a quantidade de moedas de R$0,05: "))
                                total += (quantMoeda005  * 0.05)
                                print("Você ja inseriu R$", total)

                                if total == valor:
                                    moeda1+= quantMoeda1
                                    moeda050+= quantMoeda050
                                    moeda025+= quantMoeda025
                                    moeda010+= quantMoeda010
                                    moeda005+= quantMoeda005
                                    print("Retire sua bebida!")
                                    break
                                elif total < valor:
                                    quantCedula2 = int(input("Insira a quantidade de cédulas de R$2,00: "))
                                    total += (quantCedula2 * 2)
                                    print("Você ja inseriu R$", total)

                                    if total == valor:
                                        moeda1+= quantMoeda1
                                        moeda050+= quantMoeda050
                                        moeda025+= quantMoeda025
                                        moeda010+= quantMoeda010
                                        moeda005+= quantMoeda005
                                        cedula2+= quantCedula2
                                        print("Retire sua bebida!")
                                        break
                                    elif total < valor:
                                        quantCedula5 = int(input("Insira a quantidade de cédulas de R$5,00: "))
                                        total += (quantCedula5  * 5)
                                        print("Você ja inseriu R$", total)

                                        if total == valor:
                                            moeda1+= quantMoeda1
                                            moeda050+= quantMoeda050
                                            moeda025+= quantMoeda025
                                            moeda010+= quantMoeda010
                                            moeda005+= quantMoeda005
                                            cedula2+= quantCedula2
                                            cedula5+= quantCedula5
                                            print("Retire sua bebida!")
                                            break
                                        elif total < valor:
                                            quantCedula10 = int(input("Insira a quantidade de cédulas de R$10,00: "))
                                            total += (quantCedula10  * 10)
                                            print("Você ja inseriu R$", total)

                                            if total == valor:
                                                moeda1+= quantMoeda1
                                                moeda050+= quantMoeda050
                                                moeda025+= quantMoeda025
                                                moeda010+= quantMoeda010
                                                moeda005+= quantMoeda005
                                                cedula2+= quantCedula2
                                                cedula5+= quantCedula5
                                                cedula10+= quantCedula10
                                                print("Retire sua bebida!")
                                                break
                                            elif total < valor:
                                                
                                                quantCedula20 = int(input("Insira a quantidade de modedas de R$20,00: "))
                                                total += (quantCedula20  * 20)
                                                print("Você ja inseriu R$", total)
                                            
                                                if total == valor:
                                                    moeda1+= quantMoeda1
                                                    moeda050+= quantMoeda050
                                                    moeda025+= quantMoeda025
                                                    moeda010+= quantMoeda010
                                                    moeda005+= quantMoeda005
                                                    cedula2+= quantCedula2
                                                    cedula5+= quantCedula5
                                                    cedula10+= quantCedula10
                                                    cedula20+= quantCedula20
                                                    print("Retire sua bebida!")
                                                    break
                                                    
                                                elif total < valor:
                                                    print("ATENÇÃO: Você inseriu R$", total,"Este valor é insuficiente para comprar o produto. Por favor recolha as moedas devolvidas e incie novamente!")
                                                    break   
                                                else:
                                                    troco = True
                                            else:
                                                troco = True
                                        else:
                                            troco = True
                                    else:
                                        troco = True
                                else:
                                    troco = True
                            else:
                                troco = True
                        else:
                            troco = True
                    else:
                        troco = True
                else:
                    troco = True
                
                if troco == True:

                    precoProduto = valor
                    troco = total - precoProduto

                    print("Você receberá de troco:")
                    moeda1+= quantMoeda1
                    moeda050+= quantMoeda050
                    moeda025+= quantMoeda025
                    moeda010+= quantMoeda010
                    moeda005+= quantMoeda005
                    cedula2+= quantCedula2
                    cedula5+= quantCedula5
                    cedula10+= quantCedula10
                    cedula20+= quantCedula20

                    contador = (total - valor) * 100
                    nota20 = 0
                    nota10 = 0
                    nota5 = 0
                    nota2 = 0
                    nota1 = 0
                    nota050 = 0
                    nota025 = 0
                    nota010 = 0
                    nota005 = 0
                    
                    if cedula20 > 0:
                        nota20 = int(troco // 20)
                        if nota20 <= cedula20: 
                            troco = troco - (nota20 * 20 )
                            cedula20 = cedula20 - nota20
                        else:     
                            troco = troco - (cedula20 * 20 )
                            cedula20 = 0

                    if cedula10 > 0:
                        nota10 = int(troco // 10)
                        if nota10 <= cedula10:
                            troco = troco - (nota10 * 10 )
                            cedula10 = cedula10 - nota10
                        else:   
                            troco = troco - (cedula10 * 10 )
                            cedula10 = 0

                    if cedula5 > 0:
                        nota5 = int(troco // 5)
                        if nota5 <= cedula5: 
                            troco = troco - (nota5 * 5 )
                            cedula5 = cedula5 - nota5
                        else:     
                            troco = troco - (cedula5 * 5 )


                    if cedula2 > 0:
                        nota2 = int(troco // 2)
                        if nota2 <= cedula2: 
                            troco = troco - (nota2 * 2 )
                            cedula2 = cedula2 - nota2
                        else:     
                            troco = troco - (cedula2 * 2 )

                    if moeda1 > 0:
                        
                        nota1 = int(troco // 1)
                        print(nota1)
                        if nota1 <= moeda1: 
                            troco = troco - (nota1 * 1 )
                            moeda1 = moeda1 - nota1
                        else:     
                            troco = troco - (moeda1 * 1 )
                
                    if moeda050 > 0:
                        
                        nota050 = int(troco // 0.50)
                        if nota050 <= moeda050: 
                            troco = troco - (nota050 * 0.50 )
                            moeda050 = moeda050 - nota050
                        else:     
                            troco = troco - (moeda050 * 0.50 )
                    
                    if moeda025 > 0:
                        
                        nota025 = int(troco // 0.25)
                        if nota025 <= moeda025: 
                            troco = troco - (nota025 * 0.25 )
                            moeda025 = moeda025 - nota025
                        else:     
                            troco = troco - (moeda025 * 0.25 )
                        
                    if moeda010 > 0:
                        
                        nota010 = int(troco // 0.10)
                        if nota010 <= moeda010: 
                            troco = troco - (nota010 * 0.10 )
                            moeda010 = moeda010 - nota010
                        else:     
                            troco = troco - (moeda010 * 0.10 )
                    if moeda005 > 0:
                        
                        nota005 = int(troco // 0.05)
                        if nota005 <= moeda005: 
                            troco = troco - (nota005 * 0.05 )
                            moeda005 = moeda005 - nota005
                        else:     
                            troco = troco - (moeda005 * 0.05 )

                    print (nota20, "notas de R$", 20)
                    print (nota10, "notas de R$", 10)
                    print (nota5, "notas de R$", 5)
                    print (nota2, "notas de R$", 2)
                    print (nota1, "moedas de R$", 1)
                    print (nota050, "moedas de R$", 0.50)
                    print (nota025, "moedas de R$", 0.25)
                    print (nota010, "moedas de R$", 0.10)
                    print (nota005, "moedas de R$", 0.05)
                    
                    break
                else:
                    
                    print("Sem troco disponível!")
                    break
    
    
            
    else:
        break
