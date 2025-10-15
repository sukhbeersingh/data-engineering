# Assignment 2

## Problem 1
####  Create a numpy array with the elements  `"1, 2, 3, 5, 0"`, print the array and test if all of its elements are non-zero.

<details> 
  <summary>
    Hint:
  </summary>

  Use `np.all`. 

  https://numpy.org/doc/stable/reference/generated/numpy.all.html#numpy.all

</details>

#### Create a numpy array with the elements "0, 0, 0, 0", print the array and test if any of its elements is non-zero.

<details> 
  <summary>
    Hint:
  </summary>

  Use `np.any`. 

  https://numpy.org/doc/stable/reference/generated/numpy.any.html

</details>

#### Create a numpy array with the elements "56, -2, 7", print the array and the amount of memory required to store it.

<details> 
  <summary>
    Hint:
  </summary>

  Use `.nbytes`, `.itemsize` and `.shape`. 

</details>

#### Create a numpy array with 10 zeros and print the array.

<details> 
  <summary>
    Hint:
  </summary>

  Use `np.zeros`

</details>

#### Create a numpy array with 6 ones and print the array.

<details> 
  <summary>
    Hint:
  </summary>

  Use `np.ones`. 

</details>

#### Create a numpy array with 12 '3's and print the array. [3 3 3 3 3 3 3 3 3 3 3 3]

<details> 
  <summary>
    Hint:
  </summary>

  Use `np.full`. 

</details>

#### Create a numpy array of the integers from 8 to 20 and print the array. (make sure 20 itself is included) 

<details> 
  <summary>
    Hint:
  </summary>

  Use `np.arange`. 

</details>


## Problem 2
We've all been taught to check for cracked eggs before purchasing in grocery stores. But did you know that the probability of getting a rotten egg from a lot of 400 eggs is 3.5%?

Suppose we have a factory machine that determines the freshness of an egg (based on the expiration date, cracks in the shell, and smell) then assigns a number:

✨ 100% is a healthy fresh egg.

🤮 0% is completely rotten!
```
egg_carton1 = np.array([
  [0.89, 0.90, 0.83, 0.89, 0.97, 0.98], 
  [0.95, 0.95, 0.89, 0.95, 0.23, 0.99]
])

egg_carton2 = np.array([
  [0.89, 0.95, 0.84, 0.92, 0.94, 0.93], 
  [0.93, 0.95, 0.02, 0.03, 0.23, 0.99]
])

egg_carton3 = np.array([
  [0.83, 0.95, 0.89, 0.54, 0.37, 0.92], 
  [0.98, 0.99, 0.19, 0.23, 0.89, 0.91]
])
```
Which carton should you get?

Calculate the average freshness of each of the cartons with `np.average()` and see which one has the lowest average (least fresh) and the highest average (most fresh).

## Problem 3
Halley's Comet is a comet visible from Earth every 75 years. It is the only known "short-period comet" that is consistently visible to the naked eye from Earth. It was last seen in 1986 and the next one will happen in 2061. 💫

Using `.arange()`, create an array of numbers with the years when Halley's Comet will appear next from year 1986 to 3000.

## Problem 4

Use pandas

Titanic is a classic movie about one of the most famous shipwrecks in human history. 🚢

Below is an array filled with real data from 50 of the passengers:

* Passenger id (1 to 50)
* Survived: 0 for no and 1 for yes.
* Passenger class: 1 for Upper, 2 for Middle, 3 for Lower.
* Age: 0-74
```
passengers = np.array([
   [1, 0, 3, 22],
   [2, 1, 1, 38],
   [3, 1, 3, 26],
   [4, 1, 1, 35],
   [5, 0, 3, 35],
   [6, 0, 3, 18],
   [7, 0, 1, 54],
   [8, 0, 3, 2],
   [9, 1, 3, 27],
  [10, 1, 2, 14],
  [11, 1, 3, 4],
  [12, 1, 1, 58],
  [13, 0, 3, 20],
  [14, 0, 3, 39],
  [15, 0, 3, 14],
  [16, 1, 2, 55],
  [17, 0, 3, 2],
  [18, 1, 2, 12],
  [19, 0, 3, 31],
  [20, 1, 3, 8],
  [21, 0, 2, 35],
  [22, 1, 2, 34],
  [23, 1, 3, 15],
  [24, 1, 1, 28],
  [25, 0, 3, 8],
  [26, 1, 3, 38],
  [27, 0, 3, 2],
  [28, 0, 1, 1],
  [29, 1, 3, 5],
  [30, 0, 3, 18],
  [31, 0, 1, 40],
  [32, 1, 1, 70],
  [33, 1, 3, 33],
  [34, 0, 2, 66],
  [35, 0, 1, 28],
  [36, 0, 1, 42],
  [37, 1, 3, 5],
  [38, 0, 3, 18],
  [39, 0, 3, 18],
  [40, 1, 3, 14],
  [41, 0, 3, 40],
  [42, 0, 2, 27],
  [43, 0, 3, 29],
  [44, 1, 2, 0],
  [45, 1, 3, 19],
  [46, 0, 3, 33],
  [47, 0, 3, 14],
  [48, 1, 3, 22],
  [49, 0, 3, 41],
  [50, 0, 3, 18]
])
```
You can find the full dataset here: https://github.com/datasciencedojo/datasets/blob/master/titanic.csv

Your job as a data analyst is to find the following information:

- What is the shape of this array?
- What is the average age of the passengers?
- What is the passenger number of the oldest passenger? Who is the youngest?
- What is the percentage of folks that survived?
- And now the final question of all:

What is the percentage of the folks that survived based on their passenger class? 😮

## Problem 5
import pandas at the top of the file.

Then, create a DataFrame named contacts containing information about your friends, family, or fictional characters. Your DataFrame should have at least 3 columns and 4 rows.

Feel free to be creative about what columns to include. If you need inspiration, you could consider columns like name, age, phone_number, astrological_sign. 💫

For example:

|name|	age|	phone_number	|astrological_sign|
|----|----|-----------------|----------------|
|Bart|	10	|939-555-0113|	Taurus|
|Lisa|	8	|939-555-0114|	Virgo|
|Homer|	39|	939-555-0115|	Taurus|
|Marge|	36|	939-555-0116|	Pisces|

Create the DataFrame using either the dictionary method or the list-of-lists method.

Don't forget to display the table after creating it!