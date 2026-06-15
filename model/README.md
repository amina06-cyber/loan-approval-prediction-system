# Model

This folder contains the trained machine learning model used by the application.

## Final Model

Random Forest Classifier

## Why Random Forest?

Several classification models were evaluated during development, including:

* Random Forest
* Logistic Regression
* Decision Tree
* Gradient Boosting

Random Forest was selected because it achieved the strongest overall performance and handled feature interactions effectively.

## Performance

* Accuracy: ~77%
* Cross-Validation Score: ~81%

## Saved Model

The trained model is stored as:

```text
random_forest_model.pkl
```

This file is loaded by the Gradio application to generate loan approval predictions.

