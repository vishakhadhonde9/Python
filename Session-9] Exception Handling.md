# Exception -
- An exception is an error that occurs during the execution of a program.
- For example:
     - Dividing a number by zero (ZeroDivisionError)
     - Trying to convert a string into an integer (ValueError)
     - Accessing a file that does not exist (FileNotFoundError)
- When these errors occur, Python stops the program unless we handle the exception.

# Exception Handling -
- Exception handling in Python is a mechanism to handle runtime errors gracefully, ensuring the program does not crash abruptly.
- It uses a set of keywords to catch and manage exceptions.

# Types of Exception in Python -

## 1. Built-in Exceptions -
- These are the standard exceptions that Python raises for errors that occur during program execution.
- SyntaxError: Raised when the Python interpreter encounters incorrect syntax (e.g., a missing parenthesis or a keyword used incorrectly).
- NameError: Undefined variable or function.
- TypeError: Invalid operation for the type of object.
- ValueError: Function gets an argument of the correct type but invalid value.
- IndexError: Invalid index used in a list or sequence.
- KeyError: Accessing a non-existing key in a dictionary.
- AttributeError: Accessing an invalid attribute on an object.
- ZeroDivisionError: Division by zero.
- FileNotFoundError: File doesn't exist.
- ImportError: Problem with importing a module.
- OverflowError: Numeric operation produces an overflow.
- MemoryError: Out of memory.
- RecursionError: Too deep recursion.
- StopIteration: Iteration completed.
- IndentationError: Improper indentation.
- UnicodeDecodeError: Error decoding a file with the wrong encoding.
- ConnectionError: Network connection issue.

## 2. Special Exceptions -
- Special exceptions refer to exceptions that are either specific to particular situations or are inherited from the built-in exception hierarchy but have a more specific use case.
- These exceptions typically deal with system-related issues or specific programming scenarios where you need more specialized handling.
- ileExistsError: Raised when trying to create a file or directory that already exists.
- FileNotFoundError: Raised when a file or directory is not found.
- PermissionError: Raised when lacking permission to access a file or resource.
- IsADirectoryError: Raised when attempting to open a directory as a file.
- NotADirectoryError: Raised when attempting to perform directory operations on a file.
- BlockingIOError: Raised when a blocking I/O operation is performed in non-blocking mode.
- ChildProcessError: Raised when a child process operation fails.
- ConnectionError: Base class for network-related connection issues.
- BrokenPipeError: Raised when a pipe or socket is written to after being closed.
- TimeoutError: Raised when an operation times out.
- SystemExit: Raised by sys.exit() to terminate the program.
- KeyboardInterrupt: Raised when the user interrupts the program with Ctrl+C.
- NotImplementedError: Raised when an abstract method is not implemented in a subclass.
-


# Try and Expect Block -
- **try:** Code that may raise an exception is placed in the try block.
- **except:** Handles the exception if it occurs.
- **else:** Executes code if no exception occurs.
- **finally:** Executes code regardless of whether an exception occurred or not
- Control Flow: If an error occurs in the try block, control immediately passes to the corresponding except block.
- No Exception: If no error occurs, the except block is skipped.



          try:
              # Code that may raise an exception
              risky_operation()
          except ExceptionType1:
              # Code to handle ExceptionType1
          except ExceptionType2 as e:
              # Code to handle ExceptionType2 and capture exception details in 'e'
          else:
              # Code to execute if no exception occurs
          finally:
              # Code to execute always (cleanup actions)
              




          try:
              print("This is a safe operation.")
          except Exception:
              print("An error occurred.")
          
          
          try:
              result = 10 / 0  # Division by zero error
          except ZeroDivisionError:
              print("Error: Division by zero is not allowed.")
          
          
          try:
              num = int(input("Enter a number: "))
              result = 10 / num
              print(f"Result: {result}")
          except ValueError:
              print("Invalid input! Please enter a number.")
          except ZeroDivisionError:
              print("Cannot divide by zero!")
              
          
          
           try:
              with open("file.txt", "r") as file:
                  content = file.read()
          except FileNotFoundError:
              print("File not found.")
          else:
              print("File read successfully:", content)
          finally:
              print("Operation complete.")
          
