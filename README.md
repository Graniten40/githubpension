# githubpension

This code is in Python 

This code calculate how long you have left to pension

def main():
    # Fråga användaren efter deras namn
    namn = input("Vad är ditt namn? ")

    # Fråga användaren efter deras ålder och hantera olika variabeltyper
    while True:
        ålder_input = input("Hur gammal är du? ")

        try:
            ålder = int(ålder_input)
            break  # Bryt loopen om användaren anger ett giltigt heltal
        except ValueError:
            print("Felaktig inmatning! Var god ange åldern som ett heltal.")

    # Räkna ut antalet år kvar till pensionen
    pensionering_ålder = 67  # Exempel: Antagen pensionsålder på 67 år
    år_kvar_till_pension = pensionering_ålder - ålder

    # Skriv ut resultatet
    if år_kvar_till_pension > 0:
        print(f"Hej {namn}! Du har {år_kvar_till_pension} år kvar till pensionen.")
    else:
        print(f"Hej {namn}! Du har redan gått i pension eller är pensionär.")

if __name__ == "__main__":
    main()
