## Class 1

### Data and Instructions
There are two main components of how any computer system works. Data - where its stored, how its stored, how much can be stored. 
Instructions - 
* what to do with that data
* how is that data transformed
* where does it get stored

Binary expression of data -
0 & 1 (False and True)
01 - 10 (1-3)
11 
[Link](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:digital-information/xcae6f4a7ff015e7d:binary-numbers/a/bits-and-binary)


### Variables
* int, or integer: a number without a fractional part. savings, with the value 100, is an example of an integer.
```
year = 2023
age = 32
```
* float, or floating point: a number that has both an integer and fractional part, separated by a point. 1.1, is an example of a float.
```
pi = 3.14159
meal_cost = 12.99
```
* str, or string: a type to represent text. You can use single or double quotes to build a string.
```
message = "good nite"
username = '@snoopdogg'
```
* bool, or boolean: a type to represent logical values. It can only be True or False (the capitalization is important!).
```
late_to_class = False
cranky = True
```

### Printing to the terminal (stdout|stdin)
```print('Hello World')```

### Operators
Python has the following arithmetic operators:

* `+` Addition
* `-` Subtraction
* `*` Multiplication
* `/` Division

Use PEMDAS (Parentheses, Exponents, Multiplication/Division, Addition/Subtraction) for order of operator execution. 

#### Modulo
The % modulo operator doesn’t give you the result of a division – it gives you the remainder.

```
score = 5 % 3       # score is 2
score = 5 % 2       # score is now 1
score = 5 % 1       # score is now 0
```

#### Exponents

Python can also perform exponentiation such as 2³ or 10².
So 2 ** 3 is 2³ and 10 ** 2 is 10².

Here are more examples:
```
score = 2 ** 2      # score is 4
score = 2 ** 3      # score is now 8
score = 2 ** 4      # score is now 16

print(score)        # Output: 16 - why?
```

### Input 
How can we get input from the user? Use `input()`
What if we want the input to be stored in a certain type of data (Datatype)?
```
number = int(input("please enter a number value"))
```

### Errors
*`SyntaxError`: this occurs when invalid Python code is present.
*`NameError`: this occurs when you're trying to use a variable without declaring it first.
*`TypeError`: this occurs when the data type you're using doesn't suit what you're trying to do.

#### SyntaxError
```
print(Hello, World!
# SyntaxError: invalid syntax
```
<details> 
  <summary>
   What is the error?
  </summary>
   
  ```
    File "main.py", line 1
    print(Hello, World!
                      ^
    SyntaxError: invalid syntax
  ```

</details>

#### NameError
```
print(greetings)

# NameError: name 'greetings' is not defined
```

<details> 
  <summary>
   What is the fix?
  </summary>
   
  ```
  greetings = 'Howdy 🤠'
  print(greetings)

  # Output: Howdy 🤠
  ```

</details>

#### TypeError
```
message = 'The air quality is '
print(message + 28)

# TypeError: can only concatenate str (not "int") to str
```

<details> 
  <summary>
    What is the fix?
  </summary>
   
  ```
  message = 'The air quality is '
  print(message + str(28))

  # Output: The air quality is 28
  ```

</details>

### Control Flow
`If/Else` are used to control the flow of code execution.

```
import random

num = random.randint(0, 1)   # Generates a random number that's either 0 or 1

if num > 0.5:
  print('Heads')
else:
  print('Tails')
```

If the condition evaluates to `True`, code in the if part is executed.
If the condition evaluates to `False`, code is skipped.

### Relational Operators

* `==` equal to
* `!=` not equal to
* `>`  greater than
* `<`  less than
* `>=` greater than or equal to
* `<=` less than or equal to

### Elif

One or more elif statements (short for "else if") can be optionally added in between the if and else to provide additional condition(s) to check. 
Sometimes two is simply not enough.

```
if grade > 90:
  print('A')
elif grade > 80:
  print('B')
elif grade > 70:
  print('C')
elif grade > 60:
  print('D')
else:
  print('F')
```

### Logical Operators

Logical operators, also known as Boolean operators, combine and evaluate two conditions. They are `and`, `or`, and `not` operators:

