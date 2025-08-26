# Python-Calculator
This is a simple calculator application built in Python that performs basic arithmetic operations such as addition, subtraction, multiplication, and division. The project demonstrates the use of functions, conditional statements, and user input handling in Python.
# Simple Python Calculator

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    return x / y

def calculator():
    print("=== Python Calculator ===")
    print("Select an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Exit")

    while True:
        choice = input("\nEnter choice (1/2/3/4/5): ")

        if choice == "5":
            print("Exiting calculator. Goodbye!")
            break

        if choice in ["1", "2", "3", "4"]:
            try:
                num1 = float(input("Enter first number: "))
                num2 = float(input("Enter second number: "))
            except ValueError:
                print("Invalid input. Please enter numbers only.")
                continue

            if choice == "1":
                print(f"Result: {num1} + {num2} = {add(num1, num2)}")
            elif choice == "2":
                print(f"Result: {num1} - {num2} = {subtract(num1, num2)}")
            elif choice == "3":
                print(f"Result: {num1} * {num2} = {multiply(num1, num2)}")
            elif choice == "4":
                print(f"Result: {num1} / {num2} = {divide(num1, num2)}")
        else:
            print("Invalid choice. Please select a valid option (1–5).")

if __name__ == "__main__":
    calculator()
