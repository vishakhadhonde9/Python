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

