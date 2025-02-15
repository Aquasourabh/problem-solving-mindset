__new__ is called by reference because it returns an object reference.
__init__ modifies the same referenced object created by __new__.
<!-- Python handles objects using references, unlike languages like C/C++ that use explicit pointers. -->


How Use the Dictionary Data in class
-Ans.

```.py

class Student():
    def __init__(self,name,college_id):
        self.name = name
        self.college_id = college_id

    def id(self):
        print(f"This is teacher name {self.name} and the id is {self.college_id} ")



employess_data = {
    101 : Student("Sourabh",101),
    102 : Student("Abid",102),
    103 : Student("Gaurav",103),
    104 : Student("Raghav",104)

}

fetch_data = employess_data[102]
fetch_data.id() 

``` 
# What is Constructor.
Ans.A constructor in Python is a special method used to initialize an object when it is created.
It is automatically called when a new instance of a class is created.

# What is Overloading.
Ans: Overloading is a concept in Object-Oriented Programming (OOP) where multiple functions or methods have the same name but different implementations based on the number or type of parameters.

# What is constructor Overloading?
Ans.Constructor Overloading means defining multiple constructors with different parameters in a class  but Python does not support multpile constructor.

How Do we Achive constructor Overloading in python?
Ans . We use constructor overloading by using default arguments ans kwargs (Doubt)

# what is instance Variable.
Ans.

# what is instance Methods?
Ans: Operate on instance variables (object data).
Require self as the first parameter.

```.py
class sourabh():
    def __init__(self,name,age):
        self.name = name
        self.age = age

    def tell(self):
        print(f"{self.name} is {self.age}")   


s1 = sourabh("sourabh",23)
s2 = sourabh("Abid",24)
s1.tell()
s2.tell()

```
# what is class methods
Ans: When we need to modify class-level data (shared by all objects).
Example: Updating a common property for all instances.

- The change_company method updates the class variable for all objects.
- No need to modify individual instances manually

```.py
class Student:
    name = "sourabh"
    def __init__ (self,name):
        self.name = name

    @classmethod
    def change_name(cls,New_name):
      cls.name = New_name

    def show(self):
       print(f"This is new name {self.name}")
         
       
obj = Student("Abid")
obj.show()

```
# what is Static Method?
Ans: Static Method is like simple function Where We Can't Access the instnce and the class Attribute.

```.py

class MathOperations:
    @staticmethod
    def add(a, b):
        return a + b


result = MathOperations.add(5, 3)
print(result)  # Output: 8

```
