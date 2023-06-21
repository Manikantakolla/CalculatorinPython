import math

def arithmetic_operation():
    print("Arithmetic Operations:")
    number1 = float(input("Enter the first number: "))
    number2 = float(input("Enter the second number: "))

    print("Select operation:")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")
    operation_choice = int(input("Enter your choice (1-4): "))

    if operation_choice == 1:
        result = number1 + number2
    elif operation_choice == 2:
        result = number1 - number2
    elif operation_choice == 3:
        result = number1 * number2
    elif operation_choice == 4:
        if number2 != 0:
            result = number1 / number2
        else:
            print("Error: Cannot divide by zero!")
            return

    print("Result: ", result)

def trigonometric_operation():
    print("Trigonometric Operations:")
    angle = float(input("Enter the angle in degrees: "))

    print("Select operation:")
    print("1. Sin")
    print("2. Cos")
    print("3. Tangent")
    operation_choice = int(input("Enter your choice (1-3): "))

    if operation_choice == 1:
        result = math.sin(math.radians(angle))
    elif operation_choice == 2:
        result = math.cos(math.radians(angle))
    elif operation_choice == 3:
        result = math.tan(math.radians(angle))
    else:
        print("Invalid choice!")
        return

    print("Result: ", result)

# Main program loop
while True:
    print("Calculator Menu:")
    print("1. Arithmetic Operations")
    print("2. Trigonometric Operations")
    print("3. Exit")
    menu_choice = int(input("Enter your choice (1-3): "))

    if menu_choice == 1:
        arithmetic_operation()
    elif menu_choice == 2:
        trigonometric_operation()
    elif menu_choice == 3:
        print("Exiting the calculator...")
        break
    else:
        print("Invalid choice Please Check Again...")