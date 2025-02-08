
## ** FILE INPUT & OUTPUT (I/O)**
Files store data permanently.
File handling functions are creating a file, writing into the file, reading the file, and updating the file.
### **Opening a File**
```python
file = open("data.txt", "r")  
content = file.read()
print(content)
file.close()
```

### **Writing to a File**
```python
with open("data.txt", "w") as file:
    file.write("Hello, Sourabh!")
```
 **`with open()`** automatically closes the file.

### **Appending Data**
```python
with open("data.txt", "a") as file:
    file.write("\nNew entry added!")
```

### **Reading a File Line-by-Line**
```python
with open("data.txt", "r") as file:
    for line in file:
        print(line.strip())
```



