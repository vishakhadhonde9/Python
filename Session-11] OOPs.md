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

## 