- `and` returns `True` if both conditions are `True`, and returns `False` otherwise.
- `or` returns `True` if at least one of the conditions is `True`, and `False` otherwise.
- `not` returns `True` if the condition is `False`, and vice versa.

```
if hunger > 4 and anger > 1:
  print('Hangry')
```

```
if coffee > 0 or bubble_tea > 0:
  print('😊')
```

```
if not tired:
  print('Time to code!')
```

How to remember when to use which?

|A|B|A and B|A or B|
|-----|-----|-----|-----|
|False|False|False|False|
|False|True|False|True|
|True|False|False|True|
|True|True|True|True|

#### Nested Ifs
```
weather = 'Sunny'
humidity = 35

if weather == 'Sunny':
  if humidity < 60:
    print('Let’s go to the beach! 🏖️')
  else:
    print('Hmmm, it’s a little humid for a beach day.')
else:
  print('It’s not sunny today... let’s try for another day.')
```

#### Loop

In programming, a loop is used to repeat a block of code until a specified condition is satisfied. 
People will often use the generic term “iterate” when referring to loops; iterate simply means “to repeat”.

#### While
Continue something until a condition is met.
```
print('BANK OF BRAMPTON')

pin = int(input('Enter your PIN: '))

while pin != 1234:
  pin = int(input('Incorrect PIN. Enter your PIN again: '))

if pin == 1234:
  print('PIN accepted!')
```

A while loop looks very similar to an if statement. Just like an if statement, it executes the code if the condition is True.
However, the difference is that the while loop will continue to execute the code inside of it, over and over again, as long as the
condition is True.

#### for ...
##### range()
```
for i in range(6):
  print(i)
```
To loop through a set of code a specified number of times, we can use a for loop and the range() function.
The range() function returns a sequence of numbers. By default, the sequence starts at 0 and increments by 1, ending at a specified number.

### String Concatenation
```
for i in range(5):
  print('The square of ' + str(i) + ' is ' + str(i*i))
```

### String interpolation
```
for i in range(5):
  print(f'The square of {i} is {i*i}')
```

#### nested loops
```
for i in range(1, 6):
  for j in range(1, 6):
    print(i * j)
```

```
i = 0
while i < 6:
  j = 0
  while j < 6:
    print(i * j)
    j = j + 1
  i = i + 1
```

### Importing Modules
In Python, modules are .py files containing Python code that can be imported inside another Python program. 
The Python standard library contains well over 200 modules that we can use. We can also install and use other python modules or libraries made by others.

### Lists
Creating a bunch of variables for storing numbers is tedious and error-prone. Can you imagine what it would be like with 100+ variables?
`list_name = [item1, item2, item3, item4]`

Data that could be stored in a list:

Temperatures in the past week.
pH level of the office plant in the past hour.
"Now playing" in the movie theater nearby.
```
temp = [86, 80, 82, 87, 79, 80, 82]
ph = [7.2, 7.1, 7.0, 7.0, 7.2, 7.1]
now_playing = ['Barbie', 'Oppenheimer', 'Talk to Me', 'Blue Beetle']
```

More facts about lists:

* List items allow duplicate values.
* Lists can have values with different data types.
* There's no limit to how much data a list can hold.

#### Index
List items are changeable, meaning we can update individual items within a list.

But before we do that, how can we access an individual item within a list? Well, this is where index comes in.

An index is an item's position in a list.

Python is 0-indexed, meaning that the indices starts at 0:
```
vowels = ['a', 'e', 'i', 'o', 'u']
# Index:   0    1    2    3    4
```

```
print(vowels[0])     # Output: a
print(vowels[1])     # Output: e
print(vowels[2])     # Output: i
print(vowels[3])     # Output: o
print(vowels[4])     # Output: u

vowels = ['a', 'e', 'i', 'o', 'u']
# Index:   0    1    2    3    4
# Index:  -5   -4   -3   -2   -1
```

#### Slicing
```
vowels = ['a', 'e', 'i', 'o', 'u']

print(vowels[0 : 3])
print(vowels[1 : 3])

# Output:
# ['a', 'e', 'i']
# ['e', 'i']
```
Instead of accessing an item using a single index like `name[index]`, 
we can get multiple items by specifying where to start and where to end the range like `name[start : end]`

