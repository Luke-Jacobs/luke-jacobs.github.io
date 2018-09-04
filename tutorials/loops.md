---
title: Loops
layout: jumbotron
jumboimage: imgs/loops.webp
---

Loops do the heavy lifting in a program, allowing it to do things that humans cannot. For example, a security system might have a loop integrated into its program to check a camera once every second. Computers are always vigilant, unlike some security guards, and you don't have to pay them.

There are two types of loops in Python:

- `for` loop - interates through an iterable item
- `while` loop - runs _while_ an expression is true

Don't worry if those definitions are confusing, because I'll be explaining them. A `for` loop iterates (or cycles) through an iterable variable, like a list. On each cycle, the **loop variable** is set to a different value. This is the format for a `for` loop (remember this!):

# For Loop Format

```python
for loop_variable in iterable_variable:
	do
	something
	here
```

A specific example:

```python
toDoList = ["eat brick", "fly sideways", "photograph the moon"] #initialize todo list

for thingToDo in toDoList: #loop through each item
	print thingToDo #print each item
```

This program simply prints my todo list item by item. What Python is doing is initializing `thingToDo` with every item in `toDoList`, then running the indented code section underneath it. When the indented section is done, then it cycles back around to the top of the indented section until it has cycled through the entire list.

Another example is multiplying the numbers from 1 to 100. (I don't know why any sane individual would want to do that, but let's do it anyway!) Here is the code:

```python
n = 1 #this is the variable we will be multiplying by each number
for i in range(1, 100):
	n = n * i
print n
```  

Let's explain what's going on here. On the first line, `n` is set to the value of 1. On the next line, the loop is setup: `i` is our loop variable and `range(1, 100)` is our iterable variable. This means that Python will cycle through the contents of `range(1, 100)` and for each item in that variable, `i` will be set to that variable. So on the first loop `i` is equal to 1. On the next loop `i` is equal to 2, and so on. The third line is the indented, so this will be the code that we will run for each item in our iterable. In this case, `n` is being set to its current value times the value of `i`. This means that `n` is always getting larger in value, because `i` is growing in value as the program runs. At the end of the program, the value of `n` will be the product of all the numbers from 1 to 100!

This is a real-world example of some code I wrote to automatically download NY Times articles from their database. (I didn't do this because I love their article, but because I wanted a computer to replicate their headlines.) I don't expect you to understand much of it:

# Real-World Example

```python
for year in years:
    data = collectInfoByYear(year, keys)
    print("Writing %d year info to %s..." % (year, filename))
    fp.write(data)
```

This code block writes NY Times article properties to a file given a range of years. I chose to grab all the article data from 1852 to 2017. I'm so glad I don't pay for internet by the byte!

# Exercises
Write a program to add all the numbers from 50 to 100

