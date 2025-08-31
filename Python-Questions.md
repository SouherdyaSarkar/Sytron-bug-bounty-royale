# Bug Bounty Royale - Final(Python)

Below are 5 codeblocks. Each contains hidden bugs.  
Your task:  
1. Identify and fix the bug(s).  
2. Run the corrected code.  
3. Submit the **final correct output**.  

## Qn 1 : Debug the code so it outputs Alice’s average and Bob’s average

```python
class Student:
    def __init__(self, name, marks=None):
        if marks is None:
            marks = []
        self.name = name
        self.marks = marks

    def add_mark(self, mark):
        self.marks.append(mark)

    def average(self):
        return sum(self.marks) / len(self.marks)

s1 = Student("Alice")
s2 = Student("Bob")

s1.add_mark(90)
s2.add_mark(80)

print(s1.name, "average:", s1.average())
print(s2.name, "average:", s2.average())

```

## Q2. Qn 2 : Print the expected balance

```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount

    def withdraw(self, amount):
        if self.balance >= amount:
            self.balance -= amount
        else:
            print("Insufficient funds")

a1 = BankAccount("Alice", 1000)
a1.deposit(500)
a1.withdraw(300)
print("Balance:", a1.balance)

```

## Q3. Qn 3 : Fix the code to print the following output


```
Line 0 : Hello World
Line 1 : Python Rocks
```

```python
def read_file(filename):
    f = open(filename, "r")
    lines = f.readlines()
    for i in range(len(lines)):
        print("Line", i, ":", lines[i].strip())
    f.close()

# sample.txt content:
# Hello World
# Python Rocks

read_file("sample.txt")

```

## Q4. Qn 4 : Fix the code to print the following output

```
Manager: Eve
Employee: Alice Salary: 50000
Employee: Bob Salary: 40000
```

```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def show(self):
        print("Employee:", self.name, "Salary:", self.salary)

class Manager(Employee):
    def __init__(self, name, salary, team=None):
        super().__init__(name, salary)
        if team is None:
            team = []
        self.team = team

    def add_member(self, emp):
        self.team.append(emp)

    def show_team(self):
        print("Manager:", self.name)
        for member in self.team:
            member.show()

e1 = Employee("Alice", 50000)
e2 = Employee("Bob", 40000)
m = Manager("Eve", 80000)

m.add_member(e1)
m.add_member(e2)
m.show_team()
```

## Q5. Fix the code to print the following output

```
Result is 5.0
Division by zero!
```

```python
def safe_divide(func):
    def wrapper(x, y):
        try:
            return func(x, y)
        except ZeroDivisionError:
            print("Division by zero!")
    return wrapper

@safe_divide
def divide(x, y, msg="Result is"):
    print(msg, x / y)

divide(10, 2)
divide(5, 0)
```
