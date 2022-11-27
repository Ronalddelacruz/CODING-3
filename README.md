# CODING-3
RECEIPT SYSTEM

username = "Ronald"
password = "delacruz"

attempt = 0

while attempt == 0:
    try:
        user = input("Enter username: ")
        passw = input("Enter password: ")
        if username == user and password == passw:
            print("Welcome Cashier Ronald DelaCruz")
            break
        elif username != user and password == passw:
            print("Username Password incorrect")
            attempt = attempt + 0
        elif username != user and password == passw:
            print("Passwword Incorrect")
            attempt = attempt + 0
        else:
            print("Username And Password incorrect")
    except ValueError:
        print("INVALID")
# Import Library
import datetime
now = datetime.datetime.now()
date_time = now.strftime("%Y-%m-%d %H:%M:%S")


print("Welcome to NUMERO!")
print(" ")

coffee_menu = (
    "Double Berry Tea - Regular ", "Passion Fruit Tea - Regular ", "Strawberry Iced - Regular ",
    "Matcha Iced - Regular",
    "Triple Suinchine Soda - Regular")
price_list = [149, 149, 149, 169, 149]
order = []
price = []

print("NUMERO HANDCRAFT COFFEE")
print(" ")
print("Owned and Operated By Numero handcraft coffee")
print(" ")
print("Coffee available: ")
print(" ")

for i in range(len(coffee_menu)):
    print(str(i + 1) + "." + coffee_menu[i] + " - " + str(price_list[i]))

while True:
    try:
        place_order = int(input("Please place your order: "))

        if 0 < place_order <= len(coffee_menu):
            order.append(coffee_menu[place_order - 1])
            price.append(price_list[place_order - 1])

            print(" ")
            print(date_time)
            print(" ")
            print("Cashier: ", username)
            print(" ")
            print("Placed order " + coffee_menu[place_order])
            print("Coffee " + str(order))
            print("Cost " + str(price))
            if input("Would you like to order more? (y/n): ") == "n":
                break

        else:
            print("Your order is invalid. Please Try Again!")

    except ValueError:
        print("Invalid selection, please try again")


print(date_time)
cash = int(input("Enter cash amount: "))
payments = input("How would you like to pay? card/cash : ")
print("  ------------  ")
print("Subtotal:      ", price)
print(" ")
print("  ------------  ")
print("CASH: ", cash)
print(" ")
print("Payment Type: ", payments)
print(" ")
print("This is not an official receipt and no claiming input Vat. ")
print("Please request invoice.")
print(" ")
print("This Document is not valid for claim of input tax")
