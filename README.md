# Netflix EDA and Recommendation

## Overview
This project performs Exploratory Data Analysis (EDA) on Netflix's movie and TV show dataset, uncovering trends in content distribution, genres, ratings, and more. It also builds a content-based recommendation system using TF-IDF vectorization and cosine similarity to suggest similar titles based on descriptions, directors, casts, and genres.

Key goals:
- Analyze Netflix content patterns (e.g., by country, year, type).
- Develop and iterate on a recommendation engine for personalized suggestions.

This is my first EDA project, built with Python in a Jupyter Notebook. Feedback welcome!

## Dataset
- Source: Netflix Titles Dataset(https://www.kaggle.com/datasets/shivamb/netflix-shows) (netflix_titles.csv, ~8,800 entries).
- Features: Title, type (Movie/TV Show), director, cast, country, release year, rating, duration, listed genres, description.

## Requirements

Python 3.x
Libraries: pandas, numpy, matplotlib, seaborn, wordcloud, scikit-learn (install via pip install -r requirements.txt)

## How to Run

1. Clone the repo: git clone https://github.com/yourusername/netflix-eda-recommendation.git
2. Install dependencies: pip install -r requirements.txt
3. Open the Jupyter Notebook: jupyter notebook Netflix_EDA_and_Recommendation.ipynb
4. Run all cells to perform EDA and test recommendations.

## Project Structure

- Data Loading & Cleaning: Load CSV, handle missing values (e.g., fill 'Unknown'), parse durations and genres.

- EDA:
  1. Distributions: Movie vs. TV Show (pie chart), top countries/producers (bar plots).
  2. Trends: Release years, ratings, durations (histograms, box plots).
  3. Genres: Top categories, word clouds for descriptions and genres.
  4. Correlations: Heatmap for numeric features.

## Recommendation System:
Version 1: TF-IDF on combined features (description + director + cast + genres).
Version 2: Separate matrices for genres and other text.
Version 3: Weighted combination (60% genres, 40% others) for improved relevance.
Example: Recommendations for "Stranger Things" and "Emily in Paris".

## Insights:
- US dominates content (~30%), followed by India/UK.
- TV-MA/TV-14 are most common ratings.
- Genres like Drama/Comedy prevail; recommendations align better with genre weighting.


## Results

- EDA reveals growth in Netflix originals post-2010, with movies outnumbering TV shows.
- Recommender improves iteratively: Initial version had noise; final version prioritizes genre matches for thematic similarity (e.g., supernatural shows for "Stranger Things").

## Limitations & Future Work

- Relies on content similarity (no user ratings for collaborative filtering).
- TF-IDF can miss semantic nuances; future: Use BERT embeddings.
- Add interactivity (e.g., Streamlit dashboard).
- Incorporate more data (e.g., IMDb ratings) or hybrid filtering.

## Author

ttbyun – Math student exploring data science.

Feel free to discuss more with me! ><
