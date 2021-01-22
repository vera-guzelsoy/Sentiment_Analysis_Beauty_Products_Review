# Sentiment Analysis on Beauty Products using NLP

## Introduction
The company wants to develop a software tool that will identify the positive and negative words which customers use when they write reviews for the beauty products as their purchase inclination. For that, they gave their 9 years beauty products’ reviews between 2005-2014 and asked us to develop a model which will identify positive and negative words used in the reviews as a component of customer’s sentiment towards to the company’s beauty products. 

## Project Proposal 
The problem and approach to solve the problem in project proposal. You can click [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Capstone%20Project%20Proposal.pdf) to reach it. 

## Data

The data is in Standford Analysis Project (SNAP) webpage. The original data was in a JSON format there. In order to analyze the data, I imported JSON package and decoded JSON file with using query in order to convert JSON file to csv file format. The original dataset for this project can be found [here](http://snap.stanford.edu/data/amazon/productGraph/categoryFiles/reviews_Beauty_10.json.gz)

## Data Wrangling
Data wrangling is held in 3 sections:
1-Data Inspection [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/1-Data_Inspection.ipynb)
2-Statistics and Kendall [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/2-Statistics_Kendall.ipynb)
3-Text Preprocessing [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/3-Text_Preprocessing.ipynb)

## Exploratory Data Analysis
Univarate and bivariate analysises are done by using bar charts and wordcloud visualizations. These analysis can be found [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Data_Storytelling.ipynb)

Milestone report as Data Wrangling and EDA Report can be found [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Wrangling%26EDA_Report.pdf)


## Modeling
This is a supervised binary classification problem. We are trying to predict the sentiment based on the reviews on beauty products in Amazon e-commerce online platform. We used Python’s Scikit Learn libraries to solve the problem.

Since the ratings of the reviews were not distributed normally, we decided to decrease rating classes from 5 to 2 by merging Rating 1-2 as ‘Bad’ and Rating 4-5 as 'Good' while dropping Rating 3 from the dataset.

For feature selection, we applied threshold for word occurrence with using min_df/max_df, PCA and Singular Value Decomposition. For feature engineering, we applied CountVectorizer, TF-IDF, Hashing Vectorizer and Word2Vec to the text data in order to turn a collection of text documents into numerical feature vectors.

In this context, we implemented Logistic Regression, Random Forest, Naive Bayes, XGBOOST, CatBoost algorithms and Simple Neural Network as well.

PS:
Because of that the dataset is imbalanced, we have chosen different strategies:
1st: As a result of modeling results, we took into attention the f1 score instead of precision or recall.
2nd: While implementing the modeling algorithms, we used the advantages of parameters. For example: while applying logistig regression I used this parameter: class_weight:balanced
3rd: While improving the modeling results, we used SMOTE syntetic minority oversampling technique.

Modeling notebooks can be reached from following links. 

- [Count Vectorizer, TF-IDF, Hashing Vectorizer with Traditional Algorithms](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Sentiment_Analysis-1_CV-TF_IDF-HASH.ipynb)

- [Threshold for word occurence, PCA, Singular Value Decomposition, SMOTE techniques](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Sentiment_Analysis-2_EXPWORDLST-SMOTE-PCA-TRNCTDSVD.ipynb)

- [Word2Vec with Keras](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Sentiment_Analysis-3_Word2Vec-Keras.ipynb)


## Conclusion
Final report can be found [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Final-Report.pdf)

Project Presentation can be found [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Presentation.pptx)

Project Presentation keynote can be found [here](https://github.com/vera-guzelsoy/Sentiment_Analysis_Beauty_Products_Review/blob/main/Presentation-Keynotes.pdf)
