---
layout: jumbotron
title: Operators
next: /tutorials/functions
back: /tutorials/intro_to_python
jumboimage: #
---

# What are operators?

In the last lesson you learned what variables are and how to initialize them with values. In this lesson we will learn how to perform simple operations on multiple variables. These simple operations are called **operators**, and the two variables that the operator operates on are called **operands**. You must make sure that you have initialized BOTH operands before you do an operation on them. If either variable doesn't have a value, Python will give you an error. There are a few types of operators:

- Arithmetic Operators - performs math on two variables
- Comparison Operators - compares two variables
- Assignment Operators - performs math on two variables and sets the left operand equal to the result
- Logical Operators - performs a logical operation on one or more variables
- Membership / In Operator - returns true when one variable is in another variable

# Arithmetic Operators

You've already seen these before, so these should be easy.

```python
a = 5
b = 10
#Addition
result = a + b #result is now 15
result = "AB" + "CD" #result is now "ABCD"
#Subtraction
result = a - b #result is now -5
#Multiplication
result = a * b #result is now 50
result = "AB" * 4 #result is now ABABABAB ("AB" copied 4 times)
#Division
result = b / a #result is now 2
#Modulus (Remainder)
result = a % b #result is now 5 because the remainder of 5 / 10 is 5
result = b % a #result is now 0 because the remainder of 10 / 5 is 0
#Exponent
result = a**b #result is now 9765625, 5 raised to the 10th power
```

# Comparison Operators

These operators compare two variables and return either `True` or `False`. In computer science, a value that is either true or false is called a **boolean** (named after George Boole apparently).

```python
#Equality (==) - evaluates to true ONLY IF both A and B are EQUAL - make sure to use TWO equal signs for this
True == False #False
True == True #True
False == False #True
1 == 2 #False
"Apple" == "Apple" #True
"apple" == "Apple" #False - even if only one character is different!

#Inequality (!=) - evaluates to true if A and B are DIFFERENT - the opposite of equality
True != False #True
"A" != "B" #True
"A" != "A" #False

#Greater Than (>) / Less Than (<)
10 > 5 #True
5.67 > 5.0 #True
7 < 10 #True
582099 > 10**10 #False
5 + 7 > 5 #True

#Greater Than Equal To (>=) / Less Than Equal To (<=)
10 >= 10 #True
6.0 <= 7.0 #True
```

# Assignment Operators

These operators perform an arithmetic operation on two variables, then store the result in the left operand. Make sure you know what += and -= do, since these are the most important assignment operators.

```python

a = 5
b = 10

#Addition to left operand (+=)
#this is the same as a = a + b
a += b #a is now its previous value + b's value, so in this case it is 15
#Subtraction from left operand (-=)
#this is the same as a = a - b
a -= b #a is now 5
#Multiplication to left operand (*=)
#this is the same as a = a * b
a *= b #a is now 50
#Division from left operand (/=)
#this is the same as a = a / b
a /= b #a is now 5

```

# Logical Operators

These operators perform logic on two booleans (a true or false value). They are normally used to combine comparison operators so that the program can make multiple comparisons at once. What is awesome about computer science is that it is built on logic, and I know that all of you are either taking logic or have taken logic, so you should be able to apply some of your logic skills to programming! Here are some examples:

## and

This operator evaluates to `True` if BOTH operands are `True`. 

```python
True and False #the right operand is false, so the entire expression is false
True and True #both operands are true, so the expression is true

myName = "LJ"
myGrade = 96.0

myName == "LJ" and myGrade > 76.0 #this is true because myName equals "LJ" AND myGrade is greater than 76.0
myName == "lj" and myGrade > 50.0 #this is false because myName is not equal to "lj" (even if myGrade is greater than 50.0, the expression is still false because one operand is false)
```

## or

This operator evaluates to `True` if EITHER operands are `True`

```python
True or False #the left operand is true, so the entire expresson is true
False or False #neither operand is true, so the expression is false

hasGameTicket = True
hasSeasonTicket = False

hasGameTicket or hasSeasonTicket #this is true because at least one operand is true
```

## not

This operator simply makes True False and False True. It flips the value of booleans.

```python
not True #this is False
not False #this is True

myAge = 17
not myAge == 17 #this is a bad way of writing myAge != 17
```

# Membership Operator / In Operator

This operator evaluates to True if the left operand is IN the right operand. This is very helpful when you are dealing with lists.

```python
groceryList = ["Iron Rod", "Nuclear Bomb", "Spaghetti"]

"Nuclear Bomb" in groceryList #this is true
"Eagle Claw" in groceryList #this is false, because there is not any item in groceryList that is equal to "Eagle Claw"

someNumbers = range(1, 100) #the numbers from 1 to 100

5 in someNumbers #true because 5 is between 1 and 100
101 in someNumbers #false because 101 > 100
```

# Real-World Examples

This is a snippet of code from a program I made to automatically play minesweeper. This specific block of code calculates the x and y value of where the mouse should be placed to click on a square.

```python
global mid, jumpX, jumpY
x = mid[0]+jumpX*place[0]
y = mid[1]+jumpY*place[1]
```

This is some code that used to generate a sine wave of a certain frequency. This wave can then be put into an audio file so that we can create some musical tones!

```python
math.cos(2 * freq * math.pi * float(i) / float(sampleRate))
```

# Summary

Wow that was alot of information! Unfortunately you will need to know all of these operators if you want to make a big program. But if you complete these exercises, you will know everything that you need relating to operators! I highly suggest looking back to this page if you need reference.

# Exercises

1. Use Python to find 6 raised to the 5th power.
2. Initialize two variables and compare them in some way
3. Let's say that `a = 456` and `b = 713`. What is the value of `a` after the operator `a += b`?
4. What is `(5 > 10) and (3 < 2)`?
5. What is `("Happy" == "Happy") or (False == True)`?
6. What operator do I use if I want to test for if an item is in a list?
