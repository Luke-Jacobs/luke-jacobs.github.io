---
layout: lesson
---

# Concepts

- ### Assigning variables
  You assign a variable a value by following this format: `variableName = variableValue`.

  ```python
  myVar = 5
  myName = "My name is Charles"
  myUserInput = input("This is a prompt for the user to enter some text:")
  aBigNumber = 5**10  # 5 to the power of 10
  ```

  Do not use the double equals sign (`==`)! That is for comparators!

- ### Operators

  Operators are symbols that perform operators on one or more variables. For example:

  ```python
  a = 5
  b = 9
  
  # Simple math
  a + b  # Addition
  a - b  # Subtraction
  a * b  # Multiplication
  a / b  # Division
  
  # Comparison - used in "if" blocks
  a == b  # Returns True if a equals b
  a != b  # Returns True if a is not equal to b
  a > b   # Returns True if a is greater than b
  a < b   # Returns True if b is greater than a
  
  # Membership - used in lists
  myList = [5, 9, 7]
  a in myList  # Returns True if a (5) is in myList
  10 in myList # This is False
  a not in myList  # Returns False because a is in myList
  ```

- ### Loops

  Loops do things multiple times. Each loop is a little different.

  - The `for` loop iterates over a list. This means it runs its assigned code block for every item in a given list. For example:

    ```python
    myLetters = ['a', 'b', 'z', 'y']
    for letter in myLetters:
        print("Let's say another letter:", letter)  # Prints a different letter each run-through of the loop
    
    myName = "Luke Jacobs"
    for letter in myName:
        # Do something with "letter"
        # FYI - at one point in the loop, letter is equal to " ", a space character. Spaces count as characters too!
    
    myNumbers = [56, 6212, 948390583209]
    mySum = 0
    for n in myNumbers:
        mySum = mySum + n
    # (This code adds up all the numbers in this list)
    ```

  - The `while` loop runs *while* a given condition is True.

    ```python
    myAge = 17
    whenIDie = 32  # Probably a hang-gliding accident
    while (myAge < whenIDie):
        print('You are still alive for this year!')
        myAge = myAge + 1  # Increment my age by 1 - AKA I had a birthday
    print('You have died :(')
    ```

- ### Functions

  I don't have enough time to do all this. I have a life too, you know.

