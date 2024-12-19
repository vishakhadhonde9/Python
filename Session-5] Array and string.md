# Array -
- Array is collection of similar data types or items.
- Element - Each item stored in an array is called an element.
- Index - The location of an element in an array has a numerical index, which is used to identify the element's position.
- The Array can be handled in Python by a module named Array. To use arrays in Python, you need to import the array module:
            import array
- If you need multidimensional arrays or advanced numerical operations, you can use the NumPy library:
            import numpy

# Create an array -
      array.array(typecode, [initializers])
      

| Type Code | Data Type         | Example          |
|-----------|-------------------|------------------|
| `i`       | Integer           | `10, 20, 30`    |
| `f`       | Floating-point    | `1.1, 2.2`      |
| `u`       | Unicode characters| `'a', 'b'`      |


## Function in Python -

| Function/Method          | Description                                                                 | Example                                                                                     |
|--------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| `array.append(x)`        | Adds a new element `x` to the end of the array.                            | `arr.append(4)` → `array('i', [1, 2, 3, 4])`                                               |
| `array.insert(i, x)`     | Inserts element `x` at index `i`.                                          | `arr.insert(1, 10)` → `array('i', [1, 10, 2, 3, 4])`                                       |
| `array.remove(x)`        | Removes the first occurrence of element `x`.                              | `arr.remove(10)` → `array('i', [1, 2, 3, 4])`                                              |
| `array.pop([i])`         | Removes and returns the element at index `i`. Default is the last element. | `arr.pop()` → `4`, `array('i', [1, 2, 3])`                                                 |
| `array.index(x)`         | Returns the index of the first occurrence of element `x`.                 | `arr.index(2)` → `1`                                                                       |
| `array.extend(iterable)` | Appends all elements from an iterable to the array.                       | `arr.extend([5, 6])` → `array('i', [1, 2, 3, 5, 6])`                                       |
| `array.reverse()`        | Reverses the elements of the array in place.                              | `arr.reverse()` → `array('i', [6, 5, 3, 2, 1])`                                            |
| `array.tolist()`         | Converts the array to a regular Python list.                              | `arr.tolist()` → `[6, 5, 3, 2, 1]`                                                         |
| `array.buffer_info()`    | Returns a tuple (address, length) of the array buffer.                    | `arr.buffer_info()` → `(address, length)`                                                  |
| `array.itemsize`         | Returns the size (in bytes) of each element in the array.                 | `arr.itemsize` → `4` (for an integer array)                                                |


#### Examples -

            import array
            
            # Create an array
            arr = array.array('i', [1, 2, 3])
            
            # Append a new element
            arr.append(4)
            
            # Insert an element
            arr.insert(1, 10)
            
            # Remove an element
            arr.remove(2)
            
            # Pop an element
            popped = arr.pop()
            
            # Print results
            print("Array after operations:", arr)
            print("Popped element:", popped)



# Multidimensional Array -
- In Python, you can create a multidimensional array using lists of lists.
         
## Create 2D array -
            import numpy as np
            
            # 2D array using numpy
            array_2d = np.array([
                [1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]
            ])
            print(array_2d[1][2])  # Access element at second row, third column (value: 6)


# 3D Array -
            # 3D array using numpy
            array_3d = np.array([
                [
                    [1, 2],
                    [3, 4]
                ],
                [
                    [5, 6],
                    [7, 8]
                ]
            ])
            
            print(array_3d[1][0][1]) # output : 6 

# String Function -
## 1. len()-
- Purpose: Returns the length of a string.
- Syntax: len(string)

#### Example -
         text = "Hello, world!"
         print(len(text))  # Output: 13
            
            
# 2. lower()
- Purpose: Converts all characters in the string to lowercase.
- Syntax: string.lower()
#### Example -
            text = "HELLO"
            print(text.lower())  # Output: hello
# 3. upper()
- Purpose: Converts all characters in the string to uppercase.
- Syntax: string.upper()

#### Example -
            text = "hello"
            print(text.upper())  # Output: HELLO
            
# 4. replace()
- Purpose: Replaces a specified substring with another substring.
- Syntax: string.replace(old, new, count)
            - old: The substring to be replaced.
            - new: The substring that will replace old.
            - count: (optional) The number of occurrences to replace.
#### Example -
            text = "hello world"
            print(text.replace("world", "Python"))  # Output: hello Python
            
# 5. find()
- Purpose: Searches for a substring and returns its index position (first occurrence).
- Syntax: string.find(substring)

#### Example -
            text = "hello world"
            print(text.find("world"))  # Output: 6
            
# 6. join()
- Purpose: Joins elements of an iterable (like a list) with a string as the separator.
- Syntax: separator.join(iterable)

## Example -
            words = ["Hello", "world"]
            print(" ".join(words))  # Output: Hello world

# 7. split()
- Purpose: Splits a string into a list of substrings based on a delimiter (whitespace by default).
- Syntax: string.split(separator, maxsplit)

## Example-
            text = "Hello world Python"
            print(text.split())  # Output: ['Hello', 'world', 'Python']

# 8. count()
- Purpose: Returns the number of occurrences of a substring in the string.
- Syntax: string.count(substring)

# Example -
            text = "hello hello world"
            print(text.count("hello"))  # Output: 2

# 9. format()
- Purpose: Formats a string by inserting values into placeholders.
- Syntax: string.format(value1, value2, ...)
## Example -
            name = "Alice"
            age = 30
            print("My name is {} and I am {} years old.".format(name, age))
            # Output: My name is Alice and I am 30 years old.

















