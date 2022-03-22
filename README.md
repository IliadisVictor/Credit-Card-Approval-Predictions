[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
# Credit Card Approval Predictions

![Credit Card](images/credit-card.jpg)

## Context
Credit score cards use personal information and data submitted by credit card applicants , that allow banks to predict the probability of future defaults and credit card borrowings . It is a common risk control method in the financial industry that complements the decision process on whether to issue a credit card on an applicant or not. Simply put credit scores can objectively quantify the magnitude of risk . 
 
At present, with the development of machine learning algorithms. More predictive methods such as Boosting, Random Forest, and Support Vector Machines have been introduced into credit card scoring. However, these methods often do not have good transparency. It may be difficult to provide customers and regulators with a reason for rejection or acceptance , so the models must be used as a supplement on the evaluation of the application and not simply as a yes or no mechanism.

## Project Objective

Build a classification machine learning model to predict if an application for the issuance of a credit card should be accepted or not , based on the clients historical data labeling him as a good or bad client.

## Data 
Two Datasets :
* First Dataset application_record offer general information on the client. 18 columns for 438557 rows-clients.
* Second Dataset Historical data on client's credit behavior. 1048575 rows which contain information on the status of a payment x-months back from "today" for y client.

## Preparing Data
1. Remove missing data.
2. Drop Duplicates in application_record
3. Merge categories in categorical data
4. Dummy Variables encoding
5. Engineer variables
6. Remove outliers
7. Merge dataset

## Target Variable
We are going to assume that a client is a undesired client unfit for a credit card if one of the following is true :
* He has delayed payments of over 3 months in his credit record .
* The amount of times he delayed to pay from 1 month to 3 months , exceeds the amount of times he payed on time.

## Models Preparation
1. Industry standard born from the credit card scoring , **weight of evidence** and **information value** to evaluate which features hold enough predictive power to be used in our models.
2. Split data to train and test 0.3 train to 0.7 test.
3. Scale Features with MinMax .
4. Target Variable imbalance 0.85 false to 0.15 true , dealt with **SMOTE**

## Models Run
Logistic Regression, K-Nearest Neighbors, Support Vector Machine (SVM), Decision Tree, Random Forest, XGBoost and CatBoost 
