## **9. Lambda Functions & Higher-Order Functions in Python**
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

#### **(c) `reduce()` Function**
```python
from functools import reduce
numbers = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, numbers)
print(product)  # Output: 24
```

