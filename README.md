# allows-users-to-input-their-expenses-and-categorize-them
expenses = {}

def add_expense(category, amount):
    if category in expenses:
        expenses[category] += amount
    else:
        expenses[category] = amount

while True:
    print("\n1. Add Expense")
    print("2. View Expenses")
    print("3. Quit")
    choice = input("Enter your choice: ")

    if choice == '1':
        category = input("Enter expense category: ")
        amount = float(input("Enter expense amount: "))
        add_expense(category, amount)
    elif choice == '2':
        print("\nExpense Report:")
        for category, amount in expenses.items():
            print(f"{category}: ${amount}")
    elif choice == '3':
        break
    else:
        print("Invalid choice. Please try again.")
