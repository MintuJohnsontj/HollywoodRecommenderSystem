# Hollywood Movie Recommendation System

## Features
  1. Recommendation system using cosine similarity metrics.
  2. Sentimental analysis using Naive Bayes classifier. 
  3. Website for recommendation and sentimental analysis using Python Flask framework

## Model Pipeline
### 1. Data Collection
    Collect the required data from kaggle and wikipedia web scraping.
    
1. [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)

    
2. [5000 Movie dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)

    
3. [List of American films of 2021](https://en.wikipedia.org/wiki/List_of_American_films_of_2021)  
    
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

## Text Preprocessing
### 1. Stop Word Removal
Stopwords are the words in any language which does not add much meaning to a sentence. They can safely be ignored without sacrificing the meaning of the sentence. For some search engines, these are some of the most common, short function words, such as the, is, at, which, and on. In this case, stop words can cause problems when searching for phrases that include them, particularly in names such as “The Who” or “Take That”.

If we have a task of text classification or sentiment analysis then we should remove stop words as they do not provide any information to our model, i.e keeping out unwanted words out of our corpus, but if we have the task of language translation then stopwords are useful, as they have to be translated along with other words.
There is no hard and fast rule on when to remove stop words. But it is suggeted that remove stop words if our task to be performed is one of Language Classification, Spam Filtering, Caption Generation, Auto-Tag Generation, Sentiment analysis, or something that is related to text classification.

On the other hand, if our task is one of Machine Translation, Question-Answering problems, Text Summarization, Language Modeling, it’s better not to remove the stop words as they are a crucial part of these applications.

### 2. TF-IDF
TF-IDF is an abbreviation for Term Frequency Inverse Document Frequency. This is very common algorithm to transform text into a meaningful representation of numbers which is used to fit machine algorithm for prediction.

## Model Evaluation
### AUC-ROC curve
https://www.analyticsvidhya.com/blog/2020/06/auc-roc-curve-machine-learning/
[](https://www.analyticsvidhya.com/blog/2020/06/auc-roc-curve-machine-learning/)

  The Receiver Operator Characteristic (ROC) curve is an evaluation metric for binary classification problems. It is a probability curve that plots the TPR against FPR at various threshold values and essentially separates the ‘signal’ from the ‘noise’. The Area Under the Curve (AUC) is the measure of the ability of a classifier to distinguish between classes and is used as a summary of the ROC curve.

_The higher the AUC, the better the performance of the model at distinguishing between the positive and negative classes._

When AUC = 1, then the classifier is able to perfectly distinguish between all the Positive and the Negative class points correctly. If, however, the AUC had been 0, then the classifier would be predicting all Negatives as Positives, and all Positives as Negatives.

When 0.5<AUC<1, there is a high chance that the classifier will be able to distinguish the positive class values from the negative class values. This is so because the classifier is able to detect more numbers of True positives and True negatives than False negatives and False positives.

When AUC=0.5, then the classifier is not able to distinguish between Positive and Negative class points. Meaning either the classifier is predicting random class or constant class for all the data points.

So, the higher the AUC value for a classifier, the better its ability to distinguish between positive and negative classes.

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

### Components:
The microframework Flask is part of the Pallets Projects (formerly Pocoo), and based on several others of them.

#### 1. Werkzeug
Werkzeug (German for "tool") is a utility library for the Python programming language, in other words a toolkit for Web Server Gateway Interface (WSGI) applications, and is licensed under a BSD License. Werkzeug can realize software objects for request, response, and utility functions. It can be used to build a custom software framework on top of it and supports Python 2.7 and 3.5 and later.

#### 2. Jinja
Main article: Jinja (template engine)
Jinja, also by Ronacher, is a template engine for the Python programming language and is licensed under a BSD License. Similar to the Django web framework, it handles templates in a sandbox.

#### 3. MarkupSafe
MarkupSafe is a string handling library for the Python programming language, licensed under a BSD license. The eponymous MarkupSafe type extends the Python string type and marks its contents as "safe"; combining MarkupSafe with regular strings automatically escapes the unmarked strings, while avoiding double escaping of already marked strings.

#### 4. ItsDangerous
ItsDangerous is a safe data serialization library for the Python programming language, licensed under a BSD license. It is used to store the session of a Flask application in a cookie without allowing users to tamper with the session contents.
