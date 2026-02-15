# Variable -
- A variable in Python is a name that stores a value in memory.

        Variable Name   =   Value
              x         =    10

## Rules for Variables in Python (List Only)
- Must start with a letter (a–z, A–Z) or underscore (_).
- Cannot start with a number.
- Can contain letters, numbers, and underscores only.
- Cannot contain special characters (@, #, $, %, etc.).
- Cannot use Python keywords as variable names.
- Variable names are case-sensitive.
- No spaces are allowed in variable names.

## Access the value of variable

        print(var_name)

## Built-in Functions (Related to Variables):
- type():  To check the type of the variable
- id():  	To get the address of the variable

# Data Types -
- It is defined that what type of values that variable can contains.
- In python we have 8 types of datatypes as shown below:
    -  Text Type:str
    -  Numeric Types:int, float, complex
    -  Sequence Types:list, tuple, range
    -  Mapping Type:dict
    -  Set Types:set, frozenset
    -  Boolean Type:bool
    -  Binary Types:bytes, bytearray, memoryview
    -  None Type:None Type

# a) Text Type- string
- Strings (str): A sequence of characters enclosed in quotes.

# b) Numeric Type:-
- This type is also known as python numeric it contains three classes named as:
     - 1. Int
     - 2. Float
     - 3. Complex


## 1.Int:-
- it contain non-decimal values from the range 0-9

## 2.float:-
- it contains decimal values from the range 0.0-9.9

## 3.Complex:-
- in this we create a complex values in combination of int and float object it is in the form of standard complex format.
- Example:- a + ib
- It is used to solve physics problem through maths like dot, cross product, scaler and vector product calculation
- In python the format of complex value is a+b.

# Sequence Types : list, tuple, range -

## 1.List -
- A list is collection which contains heterogenous data elements that defined by sqaure bracket [] with the properties:
    - a) Ordered
    - b) Mutable
    - c) Allow Duplicates values

#### Create list -
     my_list = [1, 2, 3, 4, 5]

#### Accessing List Elements -
     print(my_list[0])  # Output: 1
     print(my_list[2])  # Output: 3


- You can access elements in a list by using an index. The index starts at 0 for the first element.

#### Modifying List Elements -
     my_list[2] = 10
     print(my_list)  # Output: [1, 2, 10, 4, 5]

- You can modify elements by referencing their index and assigning a new value.

#### Adding Elements -
     my_list.append(6)
     print(my_list)  # Output: [1, 2, 10, 4, 5, 6]
- Append: Adds an element to the end of the list.

#### Insert: Inserts an element at a specific index.
     my_list.insert(2, 7)  # Insert 7 at index 2
     print(my_list)  # Output: [1, 2, 7, 10, 4, 5, 6]
#### Removing Elements- Removes the first occurrence of the specified value.
     my_list.remove(10)
     print(my_list)  # Output: [1, 2, 7, 4, 5, 6]

#### List Slicing - You can slice a list to get a sublist.
     sublist = my_list[1:4]  # Elements from index 1 to 3
     print(sublist)  # Output: [2, 7, 5]

#### Length of List -
     length = len(my_list)
     print(length)  # Output: 5
- You can use the len() function to get the number of elements in a list.

#### Checking if an Item Exists in a List
     if 7 in my_list:
         print("7 is in the list")
     else:
         print("7 is not in the list")
    
#### List with Mixed Data Types -
     mixed_list = [1, "hello", 3.14, True, [5, 6]]
     print(mixed_list)


## Tuple -
- Tuple is an ordered, immutable collection of elements.
- Tuples can contain elements of different types, including integers, strings, lists, or even other tuples.
- The key characteristic of a tuple is that once it's created, it cannot be modified you can't change, add, or remove elements after the tuple is defined.

#### Accessing Elements-
     # Accessing the first element
     print(my_tuple[0])  # Output: 1
        
     # Accessing the last element
     print(my_tuple[-1])  # Output: 4.5

#### Creating a Tuple:
     my_tuple = (1, 2, 3)
     single_element_tuple = (5,)

#### Concatenation -
    tuple1 = (1, 2)
    tuple2 = (3, 4)
    combined = tuple1 + tuple2
    print(combined)  # Output: (1, 2, 3, 4)

#### Repetition -
    repeated = (1, 2) * 3
    print(repeated)  # Output: (1, 2, 1, 2, 1, 2)

### Tuple Methods:
Although tuples are immutable, they have some built-in methods:

