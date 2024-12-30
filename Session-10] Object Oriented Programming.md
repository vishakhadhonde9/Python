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
