# Task 7 : Conditional Statements (if, elif, else)
Conditional statements allow you to execute specific blocks of code based on whether a given condition is True or False. They help you make decisions in your code.

- Basic Syntax of Conditional Statements:

```.py

if condition:
    # Executes when the first condition is satisfied
elif another_condition:
    # Executes when the first condition fails but the second is satisfied
else:
    # Executes if none of the above conditions are met

```
- Nested if Statements : A nested if statement is an if statement inside another if or else block. It allows you to perform more complex decisions by testing conditions within conditions.

```.py
age = 20
has_id = True
name = "Sourabh"

if age >= 18:
    if has_id:
        print(f"Access granted to {name}!")
    else:
        print(f"ID required for {name}!")
else:
    print(f"Access denied to {name}!")
```

Best Practise: We have to avoid nested conditions instead we have to use **and**

- Practise:

```.py
marks = int(input("Enter the message"))

if marks > 90:
  print("Exellent")

elif marks > 80:
  print("Good")

else:
  print("Needs Improvement")

```