# Object Oriented Programming (OOP)-
- OOPs stands for Object-Oriented Programming System, a programming paradigm based on the concept of "objects."
- These objects represent real-world entities with properties (attributes) and behaviors (methods).
- OOPs organizes software design by bundling data and functions together into these objects, promoting modularity, reusability, and abstraction.

# Constructor -




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



car1 = Car("Toyota", "Red")  # car1 is an object of the Car class.
car1.drive()  # Output: The Red Toyota is driving.

car2 = Car("Honda", "Blue")  # Another object of the Car class.
car2.drive()  # Output: The Blue Honda is driving.
