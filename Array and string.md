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
