print("=== Simple Calculator ===")
print("1 - Add")
print("2 - Subtract")
print("3 - Multiply")
print("4 - Divide")

try:
    option = int(input("Choose an operation (1-4): "))
    result = 0

    if option in [1, 2, 3, 4]:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

        if option == 1:
            result = num1 + num2
            print(f"Result: {num1} + {num2} = {result}")

        elif option == 2:
            result = num1 - num2
            print(f"Result: {num1} - {num2} = {result}")

        elif option == 3:
            result = num1 * num2
            print(f"Result: {num1} * {num2} = {result}")

        elif option == 4:
            if num2 == 0:
                print("Error: Cannot divide by zero.")
            else:
                result = num1 / num2
                print(f"Result: {num1} / {num2} = {result}")
    else:
        print("Invalid option. Please choose between 1 and 4.")

except ValueError:
    print("Invalid input! Please enter numeric values only.")
