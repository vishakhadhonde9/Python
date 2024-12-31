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


class Parent:
    def greet(self):
        print("Hello from the Parent class!")

class Child(Parent):
    def display(self):
        print("This is the Child class.")

# Creating objects
child = Child()
child.greet()  # Output: Hello from the Parent class!
child.display()  # Output: This is the Child class.




## 2.Multiple Inheritance:
- A child class inherits from multiple parent classes.


 
class Father:
    def skill_father(self):
        print("Father is good at carpentry.")

class Mother:
    def skill_mother(self):
        print("Mother is good at painting.")

class Child(Father, Mother):
    def skill_child(self):
        print("Child is good at programming.")

# Creating object
child = Child()
child.skill_father()  # Output: Father is good at carpentry.
child.skill_mother()  # Output: Mother is good at painting.
child.skill_child()   # Output: Child is good at programming.





## 3.Multilevel Inheritance: 
- A child class inherits from another child class.


class Grandparent:
    def family_name(self):
        print("Family name is Smith.")

class Parent(Grandparent):
    def greet(self):
        print("Hello from the Parent class!")

class Child(Parent):
    def display(self):
        print("This is the Child class.")

# Creating object
child = Child()
child.family_name()  # Output: Family name is Smith.
child.greet()        # Output: Hello from the Parent class!
child.display()      # Output: This is the Child class.




## 4.Hierarchical Inheritance: 
- Multiple child classes inherit from one parent class.


class Parent:
    def greet(self):
        print("Hello from the Parent class!")

class Child1(Parent):
    def display_child1(self):
        print("This is Child1.")

class Child2(Parent):
    def display_child2(self):
        print("This is Child2.")

# Creating objects
child1 = Child1()
child1.greet()         # Output: Hello from the Parent class!
child1.display_child1()  # Output: This is Child1.

child2 = Child2()
child2.greet()         # Output: Hello from the Parent class!
child2.display_child2()  # Output: This is Child2.





## 5.Hybrid Inheritance: 
- A combination of different types of inheritance.


### Overriding in Inheritance -
- Child classes can override methods from the parent class.


class Parent:
    def greet(self):
        print("Hello from the Parent class!")

class Child(Parent):
    def greet(self):
        print("Hello from the Child class!")  # Overriding greet method

# Creating object
child = Child()
child.greet()  # Output: Hello from the Child class!



### Using super() to Access Parent Methods -
- The super() function is used to call a method from the parent class.


class Parent:
    def greet(self):
        print("Hello from the Parent class!")

class Child(Parent):
    def greet(self):
        super().greet()  # Call the parent class's greet method
        print("Hello from the Child class!")

# Creating object
child = Child()
child.greet()
# Output:
# Hello from the Parent class!
# Hello from the Child class!






# Polymorphism -
- Polymorphism means "many forms".
- It allows the same function, method, or operation to work differently based on the object or data type
- Polymorphism lets you use the same code to work with objects of different types. This makes your code more flexible and easier to manage.

# 1. Compile-Time Polymorphism (Method Overloading) -
- Python does not support traditional method overloading like some other languages.

# 2. Run-Time Polymorphism (Method Overriding) -
- Overriding means function with same name and same parameters.
- Overriding is possible only in a subclass that inherits from a parent class.


# Parent class
class Animal:
    def sound(self):
        return "Some generic sound"

# Subclass overriding the parent method
class Dog(Animal):
    def sound(self):
        return "Woof!"

class Cat(Animal):
    def sound(self):
        return "Meow!"

# Using the overridden methods
animal = Animal()
dog = Dog()
cat = Cat()

print(animal.sound())  # Output: Some generic sound
print(dog.sound())     # Output: Woof!
print(cat.sound())     # Output: Meow!



























