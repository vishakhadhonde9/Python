# Function -
- Function is a block of reusable code that performs a specific task.
- It allows you to write code once and use it multiple times, making programs more organized and efficient.

## Define Function -
def function_name(parameters):
    """Optional docstring to describe the function."""
    # Function body (code to execute)
    return result  # Optional return statement

- def: keyword in Python is used to define a function.
- parameters or arguments: Parameters are variables that you define in a function to accept input values when the function is called.
- return: It ends the function execution and specifies what value the function should give back.

## function calling -
    function_name(arguments)


### Examples - 
def greet():
    print("Hello!")

# Calling the function
greet()  # Output: Hello!


def greet(name):
    print(f"Hello, {name}!")

# Calling the function with an argument
greet("Alice")  # Output: Hello, Alice!


def add(a, b):
    return a + b

# Calling the function and storing the result
result = add(5, 3)
print(result)  # Output: 8


def calculate_area(length, width):
    return length * width

# Call the function with arguments
area = calculate_area(5, 10)
print("Area of rectangle:", area)


def sum_numbers(*numbers):
    return sum(numbers)

# Call the function with different numbers of arguments
print(sum_numbers(1, 2, 3))       # Output: 6
print(sum_numbers(5, 10, 15, 20)) # Output: 50
