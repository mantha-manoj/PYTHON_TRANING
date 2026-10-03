# Python Day 44 – Encapsulation

## Duration

3 Hours

## Topics

-   Encapsulation
-   Public attributes
-   Protected attributes
-   Private attributes
-   Name mangling
-   Getter and setter methods
-   Data validation
-   Bank Account practical
-   Menu-driven practice

## Encapsulation

Encapsulation means wrapping data and the methods that operate on that
data inside a class while controlling access to the data.

### Access Conventions

Public:

``` python
self.name
```

Protected:

``` python
self._salary
```

Private:

``` python
self.__balance
```

Python uses name mangling for double-underscore attributes.

## Getter and Setter

A getter retrieves a value:

``` python
def get_marks(self):
    return self.__marks
```

A setter modifies a value:

``` python
def set_marks(self, marks):
    self.__marks = marks
```

Setters are useful for validation.

## Encapsulation with Validation

``` python
class Student:

    def __init__(self, name, marks):
        self.__name = name
        self.__marks = marks

    def get_marks(self):
        return self.__marks

    def set_marks(self, marks):
        if 0 <= marks <= 100:
            self.__marks = marks
        else:
            print("Invalid marks")

student = Student("Pavan", 85)
print(student.get_marks())

student.set_marks(95)
print(student.get_marks())

student.set_marks(150)
```

## Main Practical – BankAccount

``` python
class BankAccount:

    def __init__(self, account_holder, balance):
        self.account_holder = account_holder
        self.__balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
            print("Amount deposited successfully")
        else:
            print("Invalid deposit amount")

    def withdraw(self, amount):
        if amount <= 0:
            print("Invalid withdrawal amount")
        elif amount > self.__balance:
            print("Insufficient balance")
        else:
            self.__balance -= amount
            print("Amount withdrawn successfully")

    def get_balance(self):
        return self.__balance

account = BankAccount("Pavan", 10000)

print("Account Holder:", account.account_holder)
print("Initial Balance:", account.get_balance())

account.deposit(5000)
print("Balance:", account.get_balance())

account.withdraw(3000)
print("Balance:", account.get_balance())

account.withdraw(20000)
print("Final Balance:", account.get_balance())
```

## Advanced Practical – Bank Management System

Create a menu-driven program:

``` text
===== BANK MENU =====
1. Deposit
2. Withdraw
3. Check Balance
4. Account Details
5. Exit
```

Use: - `account_number` - `account_holder` - private `__balance`

Methods: - `deposit()` - `withdraw()` - `get_balance()` -
`display_account()`

Validation: - Deposit must be greater than 0. - Withdrawal must be
greater than 0. - Withdrawal cannot exceed balance. - Account holder
cannot be empty.

## Practice Questions

1.  What is encapsulation?
2.  What is a public attribute?
3.  What does `_variable` indicate?
4.  What does `__variable` indicate?
5.  What is name mangling?
6.  What is a getter?
7.  What is a setter?
8.  Why should bank balance be private?
9.  How does encapsulation help with validation?
10. Create a `BankAccount` class with deposit and withdrawal operations.

## Day 44 Assignment

Build a complete Bank Management System using encapsulation. Allow the
user to deposit, withdraw, check balance, display account details, and
exit.
