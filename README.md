# Movies-Dataset-Project-Using-Python

# Introduction:
This project aimed to analyze a dataset of movie information to uncover key insights related to profitability, IMDb ratings, and genre popularity. The dataset contained details on over 5,000 movies, including gross revenue, budget, ratings, and cast information. The primary objective was to clean and transform the data, and then perform exploratory data analysis to answer specific business questions.

# Project Objective:
The core objective of this project was to provide a data-driven understanding of what makes a movie successful, considering both financial returns and critical/audience acclaim. 
1. Which movies have generated the highest profits?
2. What are the top-rated films according to IMDb, and how do foreign language films perform within this elite group?
3. Who are the most consistently acclaimed directors?
4. What are the most lucrative genre combinations?
5. How do specific lead actors perform in terms of audience and critic engagement?

# Data Acquisition and Initial Inspection:

- **Acquisition:** I loaded the movie data from a CSV file using Pandas, specifically `('movie_data.csv')`. This is a standard and efficient way to bring tabular data into Python.
- **Initial Structure:**`movies.shape` immediately told me I was working with a substantial dataset: 5,043 rows and 28 columns. Knowing the dimensions upfront is crucial for planning.
- **Data Types and Non-Null Counts:** `movies.info()` provided a detailed summary, showing each column's data type (e.g., float64, object) and, critically, the number of non-null entries. This highlighted the immediate presence of missing values.
- **Descriptive Statistics:** For numerical columns, `movies.describe()` gave me quick statistical summaries like mean, standard deviation, and quartiles. This helps in understanding the distribution and range of values like gross, budget, and imdb_score.
- **Quantifying Missingness:** To precisely quantify the data quality issues, I used `movies.isnull().sum()` to count nulls per column, and then `round(100*(movies.isnull().sum()/len(movies.index)), 2)` to calculate the percentage of missing values. This revealed significant gaps, notably in gross (17.53%), budget (9.76%), and content_rating (6.01%), which directly informed my cleaning strategy.      
