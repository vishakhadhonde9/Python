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


## Nested for loop-
- A nested for loop is a loop inside another loop.
- The inner loop runs completely for every iteration of the outer loop.

#### Syntax -

     for outer_variable in outer_sequence:
         for inner_variable in inner_sequence:
            # Code block executed for each combination
        
#### Practice Examples -

    # Outer loop for x values
    for x in range(3):
        # Inner loop for y values
        for y in range(3):
            print(f"({x}, {y})")
    


    # Outer loop controls the number of rows
    for i in range(1, 6):
        # Inner loop prints stars in each row
        for j in range(i):
            print("*", end="")  # Print stars on the same line
        print()  # Print a new line after each row
        

# while loop-
- while loop is used to repeatedly execute a block of code as long as a specified condition evaluates to True.
- The condition is checked before each iteration.

#### Syntax -

     while condition:
         # Code block to execute
    
#### Practice Examples -

      count = 1
      while count <= 5:
          print(count)
          count += 1  # Increment count to avoid an infinite loop
          

      num = 1
      total_sum = 0
      
      while num <= 10:
          total_sum += num
          num += 1
      print("Sum of first 10 numbers is:", total_sum)



      secret_number = 7
      guess = None
      
      while guess != secret_number:
          guess = int(input("Guess the number: "))
          if guess < secret_number:
              print("Too low!")
          elif guess > secret_number:
              print("Too high!")
      
      print("You guessed it!")


    while True:
        print("This is an infinite loop!")


# Break Statement -
- The break statement in Python is used to exit a loop prematurely, whether it's a for loop or a while loop.
- When the break statement is encountered, the loop terminates immediately, and the program continues with the next line of code after the loop.


#### Examples-
    for i in range(1, 10):
        if i == 5:  # Break when i is equal to 5
            break
        print(i)
    


    num = 1
    while num <= 10:
        print(num)
        if num == 7:  # Break the loop when num is 7
            break
        num += 1
        


    number = 1
    while True:  # Infinite loop
        print(number)
        number += 1
        if number > 5:  # Break the loop when condition is met
            break
    

# Continue Statement -
- The continue statement in Python is used inside loops to skip the current iteration and move to the next iteration of the loop.
- When the continue statement is encountered, the rest of the code inside the loop is skipped for the current iteration, and the loop proceeds with the next iteration.

#### Example -
    for i in range(1, 6):
        if i == 3:
            continue  # Skip the iteration when i equals 3
        print(i)


    for i in range(1, 6):
        if i == 2 or i == 4:
            continue  # Skip if i is 2 or 4
        print(i)
        



    for i in range(1, 6):
        if i == 3:
            break  # Stop the loop when i is 3
        if i == 2:
            continue  # Skip printing when i is 2
        print(i)
        


















        
  
  
  
  

