# TMDB Movies Dataset Analysis

## Dataset Description
This dataset contains information about 10,000 movies extracted from TMDB. The dataset includes movies from 1960 to 2015, covering user ratings and revenue information. The original data is sourced from [Kaggle TMDB Movies Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata).

## Columns Description
- `id`, `imdb_id`: Unique ID or IMDb ID for each movie on TMDB.
- `popularity`: A metric used to measure the popularity of the movie.
- `budget`: The total budget of the movie in USD.
- `revenue`: The total revenue of the movie in USD.
- `original_title`: The original title of the movie.
- `cast`: The names of the cast members separated by "|".
- `homepage`: The official website of the movie (if available).
- `director`: Name(s) of the director(s) (separated by "|" if multiple).
- `tagline`: A catchphrase describing the movie.
- `keywords`: Keywords related to the movie.
- `overview`: Summary of the movie plot.
- `runtime`: Total runtime of the movie in minutes.
- `genres`: Genres of the movie separated by "|".
- `production_companies`: Production compan(y/ies) of the movie.
- `release_date`: Release date of the movie.
- `vote_count`: Number of votes the movie received.
- `vote_average`: The average user rating of the movie.
- `release_year`: Release year of the movie (from 1960 to 2015).
- `budget_adj`: The total budget of the movie in USD, adjusted for inflation to 2010 dollars.
- `revenue_adj`: The total revenue of the movie in USD, adjusted for inflation to 2010 dollars.

## Questions for Analysis
1. Do movies with high popularity achieve high revenue?
2. What are the most filmed genres in the dataset?
3. Is there a correlation between a movie's budget and its revenue?

## Data Wrangling
The dataset can be found in the `tmdb-movies.csv` file provided in this repository. It is an edited version of the original Kaggle TMDB 5000 Movie Dataset provided by Udacity as part of the **Become a Data Analyst Nanodegree Program**.

## Data Cleaning
### Main Observations:
- The dataset consisted of a total of 10,866 rows and 21 columns.
- We found and removed 1 duplicate row.
- Columns that were not useful for our analysis were dropped.
- Several columns had missing values that needed handling.
- The `cast`, `director`, and `genres` columns had values separated by a '|'.
- The `release_date` column required conversion to a proper date data type.
- We added a column for movie profit using the formula: `profit = revenue - budget`.
- The `vote_average` column was categorized for better analysis.
- The `profit` column was also categorized for exploratory data analysis.

## Exploratory Data Analysis (EDA)
After cleaning the dataset, we had a total of 10,840 records and 10 columns with no duplicates or null values. The data types are consistent, and categorical variables were defined to address our analysis questions. We performed various analyses and visualizations to answer our targeted questions.

### Analysis Insights:
- **Q1: Do movies with high popularity achieve high revenue?**
  - More popular movies tend to generate significantly higher revenue than less popular ones.
- **Q2: What are the most filmed genres in the dataset?**
  - Drama, Comedy, and Action are the top three genres, with Drama alone accounting for 22.6% of the movies in the dataset.
- **Q3: Is there a correlation between a movie's budget and its revenue?**
  - There is a positive correlation between budget and revenue, indicating a relationship with some outliers present.

## Built With
- **JupyterLab**
- **Python 3**
- **Pandas**
- **NumPy**

