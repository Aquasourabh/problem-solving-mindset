

## **ERROR HANDLING IN PYTHON**
Errors (exceptions) can crash a program. Handling them ensures smooth execution.

### **Common Types of Errors**
1. **SyntaxError** – Incorrect Python syntax.  
2. **TypeError** – Mismatched data types.  
3. **ValueError** – Invalid value given.  
4. **ZeroDivisionError** – Division by zero.  
5. **FileNotFoundError** – File does not exist.  

### **Try-Except for Error Handling**
```python
try:
    num = int(input("Enter a number: "))
    print(10 / num)
except ZeroDivisionError:
    print("Cannot divide by zero!")
except ValueError:
    print("Invalid input! Please enter a number.")
finally:
    print("Execution completed.")
```
 **`try`** – Code that may cause an error.  
 **`except`** – Handles the error.  
 **`finally`** – Runs no matter what.  



- **Practise:**

```python
class NegativeNumberError(Exception):
    pass

try:
    num = int(input("Enter positive number: "))
    if num < 0:
        raise NegativeNumberError("Negative numbers are not allowed!")
    print("You entered:", num)
except NegativeNumberError as e:
    print("Error:", e)

```


```python

try:
    num = int(input("Enter a number: "))
    print(10 / num)
except ZeroDivisionError:
    print("It Cannot divide by zero")
except ValueError:
    print("Invalid input! Please enter a number.")
finally:
    print("Execution completed")

```

```python
try:
    num1 = int(input("Enter a number: "))
    num2 = int(input("Enter another number: "))
    print("Division Result:", num1 / num2)
except ValueError:
    print("It shows Error: Invalid input Please enter numbers only.")
except ZeroDivisionError:
    print("It Shows Error: Cannot divide by zero!")

```


```python

```