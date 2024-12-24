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


  
