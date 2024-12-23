# Module -
- A module in Python is a file containing Python code, typically with a .py extension, that can include:
   - Functions
   - Classes
   - Variables
   - Executable statements
- Modules allow code to be organized into reusable components, improving maintainability and modularity.

## Import module -
- To import a module in Python, you use the import keyword.
- This allows you to use code (functions, classes, variables) defined in the module within your script.
#### Syntax -
     import module_name

# 1. Import the Whole Module - This imports the entire module. 
      import math
      print(math.sqrt(16))  # Output: 4.0

# 2. Import Specific Items -
      from math import sqrt, pi
      
      print(sqrt(16))  # Output: 4.0
      print(pi)        # Output: 3.141592653589793

# 3. Import All Items -
      from math import *
      
      print(sqrt(16))  # Output: 4.0
      print(pi)        # Output: 3.141592653589793

# 4. Using Aliases -
      import math as m
      
      print(m.sqrt(16))  # Output: 4.0
