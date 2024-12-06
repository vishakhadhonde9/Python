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

# Mapping Type: dict -


# c) Boolean Type -
- Data type with one of the two built-in values, True or False.
- 






