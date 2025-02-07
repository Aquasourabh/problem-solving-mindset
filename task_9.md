

### **`while` Loop: **
The `while` loop in Python is used to repeatedly execute a block of code as long as a given condition is `True`.

---

## **1. Basic Syntax**
```python
while condition:
    # Code to execute in each iteration
```

- `condition`: A boolean expression that is checked before each iteration.
- The loop continues to execute until the condition becomes `False`.

---

## **2. Example: Simple `while` Loop**
```python
count = 0
while count < 5:
    print("Count is:", count)
    count += 1
```

---

## **3. Using `break` and `continue` in a `while` Loop**
### **(a) `break` - Stop the Loop**
```python
num = 0
while num < 10:
    if num == 4:
        break  # It Stops at 4
    print(num)
    num += 1
```

### **(b) `continue` - Skip an Iteration**
```python
num = 0
while num < 5:
    num += 1
    if num == 2:
        continue  # It Skips 2
    print(num)
```

---

## **4. Infinite `while` Loop (Use with Caution!)**
```python
while True:
    print("This will run forever!")
```


## **5. Using `else` With `while` Loop**
The `else` block executes after the `while` loop completes normally (without a `break`).
```python
num = 0
while num < 3:
    print(num)
    num += 1
else:
    print("Loop completed!")
```

---

## **6. Real-World Example:**
```python
import getpass

password = 12345
max_pass =  0 
user_input = int(getpass.getpass("Enter the Password: "))

while password != user_input:
    user_input = int(getpass.getpass("Enter the Password: "))
    max_pass += 1
    if max_pass == 2:
        print("You have Reached the maximum limit try after 24 hours")
        break
    

else:
    print("You can Access the System")

```
