### **`for` Loop:**
The `for` loop in Python is used to iterate over a sequence (like a list, tuple, dictionary, string, or range) and execute a block of code for each item in the sequence.

---

## **1. Basic Syntax**
```python
for variable in sequence:
    # Code to execute in each iteration
```

- `variable`: A temporary variable that stores the current element of the sequence.
- `sequence`: A collection (list, tuple, string, range, etc.).
- The code inside the loop runs once for each element in the sequence.

---

## **2. Iterating Over Different Data Types**
### **(a) Looping Through a List**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

### **(b) Looping Through a String (Character by Character)**
```python
for char in "Sourabh":
    print(char)
```

### **(c) Looping Using `range()`**
```python
for num in range(5):  # Loops from 0 to 4
    print(num)
```

---

## **3. Using `break` and `continue` in a `for` Loop**
### **(a) `break` - Stop the Loop**
```python
for num in range(10):
    if num == 4:
        break  # Stops at 5
    print(num)
```

### **(b) `continue` - Skip an Iteration**
```python
for num in range(10):
    if num == 3:
        continue  # Skips 2
    print(num)
```

---

## **4. Looping Through a Dictionary**
```python
student = {"name": "Sourabh", "age": 20, "grade": "A"}

for key, value in student.items():
    print(key, ":", value)
```

---

## **5. Nested `for` Loop**
A `for` loop inside another `for` loop is called a nested loop.

```python
for i in range(3):  # Outer loop
    for j in range(2):  # Inner loop
        print(f"i={i}, j={j}")
```

---

## **6. Using `else` With `for` Loop**
The `else` block executes after the `for` loop completes normally (without a `break`).
```python
for num in range(3):
    print(num)
else:
    print("Loop completed!")
```

---

## **7. Real-World Example: Sum of Numbers**
```python
numbers = [10, 20, 30, 40]
total = 0

for num in numbers:
    total += num

print("Total Sum:", total)
```

---

## **8. Common Mistakes to Avoid**
 **Modifying a List While Iterating** (Use a copy instead)
```python
numbers = [1, 2, 3, 4]
for num in numbers:
    if num % 2 == 0:
        numbers.remove(num)  # Wrong approach

print(numbers)  # Unexpected output!
```
 **Correct Approach:**
```python
numbers = [1, 2, 3, 4]
for num in numbers[:]:  # Looping over a copy
    if num % 2 == 0:
        numbers.remove(num)

print(numbers)  # Correct output!