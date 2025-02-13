# **Class:** While reading a class i stuck a Probelm as we know __init__ constructor used to intiliazed the objetcs what happens we do not use init

```.py
class sourabh():
    def __init__(self,name,age):
        self.name = name
        self.age = age

    def tell(self):
        print(f"{self.name} is {self.age}")   


s1 = sourabh("sourabh",23)
s1.tell()


---    So here we do not need to write attributes manually


```

```.py
class sourabh():
    def tell(self):
        print(f"{self.name} is {self.age}")


s1 = sourabh()
s1.name = "sourabh"
s1.age = 23
s1.tell()

Every time you create a new object, you must manually set attributes everytime.
```

# Q2. As we know python object stores attributes and  values in dictionary format and each object has separate dictionary by memory overhead or consumption increase
to avoid this we use slots(It is a class attribute that control how python stores instance attributes and __slots__ does not replace the need of init because __init__ do different work and __slots__ do different work) and it coverted dictionary into tuples to store the data

without use __slots__
```.py
class Car:
    def __init__(self, brand, model):
        self.brand = brand  # attributes Initializes 
        self.model = model  

car1 = Car("Toyota", "Camry")
print(car1.brand)  #  Toyota
print(car1.model)  #  Camry

it increases the Memory consumption

```

with __slots__ It stores the attribute value in the tuple format by which memory consumtion decreases
```.py
class Car:
    __slots__ = ('brand', 'model')  # Restrict attributes to these only
    def __init__(self, brand, model):
        self.brand = brand  # attributes Initializes 
        self.model = model  

car1 = Car("Toyota", "Camry")
print(car1.brand)  #  Toyota
print(car1.model)  #  Camry
print()  
```



