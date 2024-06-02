
print("Hello! We welcome you to KKbank! Please choose one of the options bellow. ")

balance = 1500.00

def display_menu():
    print("Menu:")
    print("1 - Deposit")
    print("2 - Withdraw")
    print("3 - Exit")

while True:
    display_menu()
    try:
        choice = int(input("What do you want to do? Please choose (1, 2, 3): "))

        if choice == 1:
            try:
                deposit = float(input("Please enter the amount you want to deposit: "))
                balance += deposit
                print(f"Deposit successful! Current balance: {balance:.2f} euros. If you have any questions please call us on +371 35325971 or email info@kkbank.com . What do you want to do next? ")
            except ValueError:
                print("Invalid input. Please enter a valid numeric amount.")
        elif choice == 2:
        
            try:
                withdraw = float(input("Please enter the amount you want to withdraw: "))
                if withdraw > balance:
                    print("Insufficient funds. Please enter a smaller amount.")
                else:
                    reason = input("Please enter the reason for the withdrawal: ")
                    balance -= withdraw
                    print(f"Withdrawal successful! You withdrew {withdraw:.2f} euros for {reason}.")
                    print(f"Current balance: {balance:.2f} euros. What do you want to do next?")
            except ValueError:
                print("Invalid input. Please enter a valid numeric amount.")
        elif choice == 3:
    
            print(f"Thank you for choosing our bank! Your final balance is: {balance:.2f} euros. If you have any questions please call us on +371 35325971 or email info@kkbank.com")
            break
        else:
            print("Invalid choice. Please select a valid option from the menu.")
    except ValueError:
        print("Invalid input. Please enter a valid number from menu choice.")

print("Goodbye! See you next time! If you have any questions please call us on +371 35325971 or email info@kkbank.com ")
