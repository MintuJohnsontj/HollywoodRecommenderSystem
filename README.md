# HollywoodRecommendationSystem

## Features
  1. Recommendation system using cosine similarity metrics.
  2. Sentimental analysis using Naive Bayes classifier. 
  3. Website for recommendation and sentimental analysis using Python Flask framework

## Model Pipeline
### 1. Data Collection
    Collect the required data from kaggle and wikipedia web scraping.
    1. https://www.kaggle.com/rounakbanik/the-movies-dataset
[The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)

    2. https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset
[5000 Movie dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)

    3. https://en.wikipedia.org/wiki/List_of_American_films_of_2021
  [List of American films of 2021](https://en.wikipedia.org/wiki/List_of_American_films_of_2021)  
    
### 2. Data Preprocessing
####  a) Preprocessing for Recommendation System
      - Read the data using Pandas dataframes.
      - Select the required features only.
      - Handle the null values.
      - Save data as csv file for future purposes.
####  b) Preprocessing for Sentimental Analysis
      - Identify the stopwords.
      - Convert the words into vectors using TF-IDF Vectorizer.
      - Split the data for training and testing.
#### 3. Model Building, Training and Evaluation 
      - Use Multinomial Naive Bayes for sentiment classification 
      - Calculate accuracy score for model evaluation
#### 4. Model Deployment
      - Use Flask framework for website development
