# cafetarea

#Define the menu of restaurant

menu = {
    "pizza":40,
    "pasta":50,
    "salad":70,
    "coffe":80,
    "Burger":70
}

#greet customer

print("Welcome to PYTHON RESTAURANT")
print("pizza: Rs40\npasta: Rs50\nBurger: Rs60\nSalad: Rs70\ncoffe: Rs80" )

order_total = 0   #80 + 70 = 150

item_1 = input("Enter the name of item you want to order = ")
if item_1 in menu:
    order_total += menu[item_1]   #0 + 50
    print(f"your item {item_1} has been added to your order")
else:
    print(f"sorry sir, {item_1} is not available yet! ")


another_order = input("Do you want to add another item? (yes/no) ")
if another_order == "yes":
    item_2 = input("Enter the name of second item = ")
    if item_2 in menu:
        order_total += menu[item_2]
        print(f"item {item_2} has been added to order")
    else:
        print(f"Ordered item {item_2} is not available! ")

print(f"The total amount of items to pay is = {order_total}")
