---
layout: jumbotron
title: Intro to Variables
next: /tutorials/functions
back: #
jumboimage: /tutorials/imgs/data.jpg
---

# Initialization

Before you do any type of operation, whether that be downloading a website or hacking into Mr. Vahle's projector, you need to **initialize** some variables. In order to **initialize** some variables, you need to give your variable a **name** and a **value**. In math, variable names are quite boring - they are just letters like x and y. But in the realm of computer science, you can throw away those boring x and y's and replace those variable names with any name you choose! Well...not any name. There are a few rules to naming variables in Python:

- You cannot start your variable name with a number
  - Good: `twohorses` or `horses2`
  - Bad: `2horses`
- You cannot have spaces in your variable name (or else Python will get confused)
  - Good: `luke_jacobs_age`
  - Bad: `luke jacobs age`
- You cannot use special symbols (those are reserved for operations)
  - Good: `ilovepython`
  - Bad: `il@vepyth()n!`

My best guidelines for naming variables are to only use the alphabet and to keep variable names short, since in order to reference variables you need to type out their names. Now, how do we assign variables a value? Well, this brings us to the topic of data types. 

# Data Types

In this world, some data is different than other types of data. For example, say you have a temperature reading in Celsius and a list of student names. With a list, you can sort its individual elements and order them nicely, but you can't do that with a single data point. With a Celsius temperature value, you can convert that value to a temperature in Fahrenheit, but you can't convert a list of names into a Fahrenheit number. It just doesn't make sense. This is why there are different types of variables in Python. Here is a list of some of the built-in types of data:

- Integer (Ints)
  - any number without a decimal point 
  - Ex: `-1, 0, 7`
- Floating-Point Number (Floats)
  - any real number 
  - Ex: `8.678, -5.67, 1.0, 0.0`
- String 
  - a sequence of characters 
  - Ex: `"Some random text", "ThisIsAGoodPassword1234CATZ"`
- List 
  - a collection of other variables 
  - Ex: `[6, 7.0, 8], ["A", "B", "C"]`
- Dictionary 
  - a sequence of keys that correspond to values
  - Ex: `{"apple": "a fruit", 9: "Eaten by 7"}`
- Streams 
  - a source of data that can be read
  - Ex: `open("myshakespearebook.txt", "rb")`

These are just a few of the variable types that Python has to offer us. Each of these types have different attributes. For example, a list has an index attribute which allows access to individual items (we can grab the second item in the list), just like a string (we can grab the second letter in a sentence). Both the floating-point number type and the integer type have an attribute that allows them to be added to other numbers (we can do 5.6 + 6 which gives us 11.6), but you can't add a list and an integer ([6,8,1] + 7 gives us an error). The point I am trying to make is that these data types share some similarities, but some are very different from each other.

Your job as a programmer is to know when to use a certain data type. When you are dealing with data in English or data that contains English letters, like a website, you are almost always going to use a string to store that data. If you are dealing with precise data like a scientific measurement, you are going to want to use a float because that data type can store a number with a decimal point, unlike an int.

Integers (ints), floating-point numbers (floats), strings, and lists are the most common data types in programming, so make sure you know how they work! Here are a few examples of initializing variables with a specific data type:

# Examples

```python
#-----Initializing Integers-----

carModel = 12387 #from now on carModel is the value of 12387
studentID = 7320
a = 5 + 7 #simple addition
b = 4*6 + 7*6 #make sure you know your order of operations!
c = 6 / 5 #because these are both ints, c will be set to the value of 1 because ints cannot have decimal points, so the .2 is chopped off
d = pow(2, 100) #this function returns the value of 2 raised to the 100th power!
d = d + 1 #this takes the value of d, adds 1 to it, and stores that value back in d.

#-----Initializing Floats-----

myMathGrade = 120.567
myAPBioGrade = 0.8752
pi = 3.1415926
circumference = 2 * pi * 5 #this retreives the value of the variable named "pi", multiplies it twice, and sets the variable "circumference" equal to the value

#-----Initializing Strings-----

myName = "Caillou the Great"
myFavoriteSong = "The Grinch Song sung by Gabe"
myNickname = "Luke" + "Jacobs" #this combines the strings "Luke" and "Jacobs" together but DOES NOT PUT A SPACE IN BETWEEN THEM

#-----Initializing File objects-----

myFile = open("mychristmaslist.txt", "r") #this opens the file "mychristmaslist.txt" as read-only

```

# Exercises

1. I named my variable `3 blind mice` and Python gave me an error! Why did this happen?
2. Why are there different data types in Python?
3. Write a program that initializes a variable with the value of 2 times 8 times 9.
  
