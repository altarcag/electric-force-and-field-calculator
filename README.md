# electric-force-and-field-calculator
a calculator for calculating the electric field caused by a point charge and the electric force between two point charges


import math


# to calculate the electric field

def multiply(x, y):
    return 9.0 * pow(10, 9) * x * pow(y, -2)

def gneiss(q, x, a):
    return 9.0 * pow(10, 9) * q * x * pow((pow(a, 2) + pow(x, 2)), 0.5)

# to calculate the electric force
def ihatemylife(x, y, z):
    return 9.0 * pow(10, 9) * x * y * pow(z, -2)


print("Select operation.")
print("1. Electric Field at a point")
print("2. Electric Force")

while True:
    # take input from the user
    choice = input("Enter choice(1/2): ")

    # check if choice is one of the two options
    if choice in ('1'):
        num1 = float(input("Enter the charge (q) value: "))
        num2 = float(input("Enter the distance (r) value: "))

        scientific_notation1 = "{:e}".format(multiply(num1, num2))
        # print(num1, "*", num2, "=", multiply(num1, num2), " N/C")
        print("k", " (N m^2/C^2)", " *", num1, "(C)", "/", num2, "^2", "(m^2)", "=", (scientific_notation1), "N/C")

    if choice in ('2'):
        num1 = float(input("Enter the charge (q1) value: "))
        num2 = float(input("Enter the charge (q2) value: "))
        num3 = float(input("Enter the distance (r) value: "))
        scientific_notation2 = "{:e}".format(ihatemylife(num1, num2, num3))
        print("k", " (N m^2/C^2)", "*", num1, "C", "*" , num2, "C", "/" , num3, "^2", "(m^2)" "=", (scientific_notation2), "N")

        # check if user wants another calculation
        # break the while loop if answer is no

    sentinel = 0
    while True:
        next_calculation = input("Let's do next calculation? (yes/no): ")
        if next_calculation == "no":
            sentinel = 1
            break

        if next_calculation == "yes":
            print("Let's do it again!")
            break

        else:
            print("Invalid Input. please enter again")

    if sentinel == 1:
        sentinel = 0
        break
