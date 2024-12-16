# Flow Control-
-  Flow control statements are used to control the execution flow of a program based on certain conditions.
-  Python provided following flow control statements -
  -  Conditional Statement
  -  Loops
  -  Loop Control Statements

# Conditional Statement -
## if Statement -
- The if statement is used to test a specific condition.
- If the condition is true, a block of code (if-block) will be executed.

#### Syntax -
    if condition:
        # code to execute if condition is True

#### Example 1]:
    x = 10
    if x > 0:
        print("x is positive")

## if else Statement -
- if-else statement is used to execute a block of code when the condition in the if statement is true, and another block of code when the condition is false.
- **if statement:** Checks a condition.
  - If the condition is True, the code inside the if block is executed.
- **else statement:** Executes if the condition in the if statement is False.
  - The else block runs when the condition in the if is not met.
#### Syntax -
     if condition:
         # code to execute if the condition is True
     else:
         # code to execute if the condition is False

#### Examples-
     number = int(input("Enter a number: "))
    
     if number % 2 == 0:
         print(f"{number} is even.")
     else:
         print(f"{number} is odd.")


    age=25
    print ("age: ", age)
    if age >=18:
       print ("eligible to vote")
    else:
       print ("not eligible to vote")
  
  ## if else elif -
  - **if statement:**
      - Used to evaluate the first condition. If it evaluates to True, the code inside the if block is executed, and the rest of the conditions are not checked.
- **elif (short for "else if"):**
    - Allows you to check additional conditions if the previous if or elif conditions were not true. You can have multiple elif blocks. If one of the elif conditions is true, its corresponding code block is executed, and no further conditions are checked.
- **else statement:**
    - Executes a block of code if none of the previous conditions (if or elif) were True. The else block is optional, and it is used to define a default action when no conditions match.

#### Syntax-
    if condition1:
        # block of code if condition1 is True
    elif condition2:
        # block of code if condition2 is True
    elif condition3:
        # block of code if condition3 is True
    else:
        # block of code if no conditions are True
#### Examples -
    grade = int(input("Enter your grade: "))

    if grade >= 90:
        print("You got an A!")
    elif grade >= 80:
        print("You got a B!")
    elif grade >= 70:
        print("You got a C!")
    elif grade >= 60:
        print("You got a D!")
    else:
        print("You got an F!")



# Loop -
- Loops in Python are allow you to execute a block of code multiple times.
## 1) for loop -
- for loop in Python is used to iterate over a sequence (like a list, tuple, string, or range) and execute a block of code for each element in the sequence.
- It is one of the most commonly used loops in Python because it allows you to easily iterate over collections of data.

#### Syntax -

    for variable in sequence:
        # Code block to execute

#### Practice Examples-
     
   fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)

for i in range(5):  # Loop from 0 to 4
    print(i)


for char in "Python":
    print(char)


   numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num % 2 == 0:
        print(f"{num} is even")
    else:
        print(f"{num} is odd")


# Initialize sum variable
total_sum = 0

# Loop through the first 10 numbers (1 to 10)
for num in range(1, 11):
    total_sum += num  # Add each number to the total sum

# Print the result
print("The sum of the first 10 numbers is:", total_sum)




# Input string
text = "Python"

# Initialize an empty string to store the reversed string
reversed_text = ""

# Loop through the string in reverse order
for char in text:
    reversed_text = char + reversed_text  # Add each character at the start of reversed_text

# Print the reversed string
print("Original string:", text)
print("Reversed string:", reversed_text)
















        
  
  
  
  

