
def calculator():
    print("===== КАЛКУЛАТОР =====")
    print("1. Събиране (+)")
    print("2. Изваждане (-)")
    print("3. Умножение (*)")
    print("4. Деление (/)")
    print("0. Изход")

    while True:
        choice = input("\nИзбери операция: ")

        if choice == "0":
            print("Благодаря, че използва калкулатора!")
            break

        if choice not in ["1", "2", "3", "4"]:
            print("Невалидна операция! Опитай отново.")
            continue

        try:
            a = float(input("Въведи първото число: "))
            b = float(input("Въведи второто число: "))

            if choice == "1":
                result = a + b
            elif choice == "2":
                result = a - b
            elif choice == "3":
                result = a * b
            elif choice == "4":
                if b == 0:
                    print("Грешка! Не може да се дели на нула.")
                    continue
                result = a / b

            print("Резултат:", result)

        except ValueError:
            print("Моля, въведи валидни числа!")


if __name__ == "__main__":
    calculator()