#### count(): Returns the number of occurrences of an element.
    my_tuple = (1, 2, 2, 3, 2)
    print(my_tuple.count(2))  # Output: 3

#### index(): Returns the index of the first occurrence of an element.
    print(my_tuple.index(3))  # Output: 3

### Nested Tuples -
    nested_tuple = (1, (2, 3), (4, 5))
    print(nested_tuple[1])  # Output: (2, 3)

## Range -
- Range is a function that returns a sequence of numbers.
- By default, range returns a sequence that begins at 0 and increments in steps of 1.
- The range function only works with integers. Other data types like float numbers cannot be used.
- There are three range parameters: start, stop, and step. Only stop is required.
#### Syntax -
     range(start, stop, step)

- start : The number where the range starts (inclusive). The default is 0 if not provided.
- stop (required): The number where the range ends (exclusive).
- step : The increment between each number in the sequence. The default is 1 if not provided.

#### Examples -
     for i in range(5):
         print(i)

     for i in range(2, 6):
         print(i)

     for i in range(1, 10, 2):
         print(i)

# Mapping Type: dictionary -
- Dictionary is a collection of unordered, changeable, and indexed data.
- It is composed of key-value pairs, where each key is unique, and the value can be of any data type.

#### Creating a Dictionary -
     person = {
         "name": "John",
         "age": 30,
         "city": "New York"
     }
     
                            OR
                            
     person = dict(name="Alice", age=25, city="Los Angeles")

#### Accessing Values in a Dictionary -
     print(person["name"])  # Output: John
     print(person["age"])   # Output: 30
    
#### Adding or Modifying Key-Value Pairs -
     person["job"] = "Engineer"
     person["age"] = 31

#### Removing Key-Value Pairs -
    # Using del
    del person["city"]
    
    # Using pop()
    age = person.pop("age")
    print(age)  # Output: 31

#### Checking if a Key Exists -
     if "name" in person:
        print("Name exists in the dictionary.")

## Methods in Dictionary -
- keys(): Returns a list of all the keys.
- values(): Returns a list of all the values.
- items(): Returns a list of tuples, where each tuple is a key-value pair.

#### Example -
    print(person.keys())   # Output: dict_keys(['name', 'job'])
    print(person.values()) # Output: dict_values(['John', 'Engineer'])
    print(person.items())  # Output: dict_items([('name', 'John'), ('job', 'Engineer')])

## Example of Dictionary:
    person = {
        "name": "John",
        "age": 30,
        "city": "New York"
    }
    
    # Accessing values
    print(person["name"])  # Output: John
    
    # Adding a new key-value pair
    person["job"] = "Engineer"
    
    # Modifying an existing value
    person["age"] = 31
    
    # Checking if a key exists
    if "city" in person:
        print("City is present.")
    
    # Removing a key-value pair
    del person["city"]
    
    # Looping through the dictionary
    for key, value in person.items():
        print(key, value)

    # Output:
    # name John
    # age 31
    # job Engineer
    
# Set Types-
## Set -
- Set is the collection of the unordered items.
- Each element in the set must be unique and mutable.

#### Creating a Set -
    # Creating a set using curly braces
    fruits = {"apple", "banana", "cherry"}
                       
                         OR
                         
    # Creating a set using the set() constructor
    numbers = set([1, 2, 3, 4, 5])
    
#### Accessing Elements in a Set -
    # Looping through a set
    for fruit in fruits:
        print(fruit)
    
    # Checking if an item exists
    if "banana" in fruits:
        print("Banana is in the set.")

#### Methods in Set -
- add(): Adds a single element to the set.
- update(): Adds multiple elements to the set (can be a list, tuple, or another set).
- remove(): Removes a specific element (raises an error if the element does not exist).
- discard(): Removes an element if it exists, but does not raise an error if it does not.
- pop(): Removes and returns a random element from the set.
- clear(): Removes all elements from the set.

#### Example -
    # Adding an element
    fruits.add("orange")
    
    # Adding multiple elements
    fruits.update(["mango", "pear"])
    
    # Removing an element (raises KeyError if element is not found)
    fruits.remove("banana")
    
    # Discarding an element (does not raise error if element is not found)
    fruits.discard("cherry")
    
    # Popping a random element
    removed_fruit = fruits.pop()
    print(f"Removed: {removed_fruit}")
    
    # Clearing all elements
    fruits.clear()



## Frozenset -
- Frozenset is an immutable version of a set.
- Like sets, frozensets are unordered collections of unique elements, but unlike regular sets, once a frozenset is created, its elements cannot be modified.

