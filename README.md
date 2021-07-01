# Hollywood Movie Recommendation System

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
### 3. Model Building, Training and Evaluation 
      - Use Multinomial Naive Bayes for sentiment classification 
      - Calculate accuracy score for model evaluation
### 4. Model Deployment
      - Use Flask framework for website development

## Cosine Similarity
  Cosine similarity measures the similarity between two vectors of an inner product space. It is measured by the cosine of the angle between two vectors and determines whether two vectors are pointing in roughly the same direction. It is often used to measure document similarity in text analysis.
  
## Multinomial Naive Bayes
  Naive Bayes model applies Bayes theorem with a Naive assumption of no relationship between different features. According to Bayes theorem:
P(A|B) = P(A) * P(B|A)/P(B)

Where we are calculating the probability of class A when predictor B is already provided.

P(B) = prior probability of B; P(A) = prior probability of class A; P(B|A) = occurrence of predictor B given class A probability.

  Assuming Gaussian distribution will give rise to Gaussian Naive Bayes (GNB) or multinomial distribusion will give Multinomial Naive Bayes (MNB).
  
 ## Flask Framework
 Flask is a micro web framework written in Python. It is classified as a microframework because it does not require particular tools or libraries. It has no database abstraction layer, form validation, or any other components where pre-existing third-party libraries provide common functions. However, Flask supports extensions that can add application features as if they were implemented in Flask itself. Extensions exist for object-relational mappers, form validation, upload handling, various open authentication technologies and several common framework related tools.
