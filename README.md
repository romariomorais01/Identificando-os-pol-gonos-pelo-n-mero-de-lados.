"# Identificando-os-pol-gonos-pelo-n-mero-de-lados." 


"# Identificando-os-pol-gonos-pelo-n-mero-de-lados." 
def nome_poligono(lados):
    nomes = {
        3: "Triângulo",
        4: "Quadrado ou Quadrilátero",
        5: "Pentágono",
        6: "Hexágono",
        7: "Heptágono",
        8: "Octógono",
        9: "Eneágono (ou Nonágono)",
        10: "Decágono",
        11: "Hendecágono",
        12: "Dodecágono",
        13: "Tridecágono",
        14: "Tetradecágono",
        15: "Pentadecágono",
        16: "hexadecágono",
        17: "Heptadecágono",
        18: "Octodecágono",
        19:"Eneadecágono",
        20: "Icoságono"
    }
    if lados < 3:
        return "Não é um polígono (precisa ter pelo menos 3 lados)."
    elif lados in nomes:
        return nomes[lados]
    else:
        return f"Polígono de {lados} lados."

# Programa principal
while True:
    try:
        n = int(input("Digite o número de lados do polígono (0 para sair): "))
        if n == 0:
            print("Encerrando...")
            break
        print("→", nome_poligono(n))
    except ValueError:
        print("Por favor, digite um número válido.")
