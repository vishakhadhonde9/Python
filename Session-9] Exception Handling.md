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


# Try Block -
- Code that may raise an exception is placed in the try block.
- Control Flow: If an error occurs in the try block, control immediately passes to the corresponding except block.
- No Exception: If no error occurs, the except block is skipped.


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
    


 
