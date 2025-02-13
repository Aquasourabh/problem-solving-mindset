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

It does not take arguments except slef Every time you create a new object, you must manually set attributes everytime.
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

# Q1.Can we define a class without using class keyword in python ?

- Answer: Yes We define class without usimg class keyword in python by Tyepe() keyword but when we type() it decreases the readiablity and we can't use the init constructor

# Q2.what is difference between class variable and instance variable?


```.py

class Car:
    # Class variable (shared by all instances)
    wheels = 4

    def __init__(self, brand, color):
        # Instance variables (unique to each instance)
        self.brand = brand
        self.color = color

# Creating instances
car1 = Car("Toyota", "Red")
car2 = Car("Honda", "Blue")

# Accessing instance variables
print(car1.brand, car1.color)  # Toyota Red
print(car2.brand, car2.color)  # Honda Blue

# Accessing class variable
print(car1.wheels)  # 4
print(car2.wheels)  # 4

# Modifying class variable
Car.wheels = 6  # Changes for all instances
print(car1.wheels)  # 6
print(car2.wheels)  # 6

# Modifying instance variable
car1.color = "Black"
print(car1.color)  # Black
print(car2.color)  # Blue (remains unchanged)

Class variables are shared across all instances, while instance variables are unique to each object.

```


# Q4 . What Happens If We Don't Write self in __init__?

```.py
-- If we use self we easily do the reference and if we dont use self we don't refer the object This causes a mismatch in argument

class Car:
    def __init__(self, brand, color): 
        self.brand = brand #  Storing values in instance variables
        self.color = color

# Creating an object
car1 = Car("Toyota", "Red")

print(car1.brand, car1.color)  

```


# Q5 . Does __init__ are actually constructor and what is meaning of double underscore in this?

-- Ans : Here double underscore is a special method (dunder) and it is automatically called when object is created



# Q6. why we are making methods in every class if I want to use addition so I made a addition function and why don't I use that function in the class ? it takes less memory space and also fasten the program.

-Ans: Yes We can use outside function inside the class but we can also created the function inside the class and it is good practise to define the function if we are using it beacuse it increases readiability.

# Q7.what will happen when we assign one object to another object?

--Ans.  We can assign one object to another but they share same reference in memory if we try to modify one object value the another object value is also change 

# Q8.for calling an object we need (.) operator why we are using (.), can we call the object like variables_module(display_info())

- Ans: The dot operator allow us to Access instance attributes and call methods for objects




