# Sentencias-condicionales-2
Codigo en Python bmi


def calcular_BMI (peso, estatura):
    bmi = peso / estatura ** 2
    return bmi
def clasificacion (bmi):
    if bmi < 18.5:
        return "bajo peso"
    elif 18.5 <= bmi <= 24.9:
        return "peso normal"
    elif bmi > 24.5:
        return "sobrepeso"
    else:
        return "obesidad"
    
bajo_peso = 0
peso_normal = 0
sobrepeso = 0
obesidad = 0

personas = int(input("digite el número de personas: "))
for i in range(personas):
    print(f"persona {i + 1} ")
    peso = float(input("digite el peso de la persona en kg: "))
    estatura = float(input("digite la estatura en metros de la persona: "))
    bmi = calcular_BMI (peso, estatura)
    print(f" el bmi de la persona {i+1} es igual a {bmi}")



    categoria = clasificacion(bmi)

    
    if categoria == "bajo peso":
        bajo_peso += 1
    elif categoria == "peso normal":
        peso_normal += 1
    elif categoria == "sobrepeso":
        sobrepeso += 1
    elif categoria == "obesidad":
        obesidad += 1
    

if personas > 0:
    porcentaje_b = (bajo_peso / personas) * 100
    porcentaje_n = (peso_normal / personas) * 100
    porcentaje_s = (sobrepeso / personas) * 100
    porcentaje_o = (obesidad / personas) * 100

    print("el porcentaje de personas en bajo peso es: ", porcentaje_b)
    print("el porcentaje de personas en peso normal es: ", porcentaje_n)
    print("el porcentaje de personas en sobrepeso es: ", porcentaje_s)
    print("el porcentaje de personas en obesidad es: ", porcentaje_o)
