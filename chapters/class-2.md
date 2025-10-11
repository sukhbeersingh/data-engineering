# Class 2

## NumPy

[NumPy](https://numpy.org/) (short for "Numerical Python") is a Python library that supports large, multi-dimensional arrays. It also comes with a bunch of math functions that you can use to operate on these arrays.

```
import numpy
```

or 

```
import numpy as np
```

Now, add this line to see the version number.

```
print(np.__version__)
```

### Numpy Array

An array is the core data structure of the NumPy package. It’s a grid of values.

Here’s what a Python list looks like:
```
rent = [1500, 1500, 1500, 1500, 1750, 1750] 
```
And here’s an example of a NumPy array:
```
rent = np.array([1500, 1500, 1500, 1500, 1750, 1750])
```

NumPy arrays are faster and more efficient than Python lists. When dealing with a huge dataset with millions of data, NumPy arrays can be 100x faster than traditional Python lists.

So when you have a handful of items, lists are great. But when dealing with thousands or even millions of numbers, NumPy arrays are the way to go!

### Indexing
similar to python lists, we can index numpy array. 
```
coffee = np.array([3, 2, 1, 0, 1])

print(coffee[0])   # Output: 3
print(coffee[1])   # Output: 2
print(coffee[2])   # Output: 1
print(coffee[3])   # Output: 0
print(coffee[4])   # Output: 1
```

### Slicing
Same thing with slicing! We can slice NumPy arrays the same way as Python lists.

Slicing is where we can access certain parts of a sequence. We can get multiple elements by specifying where to start slicing and where to end like `name[start : end]`.

For example:
```
coffee = np.array([3, 2, 1, 0, 1])

print(coffee[0:2])    # Output: [3 2]
print(coffee[2:])     # Output: [1 0 1]
print(coffee[-2:])    # Output: [0 1]
```
It starts from the start index (inclusive) and ends before the end index (non-inclusive)

### 2-D Arrays (optional)
So far in this course, we’ve been only working with 1D (1-dimensional) arrays:

```
arr = np.array([1, 2, 3, 4, 5, 6]) 
```
2D arrays have 1D arrays as elements, meaning arrays within an array.

For example:
```
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]]) 
```
We can also write the same 2D array in a grid format (easier for the eyes):
```
arr = np.array([
  [1, 2, 3], 
  [4, 5, 6],
  [7, 8, 9]
]) 
```
The element at index 0 is [1, 2, 3].

The element at index 1 is [4, 5, 6].

The element at index 2 is [7, 8, 9].

To output each of the elements:
```
print(arr[0])     # Output: [1, 2, 3]
print(arr[1])     # Output: [4, 5, 6]
print(arr[2])     # Output: [7, 8, 9]
```
We can also be more specific with `arr[row][column]`. For example:
```
print(arr[0][0])  # Output: 1
print(arr[0][2])  # Output: 3
print(arr[2][2])  # Output: 9
```
#### Examples of 2D Arrays

2D arrays appear more often than you think in real-world datasets.

For example, a seating plan for a room:
```
seating_plan = np.array([
  [0, 1, 3], 
  [2, 9, 5],
  [6, 7, 10]
]) 
```
A monthly budget (organized by month and category):
```
monthly_budget = np.array([
  [453.88, 192.44, 1750.00, 980.41, 578.22],   # month 1
  [689.77, 256.81, 1750.00, 865.34, 356.84],   # month 2
  [589.23, 293.42, 1850.00, 873.45, 789.23]    # month 3
]) 
```
A grade book where rows correspond to individual students and columns to scores:
```
gradebook = np.array([
  [98, 98, 90, 84, 93, 73, 80],                # student 1
  [93, 95, 75, 90, 89, 84, 76],                # student 2
  [90, 89, 88, 84, 90, 67, 72],                # student 3
  [89, 84, 69, 74, 84, 70, 72]                 # student 4
]) 
```

### Arithmetic Operations
```
import numpy as np

order = np.array([12.99, 9.99, 4.99, 12.99])

print(order * 0.8)   # Output: [10.39 7.99 3.99 10.39]
```
how would you have to do it with python lists?

### NumPy Functions

NumPy also comes with a bunch of math functions ([full list here](https://numpy.org/doc/stable/reference/routines.math.html)).

Here are some of the common ones:
```
.min() Return the minimum value of an array.
.max() Return the maximum value of an array.
.sum() Return the total sum of an array's values.
.average() Return the average value of an array.
```
This is what they look like in practice:
```
temperatures = np.array([[50, 51, 54, 59, 59, 53, 54, 51],
                         [45, 50, 38, 44, 40, 46, 43, 39]])

print(np.min(temperatures))       # Output: 38
print(np.max(temperatures))       # Output: 59
print(np.sum(temperatures))       # Output: 776
print(np.average(temperatures))   # Output: 48.5
```

### Axis
By default, these math operations apply to the array as though it were a list of numbers. However, by specifying the axis parameter, we can apply an operation along the specified axis of an array:
```
temperatures = np.array([[50, 51, 54, 59, 59, 53, 54, 51],
                         [45, 50, 38, 44, 40, 46, 43, 39]])

np.sum(temperatures, axis=0)   # Sum of each column
np.min(temperatures, axis=1)   # Min of each row
```
`axis=0`: each column

`axis=1`: each row

### Shape
NumPy arrays have a property called .shape that returns a tuple containing number of elements each dimension has.
```
arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]]) 

print(arr.shape)     # Output: (2, 4)
```
When we print arr.shape, we get (2, 4) because there are two dimensions:

The 1st dimension has 2 elements (for the rows).
The 2nd dimension has 4 elements (for the columns).
```
arr = np.array([
    [1, 2, 3], 
    [4, 5, 6], 
    [7, 8, 9], 
    [10, 11, 12]
]) 

print(arr.shape)     # Output: (4, 3)
```

### reshape
If we want to change the shape of an array, we use the .reshape() function.

Suppose we want to convert the following 1D array into a 2D one:
```
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8]) 
new_arr = arr.reshape(2, 4)

print(new_arr)

# Output:
# [[1 2 3 4]
# [5 6 7 8]]
```
Here we are turning the arr array into two dimensions:

The 1st dimension has `2` rows.

The 2nd dimension has `4` columns.

### arange

In Python, we have the built-in `.range()` function that we use in a `for` loop. Well, NumPy has something that looks similar called the `.arange()` function.

The `.arange()` function, short for “array range”, is a function that creates an array with evenly spaced values.

For example:
```
arr = np.arange(5)

print(arr)    # Output: [0 1 2 3 4]
```
You can go further with its three parameters:

- `start` is the first value in the array.
- `stop` is end of the range.
- `step` is step size of the intervals.
For example:
```
arr = np.arange(start=1, stop=10, step=3)

print(arr)   # Output: [1 4 7]
```
* We start with the value 1.
* We stop at the value 10.
* We go up 3 each time.

why isn't 10 included? 🤔 The reason is that the stop value is always an upper limit that's not part of the range

## Pandas

why?

🗂️ Import spreadsheets: Load file types like .csv (Comma-Separated Values), .xls (Excel files), or .json into Python so we can play around with them. 

🔎 Analyze data: Quickly calculate averages, totals, or spot missing values in seconds.

🧽 Clean and manipulate data: Rename columns, remove duplicates, and edit data programmatically. Saving hours of manual spreadsheet edits.

🥣 Prep data for visualization or machine learning: Get our data ready for libraries like matplotlib (data visualization) and scikit-learn (machine learning).

```
import pandas as pd

# Recent Oscar winners
movie_data = {
  'title': ['Parasite', 'Nomadland', 'CODA', 'Everything Everywhere All at Once', 'Oppenheimer', 'Anora'],
  'release_date': ['2019-05-30', '2020-09-11', '2021-01-28', '2022-03-11', '2023-07-21', '2024-05-24'],
  'genre': ['Thriller', 'Drama', 'Drama',  'Action', 'Biography', 'Drama'],
  'studio': ['CJ Entertainment', 'Searchlight Pictures', 'Apple TV+', 'A24', 'Universal Pictures', 'A24'],
  'budget': [11400000, 5000000, 10000000, 25000000, 100000000, 3000000],
  'box_office': [263000000, 39000000, 1900000, 143000000, 975000000, 57000000],
  'runtime_minutes': [132, 108, 111, 139, 180, 98],
  'rating': [8.5, 7.3, 8.0, 8.0, 8.6, 8.1]
}

# Create the DataFrame
movies = pd.DataFrame(movie_data)
```

### Dataframe
A DataFrame is the heart of the Pandas library. Think of it like a spreadsheet we can control with code: a table made up of rows and columns, where each column holds a specific type of data like numbers, text, or even dates.

### Creating Dataframes
from data dictionary
```
import pandas as pd

data = {
  'city': ['Brooklyn', 'Seoul', 'Barcelona', 'Mexico City'],
  'country': ['US', 'South Korea', 'Spain', 'Mexico'],
  'population': [2646000, 9411000, 1636000, 9209944]
}

df = pd.DataFrame(data)
```
from list of lists
```
data = [
  ['Brooklyn', 'US', 2646000],
  ['Seoul', 'South Korea', 9411000],
  ['Barcelona', 'Spain', 1636000],
  ['Mexico City', 'Mexico', 9209944]
]

df = pd.DataFrame(data, columns=['city', 'country', 'population'])
```
from a CSV File
```
df = pd.read_csv('my_filename.csv')
```

### Web technologies
[Azure services](https://bytebytego.com/guides/azure-services-cheat-sheet/)

![Azure services](./azure-cheat-sheet.png)


Next class
* more pandas
* sql
* etl
* data storage, governance