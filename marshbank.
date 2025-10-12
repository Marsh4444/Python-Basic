mport random
import sys

class MarshBank:
    """Bank mangement system"""

    accounts = {}

    def __init__(self, name, balance):
        """Constructor for MarshBank"""
        self.name = name
        self.balance = balance
        self.account_number = self.get_account_number()

        #register both account in a dictionary using both keys
        MarshBank.accounts[self.name] = self
        MarshBank.accounts[self.account_number] = self

        print(f"✅ Account created for {self.name}")
        print(f"Account Number: {self.account_number}")
        print(f"Balance: ${self.balance}\n")

    def get_account_number(self):
        """GEnerates unigue number for each users"""
        return ''.join(str(random.randint(0,9)) for _ in range(10)) #mixed this but finnaly got this

    def deposit(self, money):
        """Deposit money to users account"""
        if money < 0:
            print("❌ invalid deposit amount")
        else:
            print("Deposit in progress")
            self.balance += money
            print(f"Deposit Completed for {self.name}\n{self.account_number} as a total balance of {self.balance} ")


    def withdraw(self, money):
        """Withdraw money from account"""
        access = input('\nwhich account do you want to access? ')
        if access != self.name:
            print("❌ SCAM ALERT")
            sys.exit() #learnt this new
        else:
            print("your withdrawal is on the way")
            if money < 0:
                print("❌ invalid withdrawal amount")
            else:
                print("withdrawal in progress")
                self.balance -= money
                print(f"withdrawal Completed for {self.name}\n{self.account_number} as a total balance of {self.balance} ")

    def transfer(self, account, funds):
        """Transfer money from one account"""
        pass

    def get_balance(self):
        """GEt the balance of an account"""
        return self.balance

account_1 = MarshBank('chris', 1000)
account_1.deposit(200)
account_1.withdraw(100)

