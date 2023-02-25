# Python
Python
faturamento_mensal = {
    "SP": 67836.43,
    "RJ": 36678.66,
    "MG": 29229.88,
    "ES": 27165.48,
    "Outros": 19849.53
}

total = sum(faturamento_mensal.values())
percentuais = {estado: faturamento / total * 100 for estado, faturamento in faturamento_mensal.items()}

for estado, percentual in percentuais.items():
    print(estado, "- percentual de representação:", percentual)
