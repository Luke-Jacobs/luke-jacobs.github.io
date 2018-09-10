---
title: Loops
layout: jumbotron
next: /tutorials/strings
back: /tutorials/operators
jumboimage: /tutorials/imgs/loops2.png
---

Loops do the heavy lifting in a program, allowing it to do things that humans cannot. For example, a security system might have a loop integrated into its program to check a camera once every second. Computers are always vigilant, unlike some security guards, and you don't have to pay them! Loops simply execute a block of code over and over again until a stopping point.

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

This program simply prints my todo list item by item. What Python is doing is initializing `thingToDo` with every item in `toDoList`, then running the indented code section underneath it (called the loop block). When the indented section is done, it cycles back around to the top of the indented section until it has cycled through the entire list. With this loop you can perform an operation given **each item** in a list. 

Another example is multiplying the numbers from 1 to 100. (I don't know why any sane individual would want to do that, but let's do it anyway!) Here is the code:

```python
n = 1 #this is the variable we will be multiplying by each number
for i in range(1, 100): #this is the top of the loop
	n = n * i #with each loop, n's value is increasing
print n #display the final value of n
```  

Let's explain what's going on here. On the first line, `n` is set to the value of 1. On the next line, the loop is setup: `i` is our loop variable and `range(1, 100)` is our iterable variable. This means that Python will cycle through the contents of `range(1, 100)` and for each item in that variable, `i` will be set to that variable. So on the first loop `i` is equal to 1. On the next loop `i` is equal to 2, and so on. The third line is the indented, so this will be the code that we will run for each item in our iterable. In this case, `n` is being set to its current value times the value of `i`. This means that `n` is always getting larger in value, because `i` is growing in value as the program runs. At the end of the program, the value of `n` will be the product of all the numbers from 1 to 100!

Here is an example of a more difficult-to-understand program, but I'm sure you guys will be able to figure it out!

```python
xValues = range(1, 100) #numbers from 1 to 100
yValues = [] #this is an empty list

for x in xValues: #loop start
	y = x**2 + 5*x + 8 #this is the most important line
	yValues.append(y) #add y value to the list
	
print yValues
```

This program fills the list `yValues` with 100 numbers. Each number in the list is the output of `x**2 + 5*x + 8` given a certain `x` value. Let's look at the start of the loop. On the first cycle of the loop, what is the value of `x`? Well, it is just the first item in the list `xValues`. We know that `xValues` is just a list of all the numbers from 1 to 100, so the first item in the list is just 1. That means on the first iteration of our loop, `x` is 1. On the next iteration, it is the next item in the list `xValues`, which is 2. On each iteration, there is a value added to the `yValues` list. This value is dependent on the value of x, because `y = x**2 + 5*x + 8`. I hope you can visualize what is going on. The output of this program is always:

```python
[14, 22, 32, 44, 58, 74, 92, 112, 134, 158, 184, 212, 242, 274, 308, 344, 382, 422, 464, 508, 554, 602, 652, 704, 758, 814, 872, 932, 994, 1058, 1124, 1192, 1262, 1334, 1408, 1484, 1562, 1642, 1724, 1808, 1894, 1982, 2072, 2164, 2258, 2354, 2452, 2552, 2654, 2758, 2864, 2972, 3082, 3194, 3308, 3424, 3542, 3662, 3784, 3908, 4034, 4162, 4292, 4424, 4558, 4694, 4832, 4972, 5114, 5258, 5404, 5552, 5702, 5854, 6008, 6164, 6322, 6482, 6644, 6808, 6974, 7142, 7312, 7484, 7658, 7834, 8012, 8192, 8374, 8558, 8744, 8932, 9122, 9314, 9508, 9704, 9902, 10102, 10304]
```

I hope you can see from this example that computers are VERY powerful math machines. What a computer can do in milliseconds would take you many excruciating hours of back-breaking, brain-hurting, miserable calculations. 

# While Loop

This loop executes _while_ an expression is true. This is the format: 

# While Loop Format

```python
while expression:
	do
	something
	here
```

This is where comparison operators come into play -------

# Real-World Example

This is a real-world example of some code I wrote to automatically download NY Times article data from their database. I didn't do this because I love their articles, but because I wanted a computer to replicate their headlines. I don't expect you to understand much of it:

```python
for year in years:
    data = collectInfoByYear(year, keys)
    print("Writing %d year info to %s..." % (year, filename))
    fp.write(data)
```

This code block writes NY Times article properties to a file given a range of years. I chose to grab all the article data from 1852 to 2017. I'm so glad I don't pay for internet by the byte! Oh, and by the way this took under a minute to grab and write to a file! 

# Exercises

1. Write a program to add all the numbers from 50 to 100.