#### IndexError
```
Traceback (most recent call last):
    print(vowels[5])
IndexError: list index out of range
```

### Built in functions
Python comes with some built-in functions, including ones specifically for lists.

Here are some examples:

The `len()` function returns the total length of a list.

The `max()` function returns the maximum value in a list.

The `min()` function returns the minimum value in a list.


```
stock1_prices = [2.52, 2.44, 2.32, 2.41, 2.51, 2.50, 2.44]
stock2_prices = [8.36, 8.31, 8.21, 8.21, 8.25, 8.11, 8.13]

print(len(stock1_prices))      # Output: 7
print(max(stock1_prices))      # Output: 2.52
print(min(stock2_prices))      # Output: 8.11
```

### List Methods

Besides built-in functions, Python has a bunch of built-in list methods that are very handy.

Here are some of them:

`.append()` method adds an item to the end of the list.

`.insert()` method adds an item to a specific index.

`.remove()` method removes an item from a list based on the value.

`.pop()` method removes the item at a particular index.

```
dna = ['AUG', 'AUC', 'UCG']

dna.append('UAA')     # ['AUG', 'AUC', 'UCG', 'UAA']
dna.insert(2, 'GAU')  # ['AUG', 'AUC', 'GAU', 'UCG', 'UAA']
dna.remove('AUC')     # ['AUG', 'GAU', 'UCG', 'UAA']
dna.pop(0)            # ['GAU', 'UCG', 'UAA']
```

| List Method | Description |
|-------------|-------------|
| `.append()` | Add an item to the end of the list |
| `.clear()`  | Remove all items from the list |
| `.copy()`   | Return a shallow copy of the list |
| `.count()`  | Return the number of times the value appears in the list |
| `.extend()` | Appends another list to the current list by extending it |
| `.index()`  | Returns the index of a value inside the list |
| `.insert()` | Insert an item at a specified position in the list |
| `.pop()`    | Remove an item from a specified position in the list |
| `.remove()` | Remove an item from the list based on the value of the item |
| `.reverse()`| Reverses the list in place |
| `.sort()`   | Sorts the list in place |

#### Iterating over lists
```
snowfall = [0.3, 0.0, 0.0, 1.2, 3.9, 2.2, 0.8]

for i in snowfall:
  print(i)
```

`range()` function returns a sequence of numbers, from 0 to a number.

len() function returns the length of the list.
```
snowfall = [0.3, 0.0, 0.0, 1.2, 3.9, 2.2, 0.8]

for i in range(len(snowfall)):
  print(snowfall[i])
```

#### Bonus - Nested lists
```
list = ['a', 'b', 'c', [1, 2, 3]]
print(list[3][1])

student1 = ['Jerry', ['CompSci', 'Math'], 2026]
student2 = ['Ellie', ['InfoSci', 'Game Design'], 2024]
student3 = ['Daniel', 'CompSci', 2028]

test_scores1 = [[760, 760, 780], 32]
test_scores2 = [745, 32]
test_scores3 = [720, [31, 33]]
```

### Functions

A function is a reusable block of code that performs a specific task. 
To execute this block of code, you just need to write the function's name, followed by a pair of parenthesis ( )

User-defined functions are functions we define ourselves to do a specific task, and it's a two-step process: 1) define and 2) call.
```
def name():
  # The code inside
```

Lets see how to use it

```
def say_hello():
  print('Howdy! 🤠')
  print('How are you?')

say_hello()
```

#### Parameters and arguments
```
def happy_birthday(name):
  print("Happy birthday "+ name)
```

#### Return arguments
```
def add(x, y):
  answer = x + y
  return answer

total = add(4.99, 9.99)   # total is 14.98

print(add(3, 4))          # Same thing as print(7)
print(add(1, 5))          # Same thing as print(6)
print(add(5, 3))          # Same thing as print(8)
```

#### Scope
Suppose we created a variable inside the body of a function. Can we use it outside of the function? Well, let's see.
Define a function named `add()` and print the variable answer outside of it:

```
def add(x, y):
  answer = x + y
  return answer

print(answer)
```
Does this work? How do we fix it?
What are global scope variables?

### Next up
* Classes and objects
* Modules
* Numpy
* Pandas
* Azure + web technologies


