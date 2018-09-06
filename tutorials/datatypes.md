---
layout: jumbotron
title: Data Types
jumboimage: /tutorials/imgs/data.jpg
---

The main point I want you to come away with after reading this lesson is that some types of data are treated differently than other types of data.

For example, says you have a temperature reading in Celsius and a list of student names. With a list, you can sort its individual elements and order them nicely, but you can't do that with a single data point. With a Celsius temperature value, you can convert that value to a temperature in Fahrenheit, but you can't convert a list of names into a Fahrenheit number. It just doesn't make sense. 

This is why there are different types of variables in Python. Here is a list of some of the built-in types:

- Integer 
  - any number without a decimal point 
  - Ex: -1, 0, 7
- Floating-Point Number 
  - any real number 
  - 8.678, -5.67, 1.0
- String 
  - a sequence of characters 
  - "Some random text"
- List 
  - a collection of other variables 
  - [6,7,8], ["A", "B", "C"]
- Dictionary 
  - a sequence of keys that correspond to values
  - {"apple": "a fruit", 9: "Eaten by 7"}
- Streams 
  - a source of data that can be read
  - open("myshakespearebook.txt", "rb")

These are just a few of the variable types that Python has to offer us. Each of these types have different attributes. For example, a list has an index attribute which allows access to individual items (we can grab the second item),   just like a string (we can grab the second letter in a sentence). Both the floating-point number type and the integer type have an attribute that allows them to be added to other numbers (we can do 5.6 + 6 which gives us 11.6), but you can't add a list and a integer ([6,8,1] + 7 gives us an error)
