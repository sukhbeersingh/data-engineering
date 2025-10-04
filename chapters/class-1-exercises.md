# Class 1 Exercises

1. Print the following pattern on your terminal:
```
       1
     2 3
   4 5 6
7 8 9 10
```

2. Create a `temperature.py` program that converts a number from Fahrenheit (°F) to Celsius (°C).
Google the current temperature of Brooklyn, NY in °F.
Use the following formula and write it out in Python:

```math
  Celsius= (Fahrenheit−32)/1.8
​
```

3. Create a pythogorean equation
Create a hypotenuse.py program that asks the user for two numbers, a and b, and then calculates the hypotenuse c.

```math
c= \sqrt{a^2+b^2}
```
​	
The a is the length of a short side.
The b is the length of another short side.
The c is the length of the hypotenuse.
The hypotenuse is the longest side of the right triangle. 

4. Catch bugs:
```
butterflies = 10
beetles = 12
ladybugs = 20

print('I caught ' + butterflies + ' 🦋 butterflies!')
print('I caught ' + beetles + ' 🪲 beetles!')
print('I caught ' + ladybug + ' 🐞 ladybugs!)

print('I caught ' + str(total) + ' total bugs!'
```

5. Create a grades.py program that checks whether a grade is above or below 55.

Start by creating a variable called `grade` and give it a value between 0-100.

Write a if/else statement for the following:

<b>If</b> grade is greater than or equal to 55, then print `"You passed."`

<b>Else</b>, print `"You failed."`
After you run the code, change grade's value and rerun it. Do this a few times to make sure it's working as intended.
Then change it to get value from user. 

6. Create a guess.py program and type in the following:

```
guess = 0

while guess != 6:
  guess = int(input("Guess the number:  "))

print("You got it!")
```
Run the code a few times so that you understand what it does.
Let's make it so that it's the same guessing game, but there is a new limit to the number of tries (it was infinite before).
First, introduce a variable called `tries` at the top and give it a value of 0.
Then, add a second condition with the `tries` variable to the while loop using a relational operator.

7. Write down the output for this code snippet.
```
import random

lucky_number = random.randint(1, 9)
not_found = True

while not_found:
  for i in range(1, 10):
    if i == lucky_number:
      not_found = False
      break
    else:
      print(i)

print(f"Yay I got my lucky number {lucky_number}! 🍀")
```

7. Create a todo.py program that will define a todo list that contains the following items:

```
'🏦 Get quarters.'
'🧺 Do laundry.'
'🌳 Take a walk.'
'💈 Get a haircut.'
'🍵 Make some tea.'
'💻 Complete Lists chapter.'
'💖 Call mom.'
'📺 Watch My Hero Academia.'
```
Print the first item and the second item. What did you get?

Next, use slicing to print the third, fourth, and fifth items.

Try printing out the item at index 9 to see the `IndexError` before moving on.

