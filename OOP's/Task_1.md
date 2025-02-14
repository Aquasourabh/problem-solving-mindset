#Q3 **Class:** While reading a class i stuck a Probelm as we know __init__ constructor used to intiliazed the objetcs what happens we do not use init

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

# Q14. As we know python object stores attributes and  values in dictionary format and each object has separate dictionary by memory overhead or consumption increase
Ans : to avoid this we use slots(It is a class attribute that control how python stores instance attributes and __slots__ does not replace the need of init because __init__ do different work and __slots__ do different work) and it coverted dictionary into tuples to store the data

without use __slots__
```.py
class Car:
    def __init__(self, brand, model):
        self.brand = brand  # attributes Initializes 
        self.model = model  

car1 = Car("Toyota", "Camry")
print(car1.brand)  #  Toyota
print(car1.model)  #  Camry

car2 = Car("Alto", "800")
print(car2.brand)  
print(car2.model)  
it increases the Memory consumption

Output:
{'brand': 'Toyota', 'model': 'Camry'}
{'brand': 'Toyota', 'model': 'Camry'}

```

with __slots__ It stores the attribute value in the tuple format by which memory consumtion decreases
```.py
class Car:
    __slots__ = ('brand', 'model')  # Restrict attributes to these only
    
    def __init__(self, brand, model):
        self.brand = brand  
        self.model = model  

car1 = Car("Toyota", "Camry")
car2 = Car("Alto", "800")

print(car1.__slots__)  Output: ('brand', 'model')
print(car2.__slots__)  Output: ('brand', 'model')
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

-- Ans : We use double Undescore to Access Private memebers or instance variable ,we can access it through methods and we cannot access it diretcly.And It Provide us Mangling to avoid name Conflitcs and  we can't use other Keywords Because of ASCII Values.

```.py

class Student:
    def __init__(self, name, roll_no):
        self.name = name  # Public member
        self.__roll_no = roll_no  # Private member

    def show_roll_no(self):
        return self.__roll_no  # Private member ko class ke andar access kar sakte hain

# Object banate hain
s1 = Student("Amit", 101)

print(s1.name)       #  Ye access ho sakta hai
print(s1.show_roll_no())  # Private member ko class ke andar se access kar sakte hain

# print(s1._roll_no)  #  Error: AttributeError: 'Student' object has no attribute '_roll_no'


```



# Q6. why we are making methods in every class if I want to use addition so I made a addition function and why don't I use that function in the class ? it takes less memory space and also fasten the program.

-Ans: If We use function outside it cannot fullfill our needs like Encapsulation which is Our requirement and if we use function inside the class we can perform encapsulation. Yes We can use outside function inside the class but we can also created the function inside the class and it is good practise to define the function if we are using it beacuse it increases readiability.

# Q7.what will happen when we assign one object to another object?

--Ans. Yes We can assign one object to another but they share same reference in memory if we try to modify one object value the another object value is also change 

```.py
class Example:
    def __init__(self, value):
        self.a = value

# Creating an object
obj1 = Example(10)

# Assigning obj1 to obj2
obj2 = obj1  

# Modifying obj2
obj2.a = 20

# Checking values in both objects
print("obj1.a:", obj1.a)  # Output: 20
print("obj2.a:", obj2.a)  # Output: 20

```

# Q8.for calling an object we need (.) operator why we are using (.), can we call the object like variables_module(display_info())

- Ans: The dot operator allow us to Access instance attributes and call methods for objects

# Q9.What happen if we don't write object in class or can we write multiple objects in one class. Does object is only using for creating instance of class or we can do more things with objects? 

Ans -- If We don't write Ojects for class the class remain unsused and no memory is allocate for attributes

```.py
class Dogs():
    def __init__(self,name,color):
        self.name = name
        self.color = color
        

    def dog_bark(self):
        print(f"This dog is {self.name} and it color is {self.color} ")
            
```

Yes We can write multiple objects for one class

```.python

class Dogs():
    def __init__(self,name,color):
        self.name = name
        self.color = color
        

    def dog_bark(self):
        print(f"This dog is {self.name} and it color is {self.color} ")
            


dog1 = Dogs("Vodaphone","red")
dog1.dog_bark()


dog2 = Dogs("tillu","black")
dog2.dog_bark()

dog3 = Dogs("sheru","brown")
dog3.dog_bark()

