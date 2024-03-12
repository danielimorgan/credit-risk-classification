# Credit Risk Classification Report

## Overview of the Analysis

Two machine learning models were built to identify the creditworthiness of borrowers, using a dataset of historical lending activity from a peer-to-peer lending services company.

The data included factors such as: the loan size and it's interest rate; the borrower's income, debt-to-income ratio, number of accounts, total debt, and if there is derogatory marks against the borrower.

The model needed to predict whether the loan is a healthy or a high-risk loan based on the factors above.
Both machine learning models were built by using the `LogisticRegression` module and the dataset was split into a training and testing sets. 

The first model had 75,036 healthy loan status and 2500 high-risk datapoints.

In the second logistic regression model, the dataset was resampled using the `RandomOverSampler` module, which equalized the loan status datapoints into 56277 points for each status.


## Results

* Machine Learning Model 1:
    * Accuracy: 99%
    * Precision: 100% for healthy loans(`0`), 87% in predicting high-risk loans(`1`).
    * Recall scores: 100% for hearlthy loans(`0`), 89% for high-risk loans(`1`).

* Machine Learning Model 2:
    * Accuracy: 100%
    * Precision: 100% for healthy loans(`0`), 87% in predicting high-risk loans(`1`).
    * Recall scores: 100% for hearlthy loans(`0`), 100% for high-risk loans(`1`).

## Summary

While Model 2 had the better perfomance overall with an increase in total accuracy, using `RandomOverSampler` to equalize the data didn't help increase the percision in predicting high-risk loans (`0`). Considering that the original data had a lower count of high-risk loans, it becomes more important to try to predict those.
