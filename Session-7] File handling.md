# File Handling -
- File handling is used to work with files, allowing you to create, read, write, append, and delete files.
- Python provides built-in functions and methods for handling files.

# Opening a File -
- Use the open() function to open a file.


         open(file_name/path, mode)


  
| **Mode** | **Description**                                                                                          | **File Must Exist** | **Overwrites Content** | **Creates New File** |
|----------|----------------------------------------------------------------------------------------------------------|----------------------|------------------------|----------------------|
| `'r'`    | Read mode. Opens a file for reading. File must exist.                                                    | Yes                  | No                     | No                   |
| `'w'`    | Write mode. Opens a file for writing. If the file exists, it overwrites the content.                     | No                   | Yes                    | Yes                  |
| `'a'`    | Append mode. Opens a file for appending data at the end. Creates the file if it doesn’t exist.           | No                   | No                     | Yes                  |
| `'x'`    | Exclusive creation mode. Creates a new file. Raises an error if the file already exists.                 | No                   | No                     | Yes                  |
| `'b'`    | Binary mode. Used to handle binary files like images, videos, etc. Can be combined with other modes (e.g., `'rb'`). | Depends on other mode | Depends on other mode | Depends on other mode |
| `'t'`    | Text mode (default). Used to handle text files. Can be combined with other modes (e.g., `'rt'`).         | Depends on other mode | Depends on other mode | Depends on other mode |
| `'r+'`   | Read and write mode. Opens a file for both reading and writing. File must exist.                         | Yes                  | No                     | No                   |
| `'w+'`   | Write and read mode. Opens a file for writing and reading. Overwrites the file if it exists.             | No                   | Yes                    | Yes                  |
| `'a+'`   | Append and read mode. Opens a file for appending and reading. Creates the file if it doesn’t exist.      | No                   | No                     | Yes                  |
| `'rb'`   | Binary read mode. Opens a file for reading in binary format. File must exist.                            | Yes                  | No                     | No                   |
| `'wb'`   | Binary write mode. Opens a file for writing in binary format. Overwrites the file if it exists.          | No                   | Yes                    | Yes                  |
| `'ab'`   | Binary append mode. Opens a file for appending in binary format. Creates the file if it doesn’t exist.   | No                   | No                     | Yes                  |
| `'r+b'`  | Binary read and write mode. Opens a file for reading and writing in binary format. File must exist.      | Yes                  | No                     | No                   |
| `'w+b'`  | Binary write and read mode. Opens a file for writing and reading in binary format. Overwrites content.   | No                   | Yes                    | Yes                  |
| `'a+b'`  | Binary append and read mode. Opens a file for appending and reading in binary format. Creates file if not exists. | No               | No                     | Yes                  |


  
# Create a File -
- To create a file, you can use the write ('w'), append ('a'), or exclusive creation ('x') mode.


         
         # Using 'w' mode (creates if file doesn't exist)
         with open("filename.txt", "w") as file:
             file.write("Content to write in the file.")
         
         # Using 'a' mode (creates if file doesn't exist)
         with open("filename.txt", "a") as file:
             file.write("Content to append to the file.")
         
         # Using 'x' mode (raises error if file exists)
         try:
             with open("filename.txt", "x") as file:
                 file.write("This file is created using 'x' mode.")
         except FileExistsError:
             print("File already exists.")
         


    


# Write to a File
- Writing in 'w' mode overwrites the content if the file already exists.


         # Open the file in write mode
         file = open("example.txt", "w")
         
         # Write content to the file
         file.write("Hello, World!\nThis is a file handling example.")
         
         # Close the file
         file.close()


# Using with Statement -
- Ensures the file is automatically closed after the operation.


         with open("example.txt", "r") as file:
             content = file.read()
             print(content)
             

# Appending to a File -
         file = open("example.txt", "a")
         file.write("\nAppending a new line.")
         file.close()
         
         


# Reading Specific Amount of Data-


         file = open("example.txt", "r")
         print(file.read(10))  # Reads the first 10 characters
         file.close()
         

# File Deletion
- Use the os module to delete or check for files.


         import os
         
         # Delete a file
         if os.path.exists("example.txt"):
             os.remove("example.txt")
         else:
             print("The file does not exist.")
         
         


- os module: Used to interact with the operating system for file and directory operations.
- os.path.exists("example.txt"): Checks if the file example.txt exists.
- os.remove("example.txt"): Deletes the specified file.
- else block: Handles the case when the file does not exist.


