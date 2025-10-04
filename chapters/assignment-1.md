# Assignment 1

1. Create a github account.
2. Create a new public repository.
3. In that repository, create a `.py` file for each question as mentioned.
4. Create a corresponding `.md` file with the result screenshots.
5. Submit the link to your public repository.

## Problem 1
In chemistry, pH is a scale used to specify the acidity or basicity of a liquid. 🧪

Create a ph_levels.py program that checks whether a pH level is basic, acidic, or neutral.

First, create a ph variable and ask the user for a value between 0 and 14.

Write an if, elif, else statement that:

If ph is greater than 7, output "Basic".
If ph is less than 7, output "Acidic".
Else, output "Neutral".

## Problem 2 
The Magic 8 Ball is a popular office toy and children's toy invented in the 1940s for fortune-telling and advice seeking. 🎱

It's an oversized 8 ball with some of the following answers:

```
Yes - definitely.
It is decidedly so.
Without a doubt.
Reply hazy, try again.
Ask again later.
Better not tell you now.
My sources say no.
Outlook not so good.
Very doubtful.
```

Create a `magic8.py` program that can respond to any Yes or No questions with a different answer each time it executes.

The output should have the following format:

```
Question:      [Question]
Magic 8 Ball:  [Answer]
```

For example:

```
Question:      Is Apple better than Orange yet?
Magic 8 Ball:  Better not tell you now.
```

## Problem 3
Since 1927, "The Cyclone" roller coaster has delighted visitors at Coney Island (Brooklyn, NY). 🎢
They're now installing a new entry system (the height requirement is 137 cm and the cost is 10 credits) and need your help writing the program for it!

Create a new file called `the_cyclone.py`.
Ask the user what their height is and how many credits they have, and store the values in a height variable and a credits variable.
Use a combination of relational and logical operators to create the rules:
If they are tall enough and have enough credits, print "Enjoy the ride!"
Else if they have enough credits, but they aren't tall enough, print "You are not tall enough to ride."
Else if they are tall enough, but they don't have enough credits, print "You don't have enough credits."
Else, print a message saying they have not met either requirement.


## Problem 4
The Sorting Hat is a magical talking hat at Hogwarts School of Witchcraft and Wizardry. The hat decides which of the four "Houses" each first-year student goes to:

🦁 Gryffindor
🦅 Ravenclaw
🦡 Hufflepuff
🐍 Slytherin

Write a `sorting_hat.py` program that asks the user some questions with the int() and input() functions:

```
Q1) Do you like Dawn or Dusk?
    1) Dawn
    2) Dusk
```

If answer is equal to 1, Gryffindor and Ravenclaw both get a +1.
Else if answer is equal to 2, Hufflepuff and Slytherin both get a +1.
Else, output the message "Wrong input."

```
Q2) When I’m dead, I want people to remember me as:
    1) The Good
    2) The Great
    3) The Wise
    4) The Bold
```

If the answer is 1, Hufflepuff +2.
Else if answer is 2, Slytherin +2.
Else if answer is 3, Ravenclaw +2.
Else if answer is 4, Gryffindor +2.
Else, output the message "Wrong input."

```
Q3) Which kind of instrument most pleases your ear?
    1) The violin
    2) The trumpet
    3) The piano
    4) The drum
```

If the answer is 1, Slytherin +4.
Else if the answer is 2, Hufflepuff +4.
Else if the answer is 3, Ravenclaw +4.
Else if the answer is 4, Gryffindor +4.
Else, output "Wrong input."
Lastly, print out the score for each house.

<b>Bonus</b>: If you want to go further, see if you can figure out how to print out the house with the most points!

## Problem 5
Fizz Buzz is a children's word game that teaches division. It's also a classic technical interview question at countless companies. 🐝

Though this challenge may appear simple to experienced coders, it is designed to weed out 90% of job candidates who cannot apply their coding knowledge to a new problem creatively. Want to give it a try?

Create a `fizz_buzz.py` program that outputs numbers from 1 to 100.

Here's the catch:

For multiples of 3, print "Fizz" instead of the number.
For multiples of 5, print "Buzz" instead of the number.
Here's the tricky part: For multiples of 3 and 5, print "FizzBuzz".
The output should look like:

```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
...
```

## Problem 6 
Create a file `square_sum.py` and add the following code.

A number is "squared" when it is either multiplied by itself or taken to the second power (e.g., 4² = 4 x 4 = 16).

First, ask the user for an integer with int(input()) and store it in a `number` variable. Then, define a total variable with an initial value of 0.
Note: You can pass a string prompt to `int(input())`.

Next, use a `for` loop and `range()` function to calculate the total of the squares of all integers from 1 to that `number`.

Last, print the output as an integer value.
For example, if `number` is 5, the total should be 55 because:

```math
1^2+2^2+3^2+4^2+5^2
=1+4+9+16+25
=55
```

## Problem 7
Create a `reading_list.py` program that stores the following items in a books list:

```
'Harry Potter'
'1984'
'The Fault in Our Stars'
'The Mom Test'
'Life in Code'
```
Suppose we want to add 'Pachinko' to the list. Can you use a list method to do so?

