
### **1. Function with Parameters**
```python
def greet(name):
    print(f"Hello, {name}!")

greet("Sourabh")
```

- `name` is a parameter that the function accepts as input.
- `greet("Sourabh")` passes the argument "Sourabh" to the function.

### **2. Function with Return Values**
```python
def add(a, b):
    return a + b

result = add(5, 10)
print("Sum:", result)
```

- The `return` statement sends back a result to the caller.
- `add(5, 10)` returns `15`, which is stored in `result`.

### **3. Function Scope (Local vs Global Variables)**
```python
global_var = "I am global "

def my_function():
    local_var = "I am local "
    print(local_var)  # Accessible only inside this function
    print(global_var)  # Accessible everywhere

my_function()
print(global_var)  # This works
# print(local_var)  # This will cause an error (local variable not accessible outside the function)
```

- `global_var` is accessible everywhere.
- `local_var` is only accessible inside `my_function()`.

