# Python
Python
texto = input("Digite um texto: ")
invertido = ""
for i in range(len(texto) - 1, -1, -1):
    invertido += texto[i]
print("Texto invertido:", invertido)
