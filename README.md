
import random

scor_utilizator = 0
scor_calculator = 0

for i in range(10):
    alegere = input("Alegi 'par' sau 'impar'? ").lower()
    numar = int(input("Alege un număr între 0 și 10: "))
    numar_calculator = random.randint(0, 10)
    suma = numar + numar_calculator
    

    print("Calculatorul a ales:", numar_calculator)
    print("Suma este:", suma)

    if suma % 2 == 0:
        rezultat = "par"
    else:
        rezultat = "impar"

    if alegere == rezultat:
        print("Ai câștigat runda!")
        scor_utilizator += 1
    else:
        print("Calculatorul a câștigat runda.")
        scor_calculator += 1


    din_nou = input("Mai joci? (da/nu): ").lower()
    if din_nou != "da":
        break

print("Scor final:")
print("Tu:", scor_utilizator)
print("Calculatorul:", scor_calculator)
