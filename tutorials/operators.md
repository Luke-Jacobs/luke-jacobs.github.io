---
layout: jumbotron
title: Operators
next: /tutorials/functions
back: /tutorials/intro_to_python
jumboimage: #
---

# What are operators?

In the last lesson you learned what variables are and how to initialize them with values. In this lesson we will learn how to perform simple operations on multiple variables. These simple operations are called **operators**, and the two variables that the operator operates on are called **operands**. You must make sure that you have initialized BOTH . There are a few types of operators:

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
#Subtraction
result = a - b #result is now -5
#Multiplication
result = a * b #result is now 50
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

These operators perform an arithmetic operation on two variables, then store the result in the left operand. You CANNOT use this operator if one of your variables 

```python