#### Creating a frozenset -
    # Creating a frozenset from a list
    fruits = frozenset(["apple", "banana", "cherry"])
    
    # Creating a frozenset from a set
    numbers = frozenset({1, 2, 3, 4, 5})
    
    # Creating an empty frozenset
    empty_frozenset = frozenset()

#### Accessing Elements in a frozenset -
    for fruit in fruits:
        print(fruit)
        
#### Modifying a frozenset -
    # This will raise an error
    fruits.add("orange")  # AttributeError: 'frozenset' object has no attribute 'add'
    
    # This will also raise an error
    fruits.remove("banana")  # AttributeError: 'frozenset' object has no attribute 'remove'


# Boolean Type -
- Data type with one of the two built-in values, True or False.
- They are the result of logical operations and comparisons and are a fundamental part of control flow in programs (such as if statements, loops, etc.).


          # Boolean values
          a = True
          b = False

        # Checking the type of a boolean
        print(type(True))  # Output: <class 'bool'>
        print(type(False)) # Output: <class 'bool'>
        
## Method in boolean type -
- bool(): This function is used to convert a value into a Boolean.
- All values in Python are considered "truthy" or "falsy".
- 0, None = False
- 1 = True

        # Converting values to boolean
        print(bool(0))      # Output: False (0 is falsy)
        print(bool(1))      # Output: True (non-zero is truthy)
        print(bool(""))     # Output: False (empty string is falsy)
        print(bool("Hello"))# Output: True (non-empty string is truthy)
        print(bool([]))     # Output: False (empty list is falsy)
        print(bool([1, 2])) # Output: True (non-empty list is truthy)

#  Binary Types: bytes, bytearray, memoryview
## Bytes -
- The bytes type represents an immutable sequence of bytes (8-bit values).
- A bytes object is typically used to handle binary data that should not be modified.
- Bytes can be store number in between 0 to 255.

#### Creating a bytes object -
You can create a bytes object using a literal with a b prefix or by converting a string or other iterable into bytes.

    # Creating bytes using a literal
    b = b"Hello"
    print(b)  # Output: b'Hello'
    
    # Creating bytes using the bytes() constructor
    b2 = bytes([65, 66, 67])  # List of integers (ASCII values of 'A', 'B', 'C')
    print(b2)  # Output: b'ABC'

#### Accessing elements:
Each element in a bytes object is an integer between 0 and 255.

    print(b[0])  # Output: 72 (ASCII value of 'H')

#### Slicing:
    
     print(b[1:4])  # Output: b'ell'

### Method in bytes -


## Bytearray -
- bytearray is a mutable sequence of bytes. You can modify its content after creation.
- This is useful when you need to work with binary data and modify it in place.

#### Creating a bytearray object:

    # Creating a bytearray using a literal
    ba = bytearray([65, 66, 67])  # List of integers (ASCII values of 'A', 'B', 'C')
    print(ba)  # Output: bytearray(b'ABC')
    
    # Creating a bytearray from a string
    ba2 = bytearray("hello", "utf-8")
    print(ba2)  # Output: bytearray(b'hello')

#### Modifying a bytearray: 
        ba[0] = 90  # Change 'A' to 'Z'
        print(ba)  # Output: bytearray(b'ZBC')

#### Slicing:
        print(ba[1:3])  # Output: bytearray(b'BC')

#### Appending to a bytearray: 
You can append elements to a bytearray using the append() method or extend() method.

        ba.append(68)  # Add the ASCII value for 'D'
        print(ba)  # Output: bytearray(b'ZBCD')
        
        ba.extend([69, 70])  # Add 'E' and 'F'
        print(ba)  # Output: bytearray(b'ZBCDEF')

## Memoryview -
- memoryview is a built-in type that allows you to access the internal memory of an object that supports the buffer protocol (e.g., bytes, bytearray, array), without copying the data.
  
#### Creating a memoryview -
    
    mv = memoryview(bytearray(b"hello world"))
    print(mv)  # Output: <memory at 0x7f9f7a0e59c0>

#### Accessing data via memoryview -
A memoryview allows access to the underlying data of the bytearray or bytes object without creating a copy.

    # Accessing data in the memoryview
    print(mv[0])  # Output: 104 (ASCII value of 'h')
    

#### Slicing a memoryview:
    print(mv[1:5])  # Output: <memory at 0x7f9f7a0e5c00>


# None Type -
-  None data type represents the absence of a value or a null value.
- It is a special constant in Python that is often used to signify "nothing" or "no value here".

        x = None
        print(x)  # Output: None










