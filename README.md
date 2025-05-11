def display_menu():
    print("\nExpense Tracker")
    print("1. Add Expense")
    print("2. View Expenses")
    print("3. Calculate Total")
    print("4. Exit")

def add_expense(expenses):
    category = input("Enter expense category (e.g., Food, Travel,entertainment,rent,other): ")
    amount = float(input("Enter expense amount: "))
    expenses.append({"category": category, "amount": amount})
    print("Expense added successfully!")

def view_expenses(expenses):
    if not expenses:
        print("No expenses recorded yet.")
    else:
        print("\nExpenses:")
        for i, expense in enumerate(expenses, start=1):
            print(f"{i}. {expense['category']} - ₹{expense['amount']:.2f}")

def calculate_total(expenses):
    total = sum(expense['amount'] for expense in expenses)
    print(f"\nTotal Expenses: ₹{total:.2f}")

def main():
