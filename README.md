def acougue():
    qtd_acougue = int(input("Qual a quantidade de produto deseja comprar?: "))
    if qtd_acougue > 5:
        preco_acougue = (qtd_acougue * 25) * 0.95
    else:
        preco_acougue = qtd_acougue * 25

    return "Açougue", qtd_acougue, preco_acougue


def limpeza():
    qtd_limpeza = int(input("Qual a quantidade de produto deseja comprar?: "))
    if qtd_limpeza > 5:
        preco_limpeza = (qtd_limpeza * 18) * 0.95
    else:
        preco_limpeza = qtd_limpeza * 18

    return "Produto de Limpeza", qtd_limpeza, preco_limpeza


def padaria():
    qtd_padaria = int(input("Qual a quantidade de produto deseja comprar?: "))
    if qtd_padaria > 5:
        preco_padaria = (qtd_padaria * 10) * 0.95
    else:
        preco_padaria = qtd_padaria * 10

    return "Padaria", qtd_padaria, preco_padaria


def quitanda():
    qtd_quitanda = int(input("Qual a quantidade de produto deseja comprar?: "))
    if qtd_quitanda > 5:
        preco_quitanda = (qtd_quitanda * 12) * 0.95
    else:
        preco_quitanda = qtd_quitanda * 12

    return "Quitanda", qtd_quitanda, preco_quitanda


opc = -1
total = 0
compras = []

while opc != 0:
    print("Escolha a loja para comprar:")
    print("1. Açougue")
    print("2. Produto de limpeza")
    print("3. Padaria")
    print("4. Quitanda")
    print("0. Sair")
    opc = int(input("Opção: "))

    if opc == 1:
        loja, qtd, preco = acougue()
        total += preco
        compras = compras + [(loja, qtd, preco)]

    elif opc == 2:
        loja, qtd, preco = limpeza()
        total += preco
        compras = compras + [(loja, qtd, preco)]

    elif opc == 3:
        loja, qtd, preco = padaria()
        total += preco
        compras = compras + [(loja, qtd, preco)]

    elif opc == 4:
        loja, qtd, preco = quitanda()
        total += preco
        compras = compras + [(loja, qtd, preco)]
numero = 0
for i in compras:
    numero = numero + 1
    loja, qtd, preco = i
    print(f"{numero}.{loja}: {qtd} - R${preco}")

print(f"O valor total da compra foi de R${total}")
