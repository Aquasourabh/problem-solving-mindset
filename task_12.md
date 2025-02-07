## **Lambda Functions & Higher-Order Functions:**
### **1. Lambda Functions**
Lambda functions are single-expression functions in Python.

```python
square = lambda x: x * x
print(square(5))  # Output: 25
```

### **2. Higher-Order Functions**
Higher-order functions take other functions as arguments or return functions.

#### **(a) `map()` Function**
```python
numbers = [1, 2, 3, 4]
squared = list(map(lambda x: x * x, numbers))
print(squared)  # Output: [1, 4, 9, 16]
```

#### **(b) `filter()` Function**
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # Output: [2, 4, 6, 8]
```
#### **(c) `Sorted()` Function**
### **Example: Sorting a List**
```python
numbers = [5, 2, 9, 1, 5, 6]
print(sorted(numbers))  # Output: [1, 2, 5, 5, 6, 9]
```

### **Example: Sorting in Descending Order**
```python
print(sorted(numbers, reverse=True))  # Output: [9, 6, 5, 5, 2, 1]
```

### **Example: Sorting with a Custom Key (Sorting by String Length)**
```python
words = ["apple", "banana", "kiwi", "cherry"]
print(sorted(words, key=len))  # Output: ['kiwi', 'apple', 'cherry', 'banana']
