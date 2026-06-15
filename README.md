# Loan Approval Prediction System

A machine learning project that predicts whether a loan application is likely to be approved, based on factors like income, credit history, education, and employment status. Built with Python and Scikit-learn, and deployed as an interactive app on Hugging Face.

## Try it out

[Live demo on Hugging Face](https://huggingface.co/spaces/aminano/loan-approval-predictor)

## Why this project

Loan approval decisions depend on multiple factors, and it's often hard to see how these factors interact with each other. I wanted to explore how machine learning models can learn these patterns from historical loan data and use them to predict approvals for new applicants.

This project walks through the complete pipeline - from data preprocessing and model training to deployment as an interactive web app.

## What it does

You enter applicant details (income, credit history, loan amount, education, etc.) and the app shows:

- Whether the loan is likely to be **approved** or **not approved**, with a probability gauge
- A confidence interval around that prediction
- Suggested next steps depending on the result
- A downloadable CSV report of the result

## How it works

1. **Data cleaning** - dropped the Loan_ID column, filled missing categorical values with the mode and missing numerical values with the mean
2. **EDA** - looked at how loan status relates to credit history, education, property area, income, and number of dependents
3. **Encoding** - label-encoded categorical variables so the models could use them
4. **Model comparison** - trained and compared Random Forest, Logistic Regression, Decision Tree, and Gradient Boosting Classifiers using accuracy and 5-fold cross-validation
5. **Final model** - went with Random Forest (see below for why), saved it as a pickle file, and wrapped it in a Gradio app deployed on Hugging Face

The full process is in [`Loan_Approval_Pred_system.ipynb`](#) - link this to your Colab notebook or export it into the repo.

## Dataset

[Loan Prediction Problem Dataset](https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset) from Kaggle - 614 rows covering applicant gender, marital status, dependents, education, employment status, applicant and co-applicant income, loan amount, loan term, credit history, and property area. The target is loan status (approved / not approved).

## Model performance & why Random Forest

I compared four models - Random Forest, Logistic Regression, Decision Tree, and Gradient Boosting - using accuracy and 5-fold cross-validation.

Random Forest came out on top:

- **Accuracy:** ~77%
- **Cross-validation score:** ~81%

Logistic Regression was close behind (~78% accuracy), but Random Forest handled feature interactions better and was less sensitive to noise. 77% isn't a huge number, and the dataset's size, missing values, and class imbalance are part of why - but the goal here was an interpretable, complete pipeline rather than squeezing out the last percentage point.

## Tech stack

- Python, Pandas, NumPy
- Scikit-learn
- Seaborn / Matplotlib (for EDA)
- Gradio
- Hugging Face Spaces
- Google Colab

## What I'd add next

- SHAP values to explain individual predictions
- Address the class imbalance to push accuracy higher
- Try other models like XGBoost or LightGBM

## A note on this project

This was built for learning and as part of my portfolio - it's not meant to be used for real lending decisions.

## About me

Amina Ashfaq
Economics with Data Science, Information Technology University (ITU), Lahore
