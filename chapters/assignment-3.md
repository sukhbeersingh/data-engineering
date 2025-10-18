# Assignment 3

In this assignment, you will work on a real world project for analysing data using pandas and sql. This is similar to what data engineers and data analysts work on often.

We will use Airbnb dataset consistint of six files with Airbnb rental listings of six cities: Austin, Bangkok, Buenos Aires, Cape Town, Istanbul, and Melbourne. You can access them via this [link](https://insideairbnb.com/get-the-data/). The data dictionary and filenames can be found at the bottom of this workbook.

Each row represents a listing with details such as coordinates, neighborhood, host id, price per night, number of reviews, and so on.

## 🧱 Part 1: Data Ingestion and Preparation

### 1. Load the Data
- Download the files into your local machine. Upload to databricks if you are using it. 
- Load the listings datasets for **all six cities** using Pandas.
- Ensure consistent column names across all datasets.
- Add a new column `"city"` to each DataFrame to identify the source city.

<details>
<summary> Sample code </summary>

```python
import pandas as pd
import os

# Define file paths for each city's listings.csv file
# Make sure the files are downloaded and stored in a folder called 'data'
city_files = {
    "Austin": "data/austin_listings.csv",
    "Bangkok": "data/bangkok_listings.csv",
    "Buenos Aires": "data/buenos_aires_listings.csv",
    "Cape Town": "data/cape_town_listings.csv",
    "Istanbul": "data/istanbul_listings.csv",
    "Melbourne": "data/melbourne_listings.csv"
}

# Empty list to hold DataFrames
city_dfs = []

# Load and label each city's dataset
for city, file_path in city_files.items():
    try:
        df = pd.read_csv(file_path)
        df['city'] = city  # Add city label
        city_dfs.append(df)
        print(f"✅ Loaded {city}: {df.shape[0]} rows")
    except Exception as e:
        print(f"❌ Error loading {city}: {e}")

```


</details>

### 2. Merge Datasets
- Combine the six city datasets into a **single unified DataFrame** for analysis.

<details>
<summary> Sample code</summary>

```python
# Combine all city DataFrames into one
all_listings = pd.concat(city_dfs, ignore_index=True)

# Preview combined dataset
print("\n📊 Combined dataset shape:", all_listings.shape)
print(all_listings[['id', 'name', 'city', 'price']].head())
```

</details>

### 3. Initial Exploration
- Print the **number of rows per city**.
- Display the **first 5 rows** of the combined dataset.
- Use `.describe()` to show basic statistics for:
  - `price`
  - `minimum_nights`
  - `number_of_reviews`

### 4. Clean the Data
- Convert the `price` column to **numeric** (strip dollar signs, commas, etc.).
- Convert `last_review` to **datetime**.
- Fill missing values:
  - Fill `reviews_per_month` with `0`
  - Fill `last_review` with `NaT` or similar placeholder
- Drop rows that have missing values in:
  - `host_id`
  - `neighbourhood`
  - `room_type`

---

## 📊 Part 2: Analysis & Engineering

### 5. Top Hosts by Number of Listings
- Identify the **top 10 hosts** (by `host_id`) across all cities who have the most listings.

### 6. Price Distribution by City
- For each city, calculate:
  - Average price
  - Median price
  - Minimum and maximum price
- *(Bonus)*: Create a **boxplot** to visualize price distribution per city.

### 7. Availability Analysis
- Find the **percentage of listings** with `availability_365 > 300` days for each city.
- Calculate the **average availability** per city.

### 8. Neighborhood Insights
- For each city:
  - Find the **top 3 neighborhoods** with the most listings.
- For each top neighborhood:
  - Calculate **average price**
  - Calculate **average number of reviews**
  - Identify the **most common room type**

### 9. Room Type Trends
- Group by `room_type` and calculate:
  - Average price
  - Number of listings
  - Average availability

### 10. Review Trends
- Calculate the **average number of reviews per listing**, per city.
- Identify the **top 5 listings** (by `id`) with the highest number of reviews across all cities.

---

## Part 3: Freestyle

🗺️ Explore: What is the distribution of prices across a city's neighborhoods? How does it change when you segment it further by room_type?           
🔎 Analyze: How do listings that require a minimum stay of a week or longer differ from those that don't?    

<b>Background</b>: An international real estate firm has hired you to research professional hosting on Airbnb. These are hosts that have multiple listings, make considerable income from their listings, and often manage teams to operate their listings. Examples include property managers and hospitality business owners.

<b>Objective</b>: Using the data from all six cities, you'll have to infer listings by professional hosts based on the distribution of `calculated_host_listings_count`. The lead consultant is interested in whether you can identify trends across listings operated by inferred professional hosts, as well as an estimation of the percentage of listings on Airbnb operated by professional hosts. This trend analysis is open to interpretation. No one should have the same answer, and there is no correct answer or one answer to this. This part is to help you deep dive and build a project for your portfolio.

You will need to prepare a report that is accessible to a broad audience. It will need to outline your motivation, analysis steps, findings, and conclusions.
This report can be a word document, a txt document, a presentation, a markdown (.md) page, or some other report format that you like.

## 🧠 Tips
- Use `groupby()`, `value_counts()`, `agg()`, `sort_values()` effectively.


## Folder structure
```
project/
│
├── data/
│   ├── austin_listings.csv
│   ├── bangkok_listings.csv
│   ├── buenos_aires_listings.csv
│   ├── cape_town_listings.csv
│   ├── istanbul_listings.csv
│   └── melbourne_listings.csv
│
├── report.txt                  # this is your report   
└── airbnb_analysis.ipynb.      # this is your notebook with all the code
```
