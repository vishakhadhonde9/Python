ki# Pillers/Characteristics of OOPs-

# Encapsulation -
- Encapsulation in Python is one of the fundamental concepts of object-oriented programming (OOP).
- It refers to the practice of restricting access to certain details of an object and exposing only necessary information.
- This is typically done by hiding the internal state of an object and requiring all interaction to be performed through public methods.
- Encapsulation is achieved through the use of public and private attributes and methods:

## 1.Public Attributes/Methods:
- These are accessible from outside the class.
- No special prefix is used.
- Example: self.attribute or self.method()

## 2.Private Attributes/Methods:
- These are intended to be hidden from outside the class.
- They are indicated by a double underscore (__) prefix, which triggers name mangling.
- This makes it harder (but not impossible) to access them from outside the class.
- Example: self.__attribute or self.__method()




class Car:
    def __init__(self, brand, colour):
        self.brand = brand  # public attribute
        self.__colour = colour  # private attribute

    # Public method to access private attribute
    def get_colour(self):
        return self.__colour

    # Private method
    def __start_engine(self):
        print("Engine started")

    # Public method calling a private method
    def start(self):
        self.__start_engine()

# Create an object of Car
car = Car("Toyota", "Red")

# Access public attribute
print(car.brand)  # Output: Toyota

# Access private attribute through a public method
print(car.get_colour())  # Output: Red

# Call public method which internally uses private method
car.start()  # Output: Engine started

# Trying to access private attribute or method directly will cause an error
# print(car.__colour)  # AttributeError: 'Car' object has no attribute '__colour'
# car.__start_engine()  # AttributeError: 'Car' object has no attribute '__start_engine'





class Student:
    def __init__(self, name, age, grade):
        self.name = name         # Public attribute
        self._age = age          # Protected attribute
        self.__grade = grade     # Private attribute

    # Getter for private attribute
    def get_grade(self):
        return self.__grade

    # Setter for private attribute
    def set_grade(self, new_grade):
        if new_grade >= 0 and new_grade <= 100:
            self.__grade = new_grade
        else:
            print("Invalid grade.")

# Creating a Student object
student = Student("John", 16, 85)

# Accessing public attribute
print(student.name)  # Output: John

# Accessing protected attribute (not recommended)
print(student._age)  # Output: 16

# Accessing private attribute directly (will cause an error)
# print(student.__grade)  # Uncommenting this will raise an AttributeError

# Using the getter method to access private attribute
print(student.get_grade())  # Output: 85

# Using the setter method to modify the private attribute
student.set_grade(95)
print(student.get_grade())  # Output: 95




# Abstraction -
- Abstraction in Python is a concept that involves hiding the complex implementation details of a system and showing only the essential features.
- The main goal of abstraction is to simplify the interface for users and prevent them from needing to understand the internal workings.
- Abstraction in Python is typically achieved using abstract classes and abstract methods.

## 1. Abstract Classes:
- An abstract class is a class that cannot be instantiated directly.
- It serves as a blueprint for other classes. You define it using the ABC (Abstract Base Class) module in Python, which is part of the abc module.
- Abstract classes can have both abstract methods (methods without implementation) and concrete methods (methods with implementation).

## 2. Abstract Methods:
- An abstract method is a method that is declared in an abstract class but does not have any implementation.
- It only has the method signature.
- Subclasses of the abstract class must implement this method, or else they will also be considered abstract.




from abc import ABC, abstractmethod

# Abstract class
class Animal(ABC):
    @abstractmethod  # Abstract method
    def sound(self):
        pass  # No implementation here

# Concrete class inheriting from Animal
class Dog(Animal):
    def sound(self):  # Implementation of abstract method
        print("Bark")

class Cat(Animal):
    def sound(self):  # Implementation of abstract method
        print("Meow")

# Creating objects of the concrete classes
dog = Dog()
dog.sound()  # Output: Bark

cat = Cat()
cat.sound()  # Output: Meow

- pass is a placeholder that allows the code to run without errors when there is no implementation for a method, class, or block of code.





from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start_engine(self):
        pass  # Abstract method

class Car(Vehicle):
    def start_engine(self):
        return "Car engine started!"

class Bike(Vehicle):
    def start_engine(self):
        return "Bike engine started!"

# Creating objects
car = Car()
bike = Bike()

print(car.start_engine())  # Output: Car engine started!
print(bike.start_engine())  # Output: Bike engine started!









# Inheritance -
- It allows a class (called the child class or subclass) to inherit the properties and methods of another class (called the parent class or base class).
- This promotes code reuse and creates a relationship between classes.
- Parent Class: The class being inherited from.
- Child Class: The class that inherits from the parent class


# Types of Inheritance in Python:
## 1.Single Inheritance:
- One child class inherits from one parent class.





## 2.Multiple Inheritance:
- A child class inherits from multiple parent classes.





## 3.Multilevel Inheritance: 
- A child class inherits from another child class.



## 4.Hierarchical Inheritance: 
- Multiple child classes inherit from one parent class.


## 5.Hybrid Inheritance: 
- A combination of different types of inheritance.







