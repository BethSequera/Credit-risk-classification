# Loan Risk Analysis README

## Overview of the Analysis

In this analysis, we aim to build machine learning models to assess the creditworthiness of borrowers using historical lending data from a peer-to-peer lending services company. The primary goal is to predict whether a loan is healthy (0) or high-risk (1). We will go through various stages of the machine learning process to achieve this goal.

### Data Overview

The dataset, named "lending_data.csv," contains the following features:

- `loan_size`: The size of the loan.
- `interest_rate`: The interest rate of the loan.
- `borrower_income`: Income of the borrower.
- `debt_to_income`: Debt-to-income ratio of the borrower.
- `num_of_accounts`: The number of accounts held by the borrower.
- `derogatory_marks`: The number of derogatory marks on the borrower's credit report.
- `total_debt`: The total debt of the borrower.
- `loan_status`: The target variable, indicating whether a loan is healthy (0) or high-risk (1).

### Stages of the Machine Learning Process

1. **Data Preparation:**
   - Read the dataset from the provided CSV file.
   - Split the data into features (X) and labels (y).
   - Checked the balance of the labels variable (y).

2. **Logistic Regression Model with Original Data:**
   - Fit a logistic regression model to the training data (X_train and y_train).
   - Made predictions on the testing data (X_test).
   - Evaluated the model's performance:
     - Calculated the accuracy score.
     - Generated a confusion matrix.
     - Printed the classification report.

3. **Logistic Regression Model with Resampled Training Data:**
   - Resampled the training data using RandomOverSampler to balance the labels.
   - Fit a logistic regression model to the resampled training data.
   - Made predictions on the testing data.
   - Evaluated the model's performance, including accuracy, precision, recall, and the confusion matrix.

## Results

### Machine Learning Model 1 (Logistic Regression with Original Data):

- Accuracy Score: 0.9924
- Balanced Accuracy Score: 0.994
- Confusion Matrix:
  ```
  [[18679, 80],
   [67, 558]]
  ```
- Classification Report:
  ```
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.89      0.88       625

    accuracy                           0.99     19384
   macro avg       0.94      0.94      0.94     19384
  weighted avg    0.99      0.99      0.99     19384

### Machine Learning Model 2 (Logistic Regression with Resampled Data):

- Accuracy Score (Resampled Data): 0.9952
- Balanced Accuracy Score (Resampled Data): 0.9959
- Confusion Matrix (Resampled Data):
  ```
  [[18668, 91],
   [2, 623]]
  ```
- Classification Report (Resampled Data):
  ```
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      1.00      0.93       625

    accuracy                           1.00     19384
   macro avg       0.94      1.00      0.96     19384
  weighted avg    1.00      1.00      1.00     19384

## Summary

Both machine learning models performed exceptionally well in predicting loan risk, with high accuracy, balanced accuracy, and precision. However, Model 2, trained with resampled data, achieved slightly better results, especially in terms of recall for class 1 (high-risk loans). The ability to identify high-risk loans is crucial for risk assessment in lending.

In conclusion, Model 2, which uses logistic regression with resampled data, is recommended for predicting loan risk. It provides a better balance between precision and recall for high-risk loans. The choice of the model may depend on the specific problem and the importance of correctly predicting healthy and high-risk loans, but overall, Model 2 offers superior performance.

If you have any questions or need further assistance, feel free to reach out to the project team for support. Happy analyzing!Happy coding!
