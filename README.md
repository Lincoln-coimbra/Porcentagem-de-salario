def calcular_aumento_salario(salario):
    if salario <= 280:
        aumento_percentual = 20
    elif salario <= 700:
        aumento_percentual = 15
    elif salario <= 1500:
        aumento_percentual = 10
    else:
        aumento_percentual = 5

    aumento = salario * (aumento_percentual / 100)
    salario_atualizado = salario + aumento

    # Calculando o aumento real descontado pela inflação
    inflacao = 3.8
    aumento_real = salario_atualizado - (salario_atualizado * (inflacao / 100))

    return aumento_percentual, aumento, aumento_real, salario_atualizado


salario = float(input("Digite o valor do salário: "))

aumento_percentual, aumento, aumento_real, salario_atualizado = calcular_aumento_salario(salario)

print("Valor antes do reajuste:", salario)
print("Percentual de aumento aplicado:", aumento_percentual, "%")
print("Valor do aumento:", aumento)
print("Salário atualizado após o reajuste:", salario_atualizado)
print("Valor do aumento real descontado a inflação:", aumento_real)
