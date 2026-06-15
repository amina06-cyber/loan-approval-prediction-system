# Loan Approval Prediction System

A machine learning project that predicts whether a loan application is likely to be approved based on applicant demographics, financial information, credit history, and loan characteristics.

## Why I Built This Project

Loan approval decisions depend on multiple factors, and it is often difficult to understand how these factors interact. I wanted to explore how machine learning models can learn these patterns from historical loan data and provide approval predictions for new applicants.

This project walks through the complete machine learning pipeline, from data preprocessing and model training to deployment through an interactive web application.

## Project Goal

To build and deploy a classification model capable of predicting loan approval status using applicant information.

## Dataset

Source: Kaggle Loan Prediction Dataset

The dataset includes:

* Gender
* Marital Status
* Number of Dependents
* Education Level
* Self Employment Status
* Applicant Income
* Co-applicant Income
* Loan Amount
* Loan Term
* Credit History
* Property Area

Target Variable:

* Loan Status (Approved / Not Approved)

## Methodology

The project followed the following workflow:

1. Data Cleaning and Preprocessing
2. Exploratory Data Analysis (EDA)
3. Categorical Variable Encoding
4. Model Training
5. Model Comparison
6. Model Evaluation
7. Deployment using Gradio

## Models Evaluated

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier

## Final Model

Random Forest Classifier

Accuracy: 77%

Although the accuracy is moderate, Random Forest produced the most reliable overall performance among the models tested and captured nonlinear relationships within the dataset more effectively than Logistic Regression.

## Key Insight

Credit History emerged as the strongest predictor of loan approval.

Applicants with a positive credit history consistently showed a much higher likelihood of approval than applicants without one.

Other important factors included:

* Applicant Income
* Loan Amount
* Property Area
* Co-applicant Income

## Deployment

The model was deployed using:

* Gradio
* Hugging Face Spaces

The web application allows users to:

* Enter applicant information
* Receive a loan approval prediction
* View approval probability
* Download a prediction report

## Repository Structure

loan-approval-predictor/

├── data/

├── notebooks/

├── model/

├── app/

├── images/

├── requirements.txt

└── README.md

## Tools Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Gradio
* Google Colab
* Hugging Face Spaces

## Future Improvements

* Hyperparameter tuning
* Explainable AI using SHAP values
* Additional feature engineering
* Deployment using Flask or FastAPI
* Testing on larger financial datasets

## Author

Amina Ashfaq
