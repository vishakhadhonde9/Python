# Object Oriented Programming (OOP)-
- OOPs stands for Object-Oriented Programming System, a programming paradigm based on the concept of "objects."
- These objects represent real-world entities with properties (attributes) and behaviors (methods).
- OOPs organizes software design by bundling data and functions together into these objects, promoting modularity, reusability, and abstraction.




# 1. What is a Class?
- A class is a blueprint for creating objects.
- It defines:
     - Attributes (data): What the object knows.
     - Methods (functions): What the object can do.



            class ClassName:
                  # Attributes and Methods



              class Car:
              def __init__(self, brand, color):  # Constructor to initialize attributes
                  self.brand = brand  # Attribute
                  self.color = color  # Attribute
          
              def drive(self):  # Method
                  print(f"The {self.color} {self.brand} is driving.")
          
              # "Car" is the class.



# 2. What is an Object? -
- An object is an instance of a class. When you create an object, you bring the class to life with specific values.
- For example: The "Car" class is the blueprint. A specific car (e.g., a red Toyota) is the object.

       object_name = ClassName(arguments)



          # Create an object of the Car class
          car1 = Car("Toyota", "Red")  # car1 is an object
          car2 = Car("Honda", "Blue")  # car2 is another object
          
          # Access attributes and call methods
          print(car1.brand)  # Output: Toyota
          print(car2.color)  # Output: Blue
          
          car1.drive()  # Output: The Red Toyota is driving.
          car2.drive()  # Output: The Blue Honda is driving.
          


# Examples - 

          class Student:
              def __init__(self, name, age, grades):
                  self.name = name  # Attribute: Name of the student
                  self.age = age  # Attribute: Age of the student
                  self.grades = grades  # Attribute: List of grades
          
              def display_info(self):
                  print(f"Student Name: {self.name}, Age: {self.age}, Grades: {self.grades}")
          
              def average_grade(self):
                  return sum(self.grades) / len(self.grades)

               # Create objects
               student1 = Student("John", 20, [85, 90, 88])
               student2 = Student("Jane", 22, [78, 82, 91])
               
               # Access methods
               student1.display_info()  # Output: Student Name: John, Age: 20, Grades: [85, 90, 88]
               print(student1.average_grade())  # Output: 87.666...
               student2.display_info()  # Output: Student Name: Jane, Age: 22, Grades: [78, 82, 91]
               print(student2.average_grade())  # Output: 83.666...
               
               



          class Animal:
              def __init__(self, name, sound):
                  self.name = name  # Attribute: Name of the animal
                  self.sound = sound  # Attribute: Sound the animal makes
          
              def make_sound(self):
                  print(f"The {self.name} says {self.sound}")
          
          # Create objects
          dog = Animal("Dog", "Woof")
          cat = Animal("Cat", "Meow")
          
          # Access methods
          dog.make_sound()  # Output: The Dog says Woof
          cat.make_sound()  # Output: The Cat says Meow



# Constructor -
- Constructor is a special method that is automatically called when an object of a class is created.
- Its primary role is to initialize the attributes (data) of the object.
- The constructor in Python is defined using the __init__() method.
- It is the initializer method that sets up the object's state when it is instantiated.


          class ClassName:
              def __init__(self, parameters):
                  self.attribute = value



- Automatically Called: When an object is created, the constructor (__init__) is called automatically.
- Initialization of Attributes: It initializes the attributes of an object when the object is created.
- Only One Constructor: A class can have only one constructor, but it can accept different numbers of arguments by using default values or variable arguments.
- The self Parameter: The self parameter refers to the instance of the class, allowing the constructor to assign values to instance variables.
 

# Types of Constructor -
## 1. Default Constructor -
- A constructor that doesn't take any arguments except self and initializes attributes with default values.



          class Car:
              def __init__(self):
                  self.brand = "Toyota"  # Default value
                  self.color = "Red"     # Default value
          
              def display_info(self):
                  print(f"Brand: {self.brand}, Color: {self.color}")
          
          # Create an object using the default constructor
          my_car = Car()
          
          # Access methods
          my_car.display_info()  # Output: Brand: Toyota, Color: Red
          
          



## 2. Parameterized Constructor -
- A constructor that takes arguments to initialize attributes with the provided values.



          class Car:
              def __init__(self, brand, color):
                  self.brand = brand  # Initialize brand with the passed argument
                  self.color = color  # Initialize color with the passed argument
          
              def display_info(self):
                  print(f"Brand: {self.brand}, Color: {self.color}")
          
          # Create objects using the parameterized constructor
          my_car1 = Car("Toyota", "Red")
          my_car2 = Car("Honda", "Blue")
          
          # Access methods
          my_car1.display_info()  # Output: Brand: Toyota, Color: Red
          my_car2.display_info()  # Output: Brand: Honda, Color: Blue












