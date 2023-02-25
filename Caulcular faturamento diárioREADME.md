# Python
Python
import json

#faturamento mensal
with open("faturamento.json") as file:
    faturamento_mensal = json.load(file)

#faturamento diário
menor = min(faturamento_mensal.values())
maior = max(faturamento_mensal.values())

#média mensal
faturamento_diario = [valor for valor in faturamento_mensal.values() if valor > 0]
media = sum(faturamento_diario) / len(faturamento_diario)

#dias faturamento diário superior à média
dias_acima_media = sum(1 for valor in faturamento_diario if valor > media)

print("Menor faturamento diário:", menor)
print("Maior faturamento diário:", maior)
print("Número de dias com faturamento acima da média:", dias_acima_media)
