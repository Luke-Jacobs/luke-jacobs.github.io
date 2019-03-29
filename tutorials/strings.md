---
title: Strings
next: /tutorials/functions
back: /tutorials/operators
layout: lesson
---

# What are strings?

Hopefully you know a little about strings from the last lesson. This lesson will give you an in-depth look at what they are and how to perform operations on them. A string is a **sequence of characters**. Well what is a sequence and what are characters? A sequence is a list composed of elements (or items). Characters are just letters, numbers, and symbols on your keyboard. But to a computer they are represented as numbers, since a computer can only deal with numbers. So we humans made a system of encoding letters as numbers so that we can store text as numbers. This encoding is called **ASCII**.

![Ascii Table](imgs/ascii_table.gif)

You might be wondering what char, dec, oct, and hex stand for. Well, char just means character and dec means decimal, which is the name for our normal number system. Oct and hex stand for octal and hexadecimal, neither of which you need to know right now, but in case you are wondering, they are just different number systems that represent numbers differently. If you look at the table, you can see that each character corresponds to one number, which is how the computer stores the information for each character. This means that in computer memory, strings are just lists of small numbers, but when we display strings, the computer automatically converts the numbers to characters so that we can read the text!

# What can I do with strings?

There are VERY many uses of strings, so I'll cover the ones I use most often. 

# String Splicing

First, you need to understand string splicing. String splicing is the operation of cutting up a big string into what are called **substrings**. Substrings are pieces of a big string. Here is a helpful image that demonstrates how to program this operation:

![String Splicing](imgs/strings_example0.png)

Programming languages start counting **indices** (the plural of index) at 0. This means that the first letter of a string is at index 0, and the second letter of a string is at index 1, etc until the end of the string. This means that:

```python
myString = "Computer Science"

print myString[0] #this prints "C"
print myString[1] #this prints "o"
```

Using one index allows you to grab one letter. But what if we wanted to grab an entire section from a string? That requires using multiple indices. Here is the format for string splicing:

# String Splicing Format
```python
myStringVariable[start:end:step]
```

You need to know what **start**, **end**, and **step** mean. **start** is the start index that points to the first character of a substring. **end** is the index of the first letter that is NOT INCLUDED in the substring. For example, if your start index is 0, then that means your substring will start at the first character in a string. If your end index is 9, your substring will STOP BEFORE the 10th character in the string, since the index of 9 is the same thing as the 10th character (because Python starts counting at 0). Here are some examples:

```python
myString = "Computer Science"
#           0123456789012345

print myString[0:8] #this prints "Computer"
print myString[9:16] #this prints "Science"
print myString[1:7] #this prints "ompute"
print myString[0:16] #this prints "Computer Science"
print myString[0:1] #this prints "C"
```

You can also **omit start and end**. If you omit the start index, Python will assume you mean to start your substring at the very beginning of the string. If you omit the end index, Python will assume you want your substring to continue all the way to the end of the string. Here are some examples of omitting start and end indices:

```python
mySchool = "Naperville Christian Academy"

print mySchool[:5] #this is an omission of the start index, and it will print "Naper"
print mySchool[11:] #this is an omission of the end index, and it will print "Christian Academy"
print mySchool[::] #this is an omission of both indices, and it is the same thing as printing mySchool without any splicing
```

# Split

This is a string operation that I use ALOT. This operation splits a string into substrings at a **separator**. Python uses the **separator** as a place to cut a string. This operation allows us to iterate through parts of a string. We can essentially convert a string into a list of small strings. Here are some examples of the split operation:

```python
itemsToBake = "Cabbage Wheel Cheese Bread" #itemsToBake is a string
itemsToBake = itemsToBake.split(" ") #itemsToBake is now a list of small strings
firstItemToBake = itemsToBake[0] #this is "Cabbage"
firstTwoItemsToBake = itemsToBake[:2] #this is ["Cabbage", "Wheel"]

sentence = "I love to use semicolons; they join two independent clauses"
sentenceParts = sentence.split("; ") #split at each occurence of "; "
part1 = sentenceParts[0] #the item at index 0 is the first item!
part2 = sentenceParts[1] #the item at index 1 is the second item
```

# Real-World Examples

```python
myBadAverage = 0.0
aStringOfSomeBadGrades = "30.76, 64.32, 21.0, 34.98, 54.36" #this is the string we are going to be dissecting
aListOfSomeBadGrades = aStringOfSomeBadGrades.split(", ") #this splits aStringOfSomeBadGrades into 5 small strings at each place where ", " occurs
print aListOfSomeBadGrades #this will print "['30.76', '64.32', '21.0', '34.98', '54.36']"

sumOfBadGrades = 0.0
for badGrade in aListOfSomeBadGrades: #iterate through the list so that we can perform operations on each item
	sumOfBadGrades += float(badGrade) #convert each string to a floating-point number (just a decimal) and add it to our sum!
myBadAverage = sumOfBadGrades / len(aListOfSomeBadGrades) #take our sum and divide it by how many grades we have - this will give us an average

print myBadAverage #this shows us the average of all our bad grades - it prints "41.084"
```

# Exercises

1. What code would I write to extract the "A" from "ABCDEF"?
2. Ask Luke for more exercises. 