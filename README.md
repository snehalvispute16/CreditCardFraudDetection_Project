# Credit Card Fraud Detection Project

## Overview
This repository contains the code and resources for a Credit card fraud detection project. The goal of the project is to identify fraudulent credit card transactions using machine learning techniques.

## Table of Contents
- [Dataset](#dataset)
- [Features](#features)
- [Results](#results)

## Dataset
The dataset used for this project is taken from 'https://www.kaggle.com/datasets/kartik2112/fraud-detection'. The link contains two datasets, 'fraudTrain.csv' and 'fraudTest.csv'. The train data contains 12,96,675 rows and 23 columns. Whereas, the test data contains 5,55,719 rows and 23 columns. 

## Features

The features present are as follows:
'Unnamed: 0', 'trans_date_trans_time', 'cc_num','merchant','category','amt', 'first','last', 'gender','street','city','state','zip','lat','long','city_pop','job', 'dob', 'trans_num','unix_time','merch_lat','merch_long','is_fraud'
where  
'is_fraud' = 1 indicates a fraudulent transaction and 'is_fraud' = 0 indicates a non-fraudulent transaction
'amt' indicates the amount of the transaction
'trans_date_trans_time' indicates the transaction's date and time
'cc_num' indicates credit card number 
'first' and 'last' indicate the first and last names 
'gender' indicates the gender: Male or Female as 'M' and 'F' respectively
'street', 'city', 'state', 'zip','lat', 'long' indicates the address information along with zip code, latitude and longitudes 
'dob' indicates the date of birth
 
The features used for fraud detection are as follows:'gender','category','state','amt','lat','long','city_pop','unix_time','merch_lat','merch_long' 

Feature Engineering:

Encoding Categorical Variables:
Converting categorical variables into numerical representations, such as one-hot encoding, label encoding, or target encoding
Scaling and Normalization:
Scaling numerical features to a standard range or normalizing them to ensure uniformity and prevent some features from dominating others
Feature Selection:
Choosing relevant features and discarding irrelevant or redundant ones to reduce dimensionality and improve model interpretability

## Results

- Overall Performance: XGBoost is the best performing model with the highest accuracy (99.32%), ROC score (89.14%), and F1 score (47.34%)

- Precision vs. Recall Trade-off: Models like Random Forest and KNN have higher precision but lower recall. On the other hand, models like Light GBM and XGBoost have a more balanced trade-off between precision and recall

- Model Specificity: KNN and SVM have lower ROC scores and F1 scores, suggesting they may not be as effective in distinguishing between positive and negative cases
