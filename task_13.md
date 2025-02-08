# **MODULES, ERROR HANDLING, AND FILE INPUT/OUTPUT (I/O) IN PYTHON**
## **MODULES IN PYTHON**
Modules help organize code by allowing you to reuse functions, classes, and variables in different files.

### **What is a Module?**
A module is a Python file that contains functions, variables, and classes.

### **Why Use Modules?**
**Code Reusability** – Write once, use multiple times.  
**Better Organization** – Keeps code manageable.  
**Encapsulation** – Hides complex logic in reusable functions.  

### **Types of Modules**
1. **Built-in Modules** – Pre-installed (e.g., `math`, `random`, `os`).  
2. **User-defined Modules** – Created by you.  
3. **Third-party Modules** – Installed via `pip` (e.g., `numpy`, `pandas`).  

### **Importing Modules**
```python
import math
print(math.sqrt(16)) 
```

#### **Importing Specific Functions**
```python
from math import sqrt
print(sqrt(25))  
```

#### **Creating a Custom Module**
Create `my_module.py`:
```python
def greet(name):
    return f"Hello, {name}!"
```
Use it in another file:
```python
import my_module
print(my_module.greet("Sourabh"))  
```
```python
import math

print(math.sqrt(49))  # Square root of 49
print(math.factorial(5))  # Factorial of 5
print(math.pi)  # Value of Pi
```