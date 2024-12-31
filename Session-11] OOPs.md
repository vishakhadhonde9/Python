# Pillers/Characteristics of OOPs-

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
