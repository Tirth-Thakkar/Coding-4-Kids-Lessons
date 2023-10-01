---
toc: True
comments: True
layout: notebook
author: Tirth Thakkar
title: Week 1 Lesson and Notes
description: Class one content and examples
categories: ['week01']
---

## Quiz
Dictionary being used to run the quiz. With user input being processed using the input function learned about in class and the if/else statements to determine if the user input is correct or incorrect.


```python
Q_Bank = {
    "Dynamic code is code that has inputs and outputs that can change?":"true",
    "What is the keyword for defining a function in Python?": "def",
    "In Jupyter Notebooks the Input is in line with the Output": "false",
    "What is grouping often used commands called?": "procedural abstraction",
}

score = 0 # Variables like score and Q_Bank can store a variety of data types from score which is an integer to Q_Bank which is a dictionary
for Q, ans in Q_Bank.items():
    print(Q)
    rsp = input(Q)
    if rsp.lower().strip() == ans.lower().strip():
        print(f"Your answer {rsp} is the correct correct")
        score += 1
    else:
        print(f"Your answer {rsp} doesn't equal the correct answer/s which is {ans}")
print(f"Your score is {score} out of {len(Q_Bank)} points.")

```

    Dynamic code is code that has inputs and outputs that can change?
    Your answer true is the correct correct
    What is the keyword for defining a function in Python?
    Your answer cheese doesn't equal the correct answer/s which is def
    In Jupyter Notebooks the Input is in line with the Output
    Your answer  doesn't equal the correct answer/s which is false
    What is grouping often used commands called?
    Your answer  doesn't equal the correct answer/s which is procedural abstraction
    Your score is 1 out of 4 points.



```python
# Making a rectangle and area program with user input in python

user_length = int(input("Please enter the length of you rectangle:")) 
user_width = int(input("Please enter the width of your rectangle:"))

# Perimeter of a rectangle is 2(l+w)

perimeter = 2*(user_length + user_width)
# print(f"The perimeter of your rectangle is {perimeter}")
print("The perimeter of your rectangle is " + str(perimeter) + " units")

# Area of a rectangle is l*w

area = user_length * user_width
# print(f"The area of your rectangle is {area}")
print("The area of your rectangle is " + str(area) + " units")
```

    The perimeter of your rectangle is 28 units
    The area of your rectangle is 24 units


## Conditional Statements 
- When a conditional statement is used, it is used to determine if a statement is true or false. Then depending on the outcome of the statement, the program will run a certain way. There are three different conditional statements within python `if`, `elif`, and `else`. The `if` statement is used to determine if a statement is true or false. The `elif` statement is used to determine if the previous statement was false and if the current statement is true. The `else` statement is used to determine if the previous statement was false and if the current statement is false. Seen bellow in code segments from in class. 


```python
# Voting eligibility program

user_age = int(input("What is your age?"))
user_citizen = input("Are you a citizen of the United States?")

if user_age >= 18 and user_citizen.lower().strip() == "yes":
   print("You are eligible to vote")

else:
    print("You are not eligible to vote")

```

    You are eligible to vote



```python
# Voting eligibility program

user_age = int(input("What is your age?"))
user_citizen = input("Are you a citizen of the United States?")

if user_age >= 18 and user_citizen.lower().strip() == "yes":
   print("You are eligible to vote")

# Elif or else if to evaluate another condition
elif user_age < 18 and user_citizen.lower().strip() == "yes":
    print(f"You will be eligible to vote in {18 - user_age} years")

else:
    print("You are not eligible to vote")
 
```

    You will be eligible to vote in 9 years



```python
let age = 18
let citizen = "yes"

if (age >= 18 && citizen == "yes") {
    console.log("You are eligible to vote")
}
```

    You are eligible to vote

