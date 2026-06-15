# Dataset

This folder contains the dataset used for training and evaluating the Loan Approval Prediction System.

## Source

Loan Prediction Problem Dataset from Kaggle:

https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset

## Description

The dataset contains information about loan applicants, including demographic, financial, and credit-related characteristics.

### Features

* Gender
* Marital Status
* Dependents
* Education
* Self Employment Status
* Applicant Income
* Co-applicant Income
* Loan Amount
* Loan Term
* Credit History
* Property Area

### Target Variable

* Loan Status (Approved / Not Approved)

## Data Preparation

Before model training:

* Missing categorical values were filled using the mode.
* Missing numerical values were filled using the mean.
* Categorical variables were encoded for machine learning models.
* The Loan_ID column was removed because it did not contribute to prediction performance.