Let's say we finished reading 'The Fault in Our Stars' and '1984'. 
Can you use the .remove() method to remove one and the .pop() method to remove the other?
Print to make sure the list is updated.

## Problem 8
Create `dna.py` and code the following.

DNA is made of the following four pieces:

Adenine (A)
Cytosine (C)
Guanine (G)
Thymine (T)
A DNA sequence is made of three-letter combinations of these pieces, such as 'ACG', TCA', and 'CGT'.

Let's use a Python list to find a specific three-letter combination, starting with the following:

```
dna_sequence = ['GCT', 'AGC', 'AGG', 'TAA', 'ACT', 'CAT', 'TAT', 'CCC', 'ACG', 'GAA', 'ACC', 'GGA']
```

Next, define two variables:

`item_to_find` string that is set as a three-letter combination of your choice, with no spaces (e.g. 'TGA' or 'CAT').
`item_found` boolean, initialized to `False`.
Loop through each item in the `dna_sequence` list. Inside, use an if statement to test if a given item is equal to the `item_to_find`. If so, set `item_found` to `True`.

Outside the loop, use an `if/else` statement to check if `item_found` is `True`:

If so, print something like `"Item Found!"`
Else, print something like `"Item not found.`

## Problem 9
Create `fortune-cookie.py` and create the code as mentioned.
Fortune Cookie is a small cookie wafer with a piece of paper inside, called a “fortune”, which is usually a Chinese phrase with translation and a list of lucky numbers. They are served in restaurants in the U.S. and Canada. 🥠

Create a fortune_cookie.py program that gives the user random fortunes.

Define a function named fortune(). Inside the function, print out a random fortune from the list of options below:

Don't pursue happiness – create it.
All things are difficult before they are easy.
The early bird gets the worm, but the second mouse gets the cheese.
Someone in your life needs a letter from you.
Don't just think. Act!
Your heart will skip a beat.
The fortune you search for is in another cookie.
Help! I'm being held prisoner in a Chinese bakery!
Make sure to use the random module's random.randint() and an if/elif/else.

Then, call the fortune() function three times and see what you get!

Bonus: If you're daring, rewrite the function without an if/elif/else.

## Problem 10
Suppose you're a NASA intern, and your team is calculating the distance a rocket needs to travel. The value calculated is in kilometers, while the next step requires miles. Your manager quickly writes this on the board:

```math
miles= 1.609/kilometer
```
​	
Create a new file called `rocket.py`.

Define a function named `distance_to_miles()` that converts a distance from kilometers to miles. It should:

Take in one parameter named `distance` (the distance in kilometers).
Print the distance in miles.
After, call the function and use 10000 as the argument.

## Problem 11
Let's try a classic Computer Science project: simple calculator program! 🔢

Create a `calculator.py` program and define these five functions:

- `add(a, b)` that adds two numbers a and b.
- `subtract(a, b)` that subtracts two numbers a and b
- `multiply(a, b)` that multiplies two numbers a and b.
- `divide(a, b)` that divides two numbers a and b.
- `exp(a, b)` that takes a to the exponent (or power) of b.
Make sure to return the result in each function definition.

Test your calculator by calling each function once to make sure that it works!

## Problem 12
In fintech, we often perform a time series analysis on stocks. 

This means that we need to analyze a stock, given its price over a certain time. 📈 

In this exercise, we will perform a simplified version of a time series analysis. 

The stock that we will be analyzing is the $AMC stock in January 2023. 
Here are the stock prices (in dollars) for each of these weekdays: 

```
stock_prices = [34.68, 36.09, 34.94, 33.97, 34.68, 35.82, 43.41, 44.29, 44.65, 53.56, 49.85, 48.71, 48.71, 49.94, 48.53, 47.03, 46.59, 48.62, 44.21, 47.21]
```
Create a `stock_analysis.py` program that implements three functions: 
- `price_at(x)` that finds the price on a given day x. 
- `max_price(a, b)` that finds the maximum price from day a to day b. 
- `min_price(a, b)` that finds the minimum price from day a to day b. 

The parameters of the days will be in the range of 1 to 20 (since that is the period for the stock we are analyzing). 

Make sure to call each function to test if your functions work correctly!

## Problem 13

When you go to a drive-thru like Harvey's, you can order food using the item numbers. For example, a Delulu Meal might be a **#3**!  

1. Create a `drive_thru.py` program with your favorite fast food chain's menu.

2. Define a function named `get_item()` that:
    - Takes in **one parameter**, the number of the item you want to order.
    - Returns the **name of that item**.

3. Example item numbers and menu:
    - Argument value `1` → `'🍔 Cheeseburger'`
    - Argument value `2` → `'🍟 Fries'`
    - Argument value `3` → `'🥤 Soda'`
    - Argument value `4` → `'🍦 Ice Cream'`
    - Argument value `5` → `'🍪 Cookie'`

4. Call the `get_item()` function a few times to make sure it works correctly.

5. Create a `welcome()` function that prints the **welcome menu**.

6. Create a **main program** that:
    - Displays the welcome menu.
    - Takes user input with `input()` to allow them to order items.