```
# Q10.define an object "a" inside a method of a class and then, define the same object "a" outside the class?

Ans -- Inside the method variable is a Local varaible and Outside the class variable is a global variable , if we try to Access method it prints the Local variable and if we print variable a it prints the value of global variable value.

```.py

class Test:
    def create_object(self):
        a = 10  # Local object inside method
        print("Inside method, a =", a)

# Creating a different object with the same name outside the class
a = 50  # Global object
print("Outside class, a =", a)

# Calling the method
obj = Test()
obj.create_object()

# Checking if 'a' inside the method affected 'a' outside
print("Outside class after method call, a =", a)

Output is come:
Outside class, a = 50  
Inside method, a = 10  
Outside class after method call, a = 50  
```
# Q10 B.define an object "a" inside  _init() and then, define the same object "a" outside the class using _init_()?
- Ans: We are manually calling __init__() again on the same object.
This reassigns a to 20, effectively reinitializing the object.
Is It a Good Practice?
No, calling __init__() manually is not recommended because:
```.py
  class Example:
    def __init__(self, value):
        self.a = value  # Defining 'a' inside __init__

# Creating an object and initializing 'a'
obj = Example(10)
print("Value of 'a' after first initialization:", obj.a)  # Output: 10

obj = Example(20)
print(obj.a)


obj.__init__(30)
# Calling __init__() again to redefine 'a' (Not recommended in practice)
# obj.__init__(20)
# print("Value of 'a' after reinitialization:", obj.a)  # Output: 20

   
```

# Q11.Can the class is compulsory to create object in python?
Ans No it is Not compulsory ,we can create object in python without class
```.py
a = 10  # 'a' is an instance of the int class
b = "Hello"  # 'b' is an instance of the str class
c = [1, 2, 3]  # 'c' is an instance of the list class

```

# Q12.can you create an instance of the LearningModule class without providing a module name or status?

Ans -  Yes We Create instance without providing module name but it return empty class.

```.py
class empty():
    pass

obj1 = empty()
print(obj1.__dict__)

Output : {}
```

# Q13.What is instance dictionary?
- Ans: An instance dictionary is a built-in attribute (__dict__) of Python objects that stores all instance variables (attributes) as a dictionary.
```.py
class person():
    def __init__(self,name,height):
        self.name = name
        self.height = height

    def the(self):
        print(f"This is the {self.name} and this is the {self.height} ")


p1 = person("Sourabh","23.4")
p1.the()

print(p1.__dict__)

```
# Q15.does a class get stored in memory even before we create an object.
Ans. Yes in Python , a class is Loaded into memery as soon as it is defined,even if no objects are Created.

# Q16.Kaise ensure karenge ki ek attribute ko sirf class ke andar hi access kiya ja sake?

-Ans.Python mein encapsulation ka use karke hum kisi attribute ko sirf class ke andar access karne ke liye private variables ka use kar sakte hain. Ye double underscore (__) ka prefix laga kar kiya jata hai, jo name mangling apply karta hai.

```.py
class Secure:
    def __init__(self, secret_code):
        self.__secret_code = secret_code  # Private attribute

    def show_secret(self):  
        return f"Secret Code: {self.__secret_code}"  # Access within class only

obj = Secure("XYZ123")
print(obj.show_secret())  

```
# Q17.Does a Class really Reduce Lines of Code?
Ans -We want to reduce the line of code in simple program we should use function and our Program is complex where we want reduce the line of code we should make class but class main aims to hide the Data and reduce data redudancy.

- If your code involves multiple objects and repeated logic, using classes reduces lines of code.
- For simple, one-time-use cases, a function is often better than a class.
- Classes help in better organization, readability, and scalability, even if they don’t always reduce

```.py
  def add(x, y):
    return x + y

   print(add(5, 3))  # It is good for simpler program

  class Calculator:
    def add(self, x, y):
        return x + y

  c = Calculator()
  print(c.add(5, 3))  # More code for a simple task
```
# Q18.Can you create unlimited object inside a class? If yes, how can you restrict the number of objects to be create insde a class.
Ans: - Yes, Python allows unlimited object creation for a class until memory runs out. There is no built-in limit on how many objects can be instantiated.

# Q19.Can we create a class with no attribute but only methods? If yes, then how is it useful?
Ans: Yes we can create a class with no attributes but only methods and It is Useful for simple math operation.

```.py
class op:
    
    def add(a, b):
        return a + b


    def multiply(a, b):
        return a * b


print(op.add(5, 3))       
print(op.multiply(4, 6))

```
