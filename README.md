# Lista-de-tarefas-compras
Listar coisas para fazer/comprar

    import os

    lista = []
    while True:
      print('Selecione uma opção:')
      opção = input('[i]nserir, [a]pagar, [l]istar: ')
  
      if opção == 'i':
          os.system('cls')
          valor = input('Valor: ')
          lista.append(valor)
      elif opção == 'a':
          indice_str = input('Escolha um índice para apagar: ')
          try:
              indice = int(indice_str)
              del lista[indice]
          except ValueError:
              print('Por favor, digite um número inteiro!')
          except IndexError:
              print('Índice não existe na lista!')
          except Exception:
              print('Erro desconhecido!')
      elif opção == 'l':
          os.system('cls')
          
          if len(lista) == 0:
              print('Lista vazia!')
          
          for i, valor in enumerate(lista):
              print(i, valor)
      else:
          print('Por favor, escolha i, a ou l.')
